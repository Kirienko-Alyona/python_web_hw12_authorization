# python_web_hw12_authorization


docker run --name HW11 -p 5432:5432 -e POSTGRES_PASSWORD=1234 -d postgres


alembic revision --autogenerate -m 'Init' 
alembic upgrade head

poetry add python-jose["cryptography"]
poetry add passlib["bcrypt"]
poetry add python-multipart

Закрепим для чего необходимы эти пакеты в нашем приложении:

python-jose["cryptography"] это пакет, который предоставляет функциональность для работы с JSON Web Tokens (JWT) и помогает создавать безопасные токены аутентификации и авторизации для REST API
passlib["bcrypt"] пакет необходим для хеширования паролей пользователей. Хеширование паролей необходимо, чтобы их нельзя было восстановить в исходный вид, даже если данные утекут из базы данных.
python-multipart этот пакет для работы с файлами в формате multipart/form-data, который является основным форматом для загрузки файлов по HTTP, необходим в данном случае для правильной работы FastAPI.