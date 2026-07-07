# supreme-rotary-phone

پروژه شبیه‌سازی ارتباط TCP بین سرور و کلاینت با قابلیت ارسال پیام‌های دوره‌ای.

## توضیحات

این پروژه شامل یک سرور TCP و چند کلاینت است که ارتباط شبکه‌ای را شبیه‌سازی می‌کند. سرور به صورت خودکار پیام‌های مختلفی را برای کلاینت‌های متصل ارسال می‌کند.

## ساختار پروژه

```
websocket-python-data/
├── server.py          # سرور TCP اصلی
├── client.py          # کلاینت TCP
├── docker-compose.yml # تنظیمات Docker
├── Dockerfile.server  # Dockerfile برای سرور
├── Dockerfile.client  # Dockerfile برای کلاینت
└── .gitignore         # فایل‌های نادیده گرفته شده
```

## اجرای پروژه

### روش اول: اجرای مستقیم با Python

1. نصب Python 3.8 یا بالاتر
2. اجرای سرور:
   ```bash
   python server.py
   ```
3. اجرای کلاینت (در ترمینال جدا):
   ```bash
   python client.py
   ```

### روش دوم: اجرا با Docker

1. ساخت و اجرای سرویس‌ها:
   ```bash
   docker-compose up --build
   ```

2. توقف سرویس‌ها:
   ```bash
   docker-compose down
   ```

## ویژگی‌ها

- ارتباط TCP چند کلاینت
- ارسال خودکار پیام‌های دوره‌ای
- پشتیبانی از Docker
- مدیریت اتصال و خطاها

## پورت‌ها

- سرور: `4404`
