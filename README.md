# three_layout
三个布局

1.linearlayout(线性布局）

它主要以水平和垂直方式来显示界面中的控件
``` android
    <?xml version="1.0" encoding="utf-8" ?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical" >
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal" >
        <Button
            android:id="@+id/btn_o1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,One" />
        <Button
            android:id="@+id/btn_o2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="One,Two"/>
        <Button
            android:id="@+id/btn_o3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,Three"/>
        <Button
            android:id="@+id/btn_o4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,Four"/>
    </LinearLayout>
```

![](https://i.loli.net/2019/03/13/5c88935c38990.png)

运行结果（上述代码为以上截图的一行）


2.constraintlayout(约束布局）
Constraint Layout是Google在2016年的Google I/O大会上提出的一个可以灵活控制子控件的位置和大小的新布局。并且其号称可以实现布局最大程度的扁平化。
``` android
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:layout_editor_absoluteY="81dp">

    <Button
        android:id="@+id/button9"
        android:layout_width="79dp"
        android:layout_height="47dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_red_dark"
        android:text="red"
        app:layout_constraintBottom_toBottomOf="@+id/button11"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.106"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/button11" />

    <Button
        android:id="@+id/button4"
        android:layout_width="67dp"
        android:layout_height="48dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@color/colorAccent"
        android:text="YELLOW"
        app:layout_constraintBottom_toBottomOf="@+id/button11"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.89"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/button11"
        app:layout_constraintVertical_bias="1.0" />

    <Button
        android:id="@+id/button5"
        android:layout_width="68dp"
        android:layout_height="45dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_green_light"
        android:text="GREEN"
        app:layout_constraintBottom_toBottomOf="@+id/button6"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.148"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/button6" />

    <Button
        android:id="@+id/button6"
        android:layout_width="62dp"
        android:layout_height="46dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:layout_marginBottom="8dp"
        android:background="@android:color/holo_blue_light"
        android:text="BLUE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.281" />

    <Button
        android:id="@+id/button7"
        android:layout_width="70dp"
        android:layout_height="44dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_purple"
        android:text="INDIGO"
        app:layout_constraintBottom_toBottomOf="@+id/button6"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.901"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/button6" />

    <Button
        android:id="@+id/button8"
        android:layout_width="277dp"
        android:layout_height="114dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@color/colorAccent"
        android:text="VIOLET"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        tools:layout_editor_absoluteY="281dp" />

    <Button
        android:id="@+id/button11"
        android:layout_width="62dp"
        android:layout_height="50dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="40dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_orange_light"
        android:text="ORANGE"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />
</android.support.constraint.ConstraintLayout>

```

![](https://i.loli.net/2019/03/13/5c88976daaf10.png)

3.linearlayout(表格布局）

表格布局是以表格形式排列控件的，通过行和列将界面划分成多个单元格
``` android
    <?xml version="1.0" encoding="utf-8"?>
<TableLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/TableLayout01"
    android:layout_width="match_parent" android:layout_height="match_parent"

    >
    <TableRow android:paddingLeft="16dp">
        <TextView android:text="Open..."
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:gravity="left"></TextView>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="match_parent"
            android:gravity="right"
            android:text="Ctrl+O"></TextView>
    </TableRow>


    <TableRow android:paddingLeft="16dp">
        <TextView android:text="Save..."
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:layout_height="wrap_content"></TextView>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="right"
            android:text="Ctrl+S"></TextView>
    </TableRow>
    <TableRow android:paddingLeft="16dp">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="Save as..."></TextView>

        <TextView android:text="Ctrl+Shift+S"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"></TextView>
    </TableRow>
    <View  android:layout_height="2px"
        android:layout_width="match_parent"
        android:background="#7B68EE"
        />
    <TableRow>

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="X import..."></TextView>
    </TableRow>

    <TableRow >

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="X Export"></TextView>

        <TextView android:text="Ctrl+E"
            android:layout_width="wrap_content"
            android:gravity="right"
            android:layout_height="wrap_content"></TextView>
    </TableRow>
    <View  android:layout_height="2px"
        android:layout_width="match_parent"
        android:background="#7B68EE"
        />
    <TableRow android:paddingLeft="16dp">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="Quit"></TextView>
    </TableRow>
</TableLayout>

```

![](https://i.loli.net/2019/03/13/5c8898bdb381e.png)



