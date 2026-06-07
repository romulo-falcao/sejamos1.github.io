---
title: "Pedido de Oração"
description: "Deixe seu pedido de oração anonimamente. Você não está sozinho."
---

Se você está passando por um momento difícil — ou conhece alguém que está — você pode deixar um pedido de oração aqui. Não precisa se identificar. Não precisa explicar tudo.

**Você não está sozinho.**

<form id="prayer-form" action="https://formspree.io/f/xeewaezr" method="POST" class="mt-8 max-w-lg mx-auto">
  <div class="mb-5">
    <label for="name" class="block text-sm font-medium text-neutral-700 dark:text-neutral-300 mb-1">
      Seu nome (opcional)
    </label>
    <input type="text" id="name" name="name" placeholder="Anônimo" class="w-full rounded-xl border border-neutral-300 dark:border-neutral-600 bg-white dark:bg-neutral-800 px-4 py-3 text-neutral-900 dark:text-neutral-100 focus:outline-none focus:ring-2 focus:ring-primary-500">
  </div>

  <div class="mb-5">
    <label for="prayer" class="block text-sm font-medium text-neutral-700 dark:text-neutral-300 mb-1">
      Seu pedido de oração
    </label>
    <textarea id="prayer" name="prayer" rows="5" required placeholder="Escreva aqui o que está no seu coração..." class="w-full rounded-xl border border-neutral-300 dark:border-neutral-600 bg-white dark:bg-neutral-800 px-4 py-3 text-neutral-900 dark:text-neutral-100 focus:outline-none focus:ring-2 focus:ring-primary-500"></textarea>
  </div>

  <button type="submit" class="w-full py-3 px-6 bg-primary-500 hover:bg-primary-600 text-white font-semibold rounded-xl transition-colors">
    Enviar pedido de oração
  </button>

  <p class="text-xs text-neutral-400 dark:text-neutral-500 text-center mt-4">
    Seu pedido é anônimo e será lido com respeito.
  </p>
</form>

<div id="prayer-success" class="hidden mt-8 text-center p-8 rounded-2xl bg-primary-50 dark:bg-primary-900/20 border border-primary-200 dark:border-primary-800">
  <p class="text-xl font-semibold text-neutral-800 dark:text-neutral-100 mb-2">🙏 Recebido</p>
  <p class="text-neutral-600 dark:text-neutral-400">
    Seu pedido de oração foi recebido. Você não está sozinho.
  </p>
</div>

<script>
  document.getElementById('prayer-form').addEventListener('submit', function(e) {
    e.preventDefault();
    var form = this;
    var data = new FormData(form);
    fetch(form.action, { method: 'POST', body: data, headers: { 'Accept': 'application/json' } })
      .then(function(res) {
        if (res.ok) {
          form.classList.add('hidden');
          document.getElementById('prayer-success').classList.remove('hidden');
        } else {
          alert('Erro ao enviar. Tente novamente ou me mande uma mensagem no WhatsApp.');
        }
      })
      .catch(function() {
        alert('Erro de conexão. Tente novamente ou me mande uma mensagem no WhatsApp.');
      });
  });
</script>

> "Clama a mim, e responder-te-ei, e anunciar-te-ei coisas grandes e ocultas, que não sabes." — Jeremias 33:3
