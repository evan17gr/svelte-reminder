<script>
import { Router, Route, Link} from "svelte-routing"; 
import Home from "./pages/Home.svelte";
import Categories from "./pages/Categories.svelte";
import Departments from "./pages/Departments.svelte";
import Modifiers from "./pages/Modifiers.svelte";
import PaymentTypes from "./pages/PaymentTypes.svelte";
import Products from "./pages/Products.svelte";
import Rotas from "./pages/Rotas.svelte";
import States from "./pages/States.svelte";
import tLayout from "./pages/tLayout.svelte";
import tNames from "./pages/tNames.svelte";
import Users from "./pages/Users.svelte";

export let url = "";
</script>

<Router url="{url}">
	<nav class="nav">
		<Link class="nav-link" to="/">Home</Link>
		<Link class="nav-link" to="/categories">Categories</Link>
		<Link class="nav-link" to="/departments">Departments</Link>
		<Link class="nav-link" to="/modifiers">Modifiers</Link>
		<Link class="nav-link" to="/paymentTypes">PaymentTypes</Link>
		<Link class="nav-link" to="/products">Products</Link>
		<Link class="nav-link" to="/rotas">Rotas</Link>
		<Link class="nav-link" to="/states">States</Link>
		<Link class="nav-link" to="/tLayout">TLayout</Link>
		<Link class="nav-link" to="/tNames">TNames</Link>
		<Link class="nav-link" to="/users">Users</Link>
	</nav>
	<Route path="/" component={Home}/>
	<Route path="/categories" component={Categories}/>
	<Route path="/departments" component={Departments}/>
	<Route path="/modifiers" component={Modifiers}/>
	<Route path="/paymentTypes" component={PaymentTypes}/>
	<Route path="/products" component={Products}/>
	<Route path="/rotas" component={Rotas}/>
	<Route path="/states" component={States}/>
	<Route path="/tLayout" component={tLayout}/>
	<Route path="/tNames" component={tNames}/>
	<Route path="/users" component={Users}/>
</Router>

<style>
nav{
	display: flex;
	justify-content: center;
	font-size:20px;
}
</style>