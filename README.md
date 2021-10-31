## Домашняя работа ADB
1. Отобразить подключённый девайс в консоли; 
```	
adb devices
```	
2. Установить .apk файл приложениия todolist на телефон с компьютера через ADB; 
```
adb install C:\Users\Дима\Desktop\app-debug.apk
```
3. Вывести адрес приложения todolist в системе Android; 
```
adb shell pm list packages | findstr todolist
```
4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде;
```
adb shell screencap /storage/emulated/0/DCIM/group_22.png && adb pull screencap /storage/emulated/0/DCIM/group_22.png C:\Users\Дима\Desktop\ADB
```
![22_1](https://user-images.githubusercontent.com/88891623/138939182-2221f40a-ae72-497d-8e90-22628ddc4bd8.PNG)

5. Вывести в консоль логи приложения todolist;
```
adb logcat | findstr -rnw "todolist"
```
6. Скопировать логи приложения todolist на компьютер;
```
adb logcat | findstr -rnw "todolist" > C:\Users\Дима\Desktop\ADB\todolist.log	
```
7. Удалить приложение todolist с телефона через ADB. 
```
adb uninstall com.android.todolist
```
