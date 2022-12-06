# myLogin


Preparamos nuestro proyecto

Al archivo AndroidManifest.xml
````
    <uses-permission android:name="android.permission.INTERNET"></uses-permission>
````

Al archivo buiild.gradle.app
````
    viewBinding {
        enabled = true
    }
````

En nuestro fragmento declarar el objeto Bindig y actualizamos los métodos onCreateView y onDestroyView
````
public class LoginFragment extends Fragment {
    FragmentLoginBinding binding;
    
    ...
    
    @Override
    public View onCreateView(LayoutInflater inflater, ViewGroup container,
                             Bundle savedInstanceState) {
        // Inflate the layout for this fragment
        // return inflater.inflate(R.layout.fragment_login, container, false);
        binding = FragmentLoginBinding.inflate(inflater, container, false);
        View view = binding.getRoot();
        return view;
    }

    @Override
    public void onDestroyView() {
        super.onDestroyView();
        binding = null;
    }    
    
    
````


Conectamos nuestra aplicación a FireBase

![](https://github.com/caamaledgar/documentationProjects/blob/main/Login/Firebase%20Auth%20Provider.PNG)

![](https://github.com/caamaledgar/documentationProjects/blob/main/Login/Firebase%20Auth%20Connect.PNG)


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
    
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        android:layout_margin="20dp">
        <Button
            android:id="@+id/btnLoginGoogle"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            style="@style/Widget.MaterialComponents.Button.TextButton"
            android:drawableLeft="@drawable/googleg_standard_color_18"
            android:text="Ingresar con Google" />
    </LinearLayout>
    
````

![](https://github.com/caamaledgar/documentationProjects/blob/main/Login/Login.PNG)




