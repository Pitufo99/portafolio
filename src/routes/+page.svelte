<script>
    let proyectos = [
        { nombre: "Lista de Cafes", imagen: "pre-listCafe.png", descripcion: "", url: "https://application-lmxo.vercel.app/" },
        { nombre: "Proyecto 2", imagen: "https://via.placeholder.com/300x200", descripcion: "", url: "https://tu-dominio-vercel.com/proyecto2" },
        { nombre: "Proyecto 2", imagen: "https://via.placeholder.com/300x200", descripcion: "", url: "https://tu-dominio-vercel.com/proyecto2" },
    ];
</script>

<main class="container">
    <h1 class="text-center">Mis Proyectos</h1>
    <div class="projects">
        {#each proyectos as proyecto}
            <div class="project-card">
                <h3>{proyecto.nombre}</h3>
				<img src={proyecto.imagen} alt="Previsualización de {proyecto.nombre}" class="preview-img">
                <p>{proyecto.descripcion}</p>
                <a href={proyecto.url} target="_blank">Ver en Vercel</a>
            </div>
        {/each}
    </div>
</main>

<style>
    .container {
        padding: 50px;
        font-family: Arial, sans-serif;
    }
    .text-center {
        text-align: center;
    }
	.preview-img {
        width: 100%;
        height: auto;
        border-radius: 5px;
        margin-bottom: 15px;
    }
    .projects {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
        margin-top: 20px;
    }
    .project-card {
        padding: 20px;
        background: #f5f5f5;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        text-align: center;
    }
    .project-card a {
        color: #007bff;
        text-decoration: none;
    }
    .project-card a:hover {
        text-decoration: underline;
    }
</style>
