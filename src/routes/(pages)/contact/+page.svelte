<h1 class="text-3xl font-bold mb-4">Contacto</h1>
<p class="mb-6">
    ¿Quieres aparecer en el directorio o tienes alguna consulta? ¡Escríbenos!
</p>
<form
    class="bg-base-100 shadow rounded px-8 pt-6 pb-8 mb-4 max-w-md mx-auto space-y-4"
>
    <div>
        <label class="block text-sm font-bold mb-2" for="name"> Nombre </label>
        <input
            class="input input-bordered w-full"
            id="name"
            type="text"
            placeholder="Tu nombre"
            required
        />
    </div>
    <div>
        <label class="block text-sm font-bold mb-2" for="email"> Email </label>
        <input
            class="input input-bordered w-full"
            id="email"
            type="email"
            placeholder="tucorreo@email.com"
            required
        />
    </div>
    <div>
        <label class="block text-sm font-bold mb-2" for="message">
            Mensaje
        </label>
        <textarea
            class="textarea textarea-bordered w-full"
            id="message"
            rows="4"
            placeholder="¿Cómo podemos ayudarte?"
            required
        ></textarea>
    </div>
    <div class="flex items-center justify-end">
        <button class="btn btn-primary" type="submit"> Enviar </button>
    </div>
</form>
