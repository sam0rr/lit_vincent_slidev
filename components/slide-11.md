---
---

# Cas Concret : Le DCA Intelligent

<div class="grid grid-cols-2 gap-8">
  <div>
    <p><b>Le besoin :</b> Alice veut acheter 50$ de BTC chaque semaine, mais uniquement si l'indicateur de marché (RSI) est inférieur à 30.</p>
    <ul class="fragment">
      <li><b>Bot classique</b>: Risqué, Alice doit lui donner sa clé API ou sa clé privée.</li>
      <li><b>Smart Contract</b>: Limité, ne peut pas accéder aux données de marché off-chain comme le RSI.</li>
      <li><b>Avec Vincent</b>:
        <ul class="fragment">
          <li>L'<b>Ability</b> sait comment acheter du BTC.</li>
          <li>La <b>Policy</b> vérifie le montant (50$) et utilise une Lit Action pour lire le RSI via une API.</li>
          <li>L'agent exécute l'ordre de manière <b>autonome et sécurisée</b>.</li>
        </ul>
      </li>
    </ul>
  </div>
  <div>
    <img src="/assets/images/slide11.png" class="rounded-lg shadow-lg" />
  </div>
</div>
