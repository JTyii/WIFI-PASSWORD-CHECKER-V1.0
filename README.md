# PASSWORD-CHECKER
@echo off<br/>
color 02<br/>
:menu<br/>
cls<br/>
echo --PASSWORD CHECKER--v1.0<br/>
echo.<br/>
echo.<br/>
echo Choose a number<br/>
echo.<br/>
echo 1.Start checking<br/>
echo 2.How to use<br/>
echo 3.Exit<br/>
set /p c=<br/>
if %c%==1 goto start<br/>
if %c%==2 goto ins<br/>
if %c%==3 goto exit<br/>
goto menu<br/>
:start<br/>
cls<br/>
echo --PASSWORD CHECKER--v1.0<br/>
netsh wlan show profiles<br/>
goto profiles<br/>
:profiles<br/>
echo Choose the wifi name you want to know the password and write down.<br/>
echo.<br/>
echo !!!Please type the exact wifi name as shown on the above.!!!<br/>
echo.<br/>
echo ATTENTION!!! If the wifi name have space between it, put "" at two sides of the name.<br/>
echo. <br/>
echo Ctrl+C , Ctrl+V is allowed to copypaste the wifi name.<br/>
pause<br/>
echo WIFI NAME:<br/>
set /p name=<br/>
echo HACKING.........<br/>
ping localhost -n 3 >nul<br/>
echo HACKING.........<br/>
ping localhost -n 2 >nul<br/>
goto hack<br/>
:hack<br/>
netsh wlan show profiles %name% key=clear<br/>
echo The password is shown at the above (key content)<br/>
pause<br/>
goto done<br/>
:done<br/>
cls<br/>
echo The password is already hacked.Thanks for using this app.<br/>
echo.<br/>
echo Do you want to hack again(y/Y) or exit(e/E)?<br/>
set /p choose=<br/>
if %choose%==y goto start<br/>
if %choose%==Y goto start<br/>
if %choose%==e goto exit<br/>
if %choose%==E goto exit<br/>
goto done<br/>
:ins<br/>
cls<br/>
echo --PASSWORD VIEWRER--v1.0<br/>
echo.<br/>
echo.<br/>
echo ATTENTION!!! If the wifi name have space between it, put "" at two sides of the name.<br/>
echo. <br/>
echo Ctrl+C , Ctrl+V is allowed to copypaste the wifi name.<br/>
echo Thanks.:D<br/>
echo.<br/>
echo MADE BY JTYII<br/>
pause<br/>
goto menu<br/>
:exit<br/>
echo This app is made by JTYII<br/>
pause<br/>
exit<br/>
