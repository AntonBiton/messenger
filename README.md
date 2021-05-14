Чтобы добавить binding надо дописать:

В	<i>build.gradle(Module...</i>


<pre>android {
    ...........

    buildFeatures{
        viewBinding true
    }
   ..........</pre>
==============================

В	<i>MainActivity.kt</i>

<b>import com.example.messenger.databinding.ActivityMainBinding</b>
<pre>
class MainActivity : AppCompatActivity() {

    <b>private lateinit var binding: ActivityMainBinding</b>

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        <b>binding = ActivityMainBinding.inflate(layoutInflater)
        val view = binding.root</b>
        setContentView(<b>view</b>)
    }
}
</pre>
