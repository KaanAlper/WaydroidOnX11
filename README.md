Installing Weston and Waydroid
1) curl -sSL https://raw.githubusercontent.com/KaanAlper/WaydroidOnX11/refs/heads/main/install.sh | sudo bash
2) weston --socket=mysocket
3) sudo waydroid init -f -s GAPPS
4) waydroid show-full-ui

If it gives Uncertified GAPPS Error:
1) sudo waydroid shell
2) ANDROID_RUNTIME_ROOT=/apex/com.android.runtime ANDROID_DATA=/data ANDROID_TZDATA_ROOT=/apex/com.android.tzdata ANDROID_I18N_ROOT=/apex/com.android.i18n sqlite3 /data/data/com.google.android.gsf/databases/gservices.db "select * from main where name = \"android_id\";"
3) https://www.google.com/android/uncertified
4) use the number you got at step 2, send it and wait 2-3 min and finally restart waydroid
5) sudo waydroid session stop
6) waydroid show-full-ui
