.PHONY : all up pull prune clean
all: pull up prune clean

up:
	docker-compose -p $$(hostname -s) up -d --build --remove-orphans
down:
	docker-compose -p $$(hostname -s) stop

pull:
	docker-compose -p $$(hostname -s) pull --include-deps
	docker-compose -p $$(hostname -s) build --pull
prune clean:
	docker container prune -f
	docker volume prune -f
	docker image prune -af
	docker network prune -f
	docker system prune -f
