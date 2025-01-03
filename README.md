<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>El Secreto de la Navidad en Mendoza</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Comic+Neue:wght@300;700&display=swap');
        body {
            font-family: 'Comic Neue', cursive;
        }
        .page {
            display: none;
        }
        .page.active {
            display: block;
            animation: slide-in 0.5s ease-in-out;
        }
        @keyframes slide-in {
            from { opacity: 0; transform: translateX(100%); }
            to { opacity: 1; transform: translateX(0); }
        }
    </style>
</head>
<body class="bg-green-100 p-4">
    <div class="max-w-2xl mx-auto bg-white p-8 rounded-lg shadow-lg">
        <div id="page-1" class="page active">
            <h1 class="text-3xl font-bold mb-4 text-center">El Secreto de la Navidad en Mendoza</h1>
            <img src="img/cuento1.jpeg" alt="Fran y Luna mirando las estrellas" class="mb-4">
            <p>En una cálida noche de verano en Villa Nueva, Mendoza, Fran y Luna estaban sentados en el patio de su casa, mirando las estrellas...</p>
            <button onclick="nextPage(2)" class="mt-4 px-4 py-2 bg-blue-500 text-white rounded">Siguiente</button>
        </div>
        <div id="page-2" class="page">
            <img src="img/cuento2.jpeg" alt="Destello de luz en el cielo" class="mb-4">
            <p>Justo en ese momento, un destello de luz atravesó el cielo y algo cayó suavemente en el jardín. Se acercaron y encontraron una caja misteriosa...</p>
            <button onclick="prevPage(1)" class="mt-4 px-4 py-2 bg-gray-500 text-white rounded">Anterior</button>
            <button onclick="nextPage(3)" class="mt-4 px-4 py-2 bg-blue-500 text-white rounded">Siguiente</button>
        </div>
        <div id="page-3" class="page">
            <img src="img/cuento3.jpeg" alt="Fran y Luna con duendes de madera" class="mb-4">
            <p>Abrieron la caja y encontraron dos pequeños duendes de madera y un mapa. La nota continuaba: “Sigan el mapa y descubrirán un secreto mágico”...</p>
            <button onclick="prevPage(2)" class="mt-4 px-4 py-2 bg-gray-500 text-white rounded">Anterior</button>
            <button onclick="nextPage(4)" class="mt-4 px-4 py-2 bg-blue-500 text-white rounded">Siguiente</button>
        </div>
        <div id="page-4" class="page">
            <img src="img/cuento4.jpeg" alt="Fran y Luna siguiendo el mapa" class="mb-4">
            <p>Decidieron seguir el mapa que los llevó a través de las calles empedradas del pueblo hasta el bosque cercano...</p>
            <button onclick="prevPage(3)" class="mt-4 px-4 py-2 bg-gray-500 text-white rounded">Anterior</button>
            <button onclick="nextPage(5)" class="mt-4 px-4 py-2 bg-blue-500 text-white rounded">Siguiente</button>
        </div>
        <div id="page-5" class="page">
            <img src="img/cuento5.jpeg" alt="La cabaña iluminada con luces navideñas" class="mb-4">
            <p>Finalmente, llegaron a un claro donde había una cabaña iluminada con luces navideñas. Dentro de la cabaña, se encontraron con un hombre de barba blanca y traje rojo...</p>
            <button onclick="prevPage(4)" class="mt-4 px-4 py-2 bg-gray-500 text-white rounded">Anterior</button>
            <button onclick="nextPage(6)" class="mt-4 px-4 py-2 bg-blue-500 text-white rounded">Siguiente</button>
        </div>
        <div id="page-6" class="page">
            <img src="img/cuento6.jpeg" alt="Papá Noel mostrando cartas y dibujos" class="mb-4">
            <p>Papá Noel les mostró un baúl lleno de cartas y dibujos de niños de todo el mundo, agradeciéndole por los regalos...</p>
            <button onclick="prevPage(5)" class="mt-4 px-4 py-2 bg-gray-500 text-white rounded">Anterior</button>
            <button onclick="nextPage(7)" class="mt-4 px-4 py-2 bg-blue-500 text-white rounded">Siguiente</button>
        </div>
        <div id="page-7" class="page">
            <img src="img/cuento7.jpeg" alt="Fran y Luna abrazando a Papá Noel" class="mb-4">
            <p>Fran y Luna se despidieron con abrazos y volvieron a casa con el corazón lleno de alegría y una nueva comprensión de la magia de la Navidad...</p>
            <button onclick="prevPage(6)" class="mt-4 px-4 py-2 bg-gray-500 text-white rounded">Anterior</button>
            <p class="text-center mt-8">Fin</p>
        </div>
    </div>

    <script>
        function nextPage(page) {
            document.querySelector('.page.active').classList.remove('active');
            document.getElementById('page-' + page).classList.add('active');
        }
        function prevPage(page) {
            document.querySelector('.page.active').classList.remove('active');
            document.getElementById('page-' + page).classList.add('active');
        }
    </script>
</body>
</html>

