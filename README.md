# Запуск
docker build -t mock-api .
docker run -d -p 8000:8000 --name mock-api mock-api

# Тестирование
curl http://localhost:8000/order
curl http://localhost:8000/user  
curl http://localhost:8000/catalog | jq '.[0]'
