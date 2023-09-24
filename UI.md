# 修改ui
- 主ui目录:/res/layout-v21/toolbox_overlay.xml

### 主ui代码注释
```xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:theme="@7F110009"
    android:layout_width="-1"
    android:layout_height="-1">
    <!-- 左边功能分类栏 -->
    <androidx.recyclerview.widget.RecyclerView
        android:id="@7F090057"
        android:background="#80000000"
        android:paddingTop="8dp"
        android:paddingBottom="8dp"
        android:clipToPadding="false"
        android:layout_width="186dp"
        android:layout_height="-1"
        android:layout_alignParentStart="true"
        android:elevation="12dp" />
    <!-- 右边功能栏 -->
    <androidx.recyclerview.widget.RecyclerView
        android:id="@7F090103"
        android:background="#80000000"
        android:paddingTop="8dp"
        android:paddingBottom="8dp"
        android:clipToPadding="false"
        android:layout_width="240dp"
        android:layout_height="-1"
        android:layout_alignParentEnd="true"
        android:elevation="12dp" />
    <!-- 上面剩余时间栏 -->
    <FrameLayout
        android:layout_width="-1"
        android:layout_height="-1"
        android:layout_toStartOf="@7F090103"
        android:layout_toEndOf="@7F090057">
        <TextView
            android:textAppearance="@7F11012E"
            android:gravity="0x00000011"
            android:layout_gravity="0x00000031"
            android:id="@7F09011D"
            android:background="@7F08011F"
            android:layout_width="-2"
            android:layout_height="-2"
            android:layout_marginTop="16dp"
            android:drawablePadding="8dp"
            android:drawableEnd="@7F080122"
            android:paddingStart="16dp"
            android:paddingEnd="16dp" />
        <!-- 底部三个图标栏 -->
        <LinearLayout
            android:layout_gravity="0x00000051"
            android:layout_width="-2"
            android:layout_height="-2">
            <ImageView
                android:id="@7F090143"
                android:background="@7F08011F"
                android:layout_width="-2"
                android:layout_height="-2"
                android:layout_marginBottom="16dp"
                android:src="@7F0800EF"
                app:tint="#FFFFFFFF" />
            <ImageView
                android:id="@7F0900AC"
                android:background="@7F08011F"
                android:layout_width="-2"
                android:layout_height="-2"
                android:layout_marginBottom="16dp"
                android:src="@7F0800D8"
                app:tint="#FFFFFFFF" />
            <ImageView
                android:id="@7F090089"
                android:background="@7F08011F"
                android:layout_width="-2"
                android:layout_height="-2"
                android:layout_marginBottom="16dp"
                android:src="@7F0800CC"
                app:tint="#FFFFFFFF" />
        </LinearLayout>
    </FrameLayout>
</RelativeLayout>
```

- 如需进一步修改学了<kbd>安卓xml</kbd>自然就会了
