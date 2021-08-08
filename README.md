# spin up docker container
docker-compose down && docker-compose build && docker-compose up -d

# docker-compose run --rm composer/npm/artisan

docker-compose run --rm composer create-project laravel/laravel .

composer install
npm install
npm run dev

docker-compose run --rm artisan cache:clear
docker-compose run --rm artisan config:clear
docker-compose run --rm php sudo chmod -R 777 storage

