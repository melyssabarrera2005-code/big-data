<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>HydraLife | Bebidas Hidratantes Naturales</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:'Poppins', sans-serif;
    background:#f4f9fb;
    color:#333;
}

/* NAV */
nav{
    position:fixed;
    width:100%;
    background:rgba(0,0,0,0.8);
    padding:15px 8%;
    display:flex;
    justify-content:space-between;
    align-items:center;
    z-index:1000;
}

nav h2{
    color:#00f5d4;
    font-weight:700;
}

nav a{
    color:white;
    text-decoration:none;
    margin-left:20px;
    transition:0.3s;
}

nav a:hover{
    color:#00f5d4;
}

/* HERO */
.hero{
    height:100vh;
    background:url('https://images.unsplash.com/photo-1551024601-bec78aea704b?auto=format&fit=crop&w=1600&q=80') no-repeat center center/cover;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
    color:white;
    padding:0 8%;
}

.hero-overlay{
    background:rgba(0,0,0,0.65);
    padding:50px;
    border-radius:20px;
    animation:fadeIn 1.5s ease-in-out;
}

.hero h1{
    font-size:3rem;
    margin-bottom:20px;
}

.hero p{
    font-size:1.2rem;
    margin-bottom:30px;
}

.btn{
    background:#00f5d4;
    padding:14px 30px;
    color:#000;
    border-radius:40px;
    text-decoration:none;
    font-weight:600;
    transition:0.3s;
}

.btn:hover{
    background:#02c39a;
    color:white;
}

/* SECTIONS */
section{
    padding:90px 8%;
    text-align:center;
}

section h2{
    font-size:2.2rem;
    margin-bottom:20px;
}

/* CARDS */
.cards{
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(280px,1fr));
    gap:30px;
    margin-top:40px;
}

.card{
    background:white;
    border-radius:20px;
    overflow:hidden;
    box-shadow:0 15px 35px rgba(0,0,0,0.1);
    transition:0.4s;
}

.card:hover{
    transform:translateY(-12px);
}

.card img{
    width:100%;
    height:250px;
    object-fit:cover;
}

.card h3{
    margin:20px 0 10px;
}

.card p{
    padding:0 20px 25px;
}

/* FORM */
.cta{
    background:linear-gradient(135deg,#00f5d4,#02c39a);
    color:#000;
    border-radius:30px;
}

form{
    margin-top:30px;
}

input{
    display:block;
    width:100%;
    max-width:400px;
    margin:10px auto;
    padding:14px;
    border-radius:30px;
    border:none;
    outline:none;
}

button{
    padding:14px 30px;
    border:none;
    border-radius:30px;
    background:#000;
    color:white;
    cursor:pointer;
    font-weight:600;
    transition:0.3s;
}

button:hover{
    background:#222;
}

/* FOOTER */
footer{
    background:#111;
    color:white;
    padding:20px;
    text-align:center;
}

/* ANIMATION */
@keyframes fadeIn{
    from{opacity:0; transform:translateY(20px);}
    to{opacity:1; transform:translateY(0);}
}

/* RESPONSIVE */
@media(max-width:768px){
    .hero h1{
        font-size:2rem;
    }
}
</style>
</head>

<body>

<nav>
    <h2>HydraLife</h2>
    <div>
        <a href="#beneficios">Beneficios</a>
        <a href="#contacto">Contacto</a>
    </div>
</nav>

<section class="hero">
    <div class="hero-overlay">
        <h1>La Nueva Generación de Hidratación</h1>
        <p>Bebidas naturales con electrolitos y energía real para tu rendimiento diario.</p>
        <a href="#contacto" class="btn">Quiero Información</a>
    </div>
</section>

<section id="beneficios">
    <h2>Beneficios Principales</h2>
    <div class="cards">
        <div class="card">
            <img src="https://images.unsplash.com/photo-1510627498534-cf7e9002facc?auto=format&fit=crop&w=1200&q=80">
            <h3>100% Natural</h3>
            <p>Ingredientes frescos sin conservantes artificiales.</p>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1505575967458-6bdb6f7f18bb?auto=format&fit=crop&w=1200&q=80">
            <h3>Electrolitos Activos</h3>
            <p>Rehidrata y mejora tu recuperación física.</p>
        </div>
        <div class="card">
            <img src="https://images.unsplash.com/photo-1571003121915-cbb859a53f28?auto=format&fit=crop&w=1200&q=80">
            <h3>Sabores Premium</h3>
            <p>Mango tropical, limón fresco y coco natural.</p>
        </div>
    </div>
</section>

<section id="contacto" class="cta">
    <h2>Solicita Información</h2>
    <p>Déjanos tus datos y te escribiremos inmediatamente.</p>

    <form onsubmit="enviarWhatsApp(); return false;">
        <input type="text" id="nombre" placeholder="Tu Nombre" required>
        <input type="email" id="email" placeholder="Tu Email" required>
        <input type="tel" id="telefono" placeholder="Tu Teléfono" required>
        <button type="submit">Enviar por WhatsApp</button>
    </form>
</section>

<footer>
    © 2026 HydraLife | Todos los derechos reservados
</footer>

<script>
function enviarWhatsApp(){
    var nombre = document.getElementById("nombre").value;
    var email = document.getElementById("email").value;
    var telefono = document.getElementById("telefono").value;

    var mensaje = "Hola, quiero información sobre HydraLife:%0A%0A" +
                  "Nombre: " + nombre + "%0A" +
                  "Email: " + email + "%0A" +
                  "Teléfono: " + telefono;

    var url = "https://wa.me/593980293363?text=" + mensaje;

    window.open(url, "_blank");
}
</script>

</body>
</html>
