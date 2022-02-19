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
