# as

Cau 4: 
ông copy từ đây nha:
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="40dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintTop_toTopOf="parent">

        <EditText
            android:id="@+id/editText"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="Username" />

        <EditText
            android:id="@+id/editText2"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:hint="Password" />

        <LinearLayout
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            android:orientation="horizontal">

            <CheckBox
                android:layout_width="wrap_content"
                android:layout_height="wrap_content" />

            <TextView
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:text="Remember me" />
        </LinearLayout>

        <Button
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            android:text="login" />
    </LinearLayout>
</androidx.constraintlayout.widget.ConstraintLayout>


Cau 3: 

class PhanSo(private var tuso: Float,private var mauso: Float) {
    init {
        if (mauso == 0f) {
            tuso = 1f
            mauso = 1f
        }
    }
    fun printl() {
        println("Phan so la $tuso/$mauso")
    }
    fun add(phanSo: PhanSo) : PhanSo{
        val tuso = this.tuso* phanSo.mauso + this.mauso +phanSo.tuso
        val mauso = this.mauso * phanSo.mauso
        return PhanSo(tuso, mauso)
    }
}



private void saveText(String text, String name) throws IOException {
        OutputStream fos = null;
        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.Q) {
            ContentValues contentValues = new ContentValues();
            contentValues.put(MediaStore.MediaColumns.DISPLAY_NAME, name + ".txt");
            contentValues.put(MediaStore.MediaColumns.MIME_TYPE, "text/plain");
            contentValues.put(MediaStore.MediaColumns.RELATIVE_PATH, Environment.DIRECTORY_DOWNLOADS + "/text/");
            Uri uri = getContentResolver().insert(MediaStore.Files.getContentUri("external"), contentValues);
            fos = getContentResolver().openOutputStream(uri);
            fos.write(text.getBytes());
        } else {
            if (checkPermission()) {
                if (android.os.Build.VERSION.SDK_INT >= android.os.Build.VERSION_CODES.KITKAT) {
                    String textDir = Environment.getExternalStoragePublicDirectory(Environment.DIRECTORY_DOCUMENTS).toString();
                    File textFile = new File(textDir, name+ ".txt");
                    fos = new FileOutputStream(textFile);
                    final PrintStream printStream = new PrintStream(fos);
                    printStream.print(text);
                    printStream.close();
                }
            } else {
                if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.M) {
                    requestPermissions(new String[]{android.Manifest.permission.WRITE_EXTERNAL_STORAGE, Manifest.permission.READ_EXTERNAL_STORAGE},111);
                }
            }
            fos.close();
        }
    }
    
    
    https://flexiple.com/android/android-workmanager-tutorial-getting-started/
    
    https://stackoverflow.com/questions/50279364/android-workmanager-vs-jobscheduler
    
    https://medium.com/androiddevelopers/introducing-workmanager-2083bcfc4712
    
    https://blog.mindorks.com/integrating-work-manager-in-android
    
    https://viblo.asia/p/android-jetpack-series-chapter-1-workmanager-6J3ZgmqL5mB
    
    https://viblo.asia/p/tim-hieu-ve-workmanager-trong-android-jetpack-Az45bWbQKxY
    
    https://medium.com/android-news/how-scheduling-work-with-new-android-jetpack-component-workmanager-852163f4825b
    
    https://www.simplifiedcoding.net/android-workmanager-tutorial/
