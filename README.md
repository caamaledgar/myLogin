# myLogin




Creamos nuestro fragmento Login, nuestros campos TextInputLayout añadir las propiedades de tipo email y password
````
   android:inputType="textEmailAddress"
   android:inputType="textPassword"
````

````
    <View
        android:layout_width="match_parent"
        android:layout_height="70dp">
    </View>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/titemail"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"
        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:inputType="textEmailAddress"
            android:hint="Usuario o Correo Electrónico" />
    </com.google.android.material.textfield.TextInputLayout>

    <com.google.android.material.textfield.TextInputLayout
        android:id="@+id/titpassword"
        style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox"

        android:layout_width="match_parent"
        android:layout_height="match_parent">

        <com.google.android.material.textfield.TextInputEditText
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:inputType="textPassword"
            android:hint="Pasword" />
    </com.google.android.material.textfield.TextInputLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:layout_margin="20dp">


        <Button
            android:id="@+id/btnLogin"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:layout_marginRight="10dp"
            android:text="Login" />

        <Button
            android:id="@+id/btnRegistrar"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="Registrar" />
    </LinearLayout>
````

![](https://github.com/caamaledgar/documentationProjects/blob/main/Login/Login.png)
