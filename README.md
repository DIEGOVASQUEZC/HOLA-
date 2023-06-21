<!DOCTYPE html>
<html>
<head>
  <title>Carta para Paola</title>
  <style>
    .emoji {
      font-size: 30px;
    }
    .hidden {
      display: none;
    }
  </style>
</head>
<body>
  <h1>Carta para Paola</h1>
  <div id="carta">
    <p>Querida Paola,</p>
    <p>Espero que esta carta te encuentre bien. Me siento emocionado mientras escribo estas palabras, ya que hay algo importante que quiero compartir contigo.</p>
    <p>Desde que nos separamos, he reflexionado mucho sobre nuestro tiempo juntos y lo que significas para mí. Me he dado cuenta de cuánto te extraño y cómo mi vida no es la misma sin ti. Los momentos que compartimos fueron verdaderamente especiales y valiosos para mí, y desearía poder revivirlos una vez más.</p>
    <p>Paola, no puedo negar lo mucho que te amo. Eres una persona única y maravillosa, con quien he compartido risas, alegrías y también momentos difíciles. Me has enseñado lecciones importantes sobre el amor y la conexión, y estoy agradecido por cada instante que hemos compartido.</p>
    <p>Antes de continuar, quiero aprovechar esta oportunidad para disculparme sinceramente por todos mis errores y por cualquier daño que te haya causado. Reconozco que cometí errores y que puedo haber lastimado tus sentimientos en el pasado. Lamento profundamente cualquier dolor que haya experimentado a causa de mis acciones o palabras.</p>
    <button id="continuarBtn">CONTINUAR</button>
  </div>

  <div id="pregunta" class="hidden">
    <h2>¿Quieres regresar conmigo?</h2>
    <form>
      <input type="radio" name="respuesta" value="si"> Sí<br>
      <input type="radio" name="respuesta" value="no"> No<br>
      <br>
      <input type="submit" value="Enviar">
    </form>
    <div id="emojiResultado" class="emoji"></div>
  </div>

  <script>
    const carta = document.getElementById('carta');
    const continuarBtn = document.getElementById('continuarBtn');
    const pregunta = document.getElementById('pregunta');
    const form = document.querySelector('form');
    const emojiResultado = document.getElementById('emojiResultado');

    continuarBtn.addEventListener('click', function() {
      carta.classList.add('hidden');
      pregunta.classList.remove('hidden');
    });

    form.addEventListener('submit', function(e) {
      e.preventDefault();
      const respuesta = document.querySelector('input[name="respuesta"]:checked').value;

      if (respuesta === 'si') {
        emojiResultado.textContent = '😊';
      } else if (respuesta === 'no') {
        emojiResultado.textContent = '😢';
      }
    });
  </script>
</body>
</html>
