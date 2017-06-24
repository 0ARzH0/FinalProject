# FinalProject
CRUD administrativo hecho en Laravel
<br>
<h1>Paso 1</h1>
crear la base de datos y darle acceso desde el archivo .env
<br>
<h1>Paso 2</h1>
correr la primera migracion, pero antes modificar el archivo

<h3>Dato</h3>
<ul>
	<li>para corregir el problema de utilizar usuario diferente a root primero se modifica en config/database.php, y tambien en el .env</li>
	<li>para solucionar el problema de los strings se modifica en App\Providers\AppServiceProvider.php</li>
	<code>
	use Illuminate\Support\ServiceProvider;
	use Illuminate\Support\Facades\Schema;

	class AppServiceProvider extends ServiceProvider{
	    /**
	     * Bootstrap any application services.
	     *
	     * @return void
	     */
	    public function boot(){
	        //
	        Schema::defaultStringLength(191);
	    }

	    /**
	     * Register any application services.
	     *
	     * @return void
	     */
	    public function register(){
	        //
	    }
	}</code>
</ul>