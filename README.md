<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro de Usuario</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
        input { margin: 10px; padding: 10px; }
    </style>
</head>
<body>
    <h1>Registro de Usuario</h1>
    <form id="registroForm">
        <input type="text" id="username" placeholder="Nombre de Usuario" required>
        <input type="email" id="email" placeholder="Correo Electrónico" required>
        <div>
            <input type="text" id="password" placeholder="Contraseña" required> <!-- Cambiado a type="text" -->
        </div>
        <button type="submit">Registrar</button>
    </form>
    <h2>Registros</h2>
    <ul id="registros"></ul>
    <script>
        const form = document.getElementById('registroForm');
        const registrosList = document.getElementById('registros');
        form.addEventListener('submit', function(event) {
            event.preventDefault();
            const username = document.getElementById('username').value;
            const email = document.getElementById('email').value;
            const password = document.getElementById('password').value;
            // Aquí puedes hacer una llamada a tu backend para guardar los datos
            // Solo para mostrar los datos en la lista
            const li = document.createElement('li');
            li.textContent = `Usuario: ${username}, Email: ${email}, Contraseña: ${password}`; // Muestra la contraseña
            registrosList.appendChild(li);
