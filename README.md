Запуск сервиса

dotnet run --project DeviceMonitoringService
Запуск клиентов (в отдельных терминалах)

# HTTP клиент
dotnet run --project HttpClient

# TCP клиент  
dotnet run --project TcpClient
Эндпоинты
Протокол	Адрес
HTTP	http://localhost:5000/DeviceService/http
TCP	net.tcp://localhost:8090/DeviceService/tcp
Методы службы
GetAllDevices() — список всех устройств

GetDevice(id) — информация об устройстве

PingDevice(id) — проверка доступности

GetServiceStats() — статистика вызовов

Структура

├── Contracts/     — контракты (общая библиотека)

├── Server/        — сервер ASP.NET Core + CoreWCF

├── HttpClient/    — консольный HTTP-клиент

└── TcpClient/     — консольный TCP-клиент
