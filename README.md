@echo off
REM Clear Windows cache

echo Clearing DNS cache...
ipconfig /flushdns

echo Clearing Windows Temp files...
del /q/f/s %TEMP%\*

echo Clearing Prefetch files...
del /q/f/s C:\Windows\Prefetch\*

echo Clearing browser cache for Chrome...
rmdir /q/s "%USERPROFILE%\AppData\Local\Google\Chrome\User Data\Default\Cache"

echo Cache cleared successfully!
pause
