# Agent Plan: Lit Protocol & Vincent Presentation

This document outlines the step-by-step plan to create the Slidev presentation based on the research provided in `lit_protocol_plan.md`.

## Project Setup

*   **Framework**: Slidev
*   **Theme**: `slidev-theme-the-unnamed`
*   **Content Source**: `lit_protocol_plan.md`
*   **Assets**: Images located in `assets/images/`

## Implementation To-Do List

1.  [ ] Clear the boilerplate content from `slides.md`.
2.  [ ] Implement Slide 1: Title and Vision.
3.  [ ] Implement Slide 2: The Current Impasse.
4.  [ ] Implement Slide 3: The Paradigm Shift.
5.  [ ] Implement Slide 4: Lit Protocol - Key Management Infrastructure.
6.  [ ] Implement Slide 5: The Secret of MPC.
7.  [ ] Implement Slide 6: The Hardware Fortress (TEE).
8.  [ ] Implement Slide 7: Lit Actions - Network Intelligence.
9.  [ ] Implement Slide 8: Introduction to the Vincent Framework.
10. [ ] Implement Slide 9: The Three Pillars of Vincent.
11. [ ] Implement Slide 10: The Delegation Workflow.
12. [ ] Implement Slide 11: Concrete Use Case - Smart DCA.
13. [ ] Implement Slide 12: The Cross-Chain Agent.
14. [ ] Implement Slide 13: Summary of Advantages.
15. [ ] Implement Slide 14: Towards the Agent Economy.
16. [ ] Implement Slide 15: Q&A and Resources.
17. [ ] Review the entire presentation for consistency and correctness.

---

## Slide-by-Slide Implementation Details

This section details the markdown, layout, and assets for each slide.

### Slide 1: Titre et Vision

*   **Content**: Title "Au-delà de la Clé Privée : L'Ère des Agents Autonomes Sécurisés" and hook.
*   **Layout**: `cover` from the theme.
*   **Image**: `assets/images/slide1.png` as the background.
*   **Implementation**:
    ```markdown
    ---
    layout: cover
    background: /assets/images/slide1.png
    ---

    # Au-delà de la Clé Privée : L'Ère des Agents Autonomes Sécurisés

    <div class="abs-br m-6 flex gap-2">
      Comment donner à une IA le pouvoir d'agir sur la blockchain sans lui donner les clés de votre coffre-fort?
    </div>
    ```

### Slide 2: L'Impasse Actuelle (Le Mur de la Custody)

*   **Content**: The trilemma: Security vs. Autonomy vs. Convenience.
*   **Layout**: `default` with two columns created manually.
*   **Image**: `assets/images/slide2.png`.
*   **Implementation**:
    ```markdown
    ---
    layout: default
    ---

    # L'Impasse Actuelle : Le Mur de la Custody

    <div class="grid grid-cols-2 gap-8">
      <div>
        <p>Le modèle "Not your keys, not your crypto" freine l'innovation de l'IA et de l'automatisation.</p>
        <p>Un utilisateur fait face à un choix inacceptable :</p>
        <ul>
          <li class="fragment"><b>Risque Total (Custody)</b>: Donner sa clé privée à un bot.</li>
          <li class="fragment"><b>Friction Totale (Manuel)</b>: Devoir signer chaque transaction.</li>
        </ul>
        <p class="fragment">C'est le trilemme : <b>Sécurité</b> vs <b>Autonomie</b> vs <b>Facilité</b>.</p>
      </div>
      <div>
        <img src="/assets/images/slide2.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 3: Le Changement de Paradigme

*   **Content**: Transition from static key to programmable code. Introduce Lit Protocol.
*   **Layout**: `default`.
*   **Image**: `assets/images/slide3.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # Le Changement de Paradigme

    <div class="grid grid-cols-2 gap-8">
      <div>
        <p>La solution n'est pas une meilleure gestion des clés, mais une redéfinition de la clé privée.</p>
        <p class="fragment">Passer de :</p>
        <p class="fragment">"Qui possède la clé ?"</p>
        <p class="fragment">à</p>
        <p class="fragment">"Quelles sont les règles d'utilisation de la clé ?"</p>
        <br/>
        <p class="fragment">C'est la mission de <b>Lit Protocol</b> : créer un réseau où les clés peuvent être invoquées par du code sous des conditions strictes.</p>
      </div>
      <div>
        <img src="/assets/images/slide3.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 4: Lit Protocol - Infrastructure de Gestion de Clés

*   **Content**: Simple definition of Lit Protocol as a key management network.
*   **Layout**: `section`.
*   **Image**: `assets/images/slide4.png` as background.
*   **Implementation**:
    ```markdown
    ---
    layout: section
    background: /assets/images/slide4.png
    ---

    # Lit Protocol
    ### Une infrastructure pour la gestion de clés programmables.
    ```

### Slide 5: Le Secret du MPC (Multi-Party Computation)

*   **Content**: Analogy of the "Torn Treasure Map", Threshold Cryptography (2/3), No Single Point of Failure.
*   **Layout**: `default`.
*   **Image**: `assets/images/slide5.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # Le Secret : Multi-Party Computation (MPC)

    <div class="grid grid-cols-2 gap-8">
      <div>
        <p>La clé privée est divisée en fragments distribués sur le réseau. C'est la <b>Cryptographie à Seuil</b>.</p>
        <ul class="fragment">
            <li>Analogie : Une carte au trésor déchirée en plusieurs morceaux.</li>
            <li>La clé privée complète n'est <b>jamais</b> assemblée.</li>
            <li>Il faut un seuil (ex: 2/3 des noeuds) pour approuver une signature.</li>
        </ul>
        <p class="fragment">Bénéfice principal : <b>Pas de Point de Défaillance Unique (No Single Point of Failure)</b>.</p>
      </div>
      <div>
          <img src="/assets/images/slide5.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 6: La Forteresse Matérielle (TEE)

*   **Content**: Hardware isolation (Intel SGX), "Défense en Profondeur" (MPC + TEE).
*   **Layout**: `default`.
*   **Image**: `assets/images/slide6.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # La Forteresse : Environnements d'Exécution de Confiance (TEE)

    <div class="grid grid-cols-2 gap-8">
      <div>
        <p>Chaque noeud du réseau Lit exécute son code dans une enclave matérielle sécurisée (TEE).</p>
        <ul class="fragment">
          <li>C'est une "boîte noire" au sein du processeur.</li>
          <li>Même l'opérateur du serveur ne peut pas accéder aux fragments de clé.</li>
        </ul>
        <h3 class="fragment">"Défense en Profondeur"</h3>
        <p class="fragment">La combinaison <b>MPC + TEE</b> offre une sécurité maximale et une vitesse accrue, en exigeant à un attaquant de briser deux barrières radicalement différentes.</p>
      </div>
      <div>
        <img src="/assets/images/slide6.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 7: Lit Actions - L'Intelligence du Réseau

*   **Content**: "Programmable Signing", ability to read the web (HTTP Fetch).
*   **Layout**: `default`.
*   **Image**: `assets/images/slide7.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # L'Intelligence : Lit Actions

    <div class="grid grid-cols-2 gap-8">
      <div>
        <p>Les <b>Lit Actions</b> sont des scripts JavaScript qui agissent comme des gardiens logiques pour les clés.</p>
        <p class="fragment">Le code décide si une signature doit être effectuée : "Signature Programmable".</p>
        <br/>
        <h3 class="fragment">Capacité unique : Accès au Web</h3>
        <p class="fragment">Une Lit Action peut faire des requêtes HTTP (`fetch`) pour conditionner une signature à des données du monde réel.</p>
        <p class="fragment">Exemple : <i>"Signer la transaction uniquement si le prix de l'ETH est supérieur à 3000$ sur l'API de Coinbase."</i></p>
      </div>
      <div>
        <img src="/assets/images/slide7.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 8: Introduction au Framework Vincent

*   **Content**: Transition "Lit is the engine, Vincent is the vehicle".
*   **Layout**: `section`.
*   **Image**: `assets/images/slide8.png` as background.
*   **Implementation**:
    ```markdown
    ---
    layout: section
    background: /assets/images/slide8.png
    ---

    # Le Framework Vincent
    ### "Lit est le moteur, Vincent est le véhicule."
    ```

### Slide 9: Les Trois Piliers de Vincent

*   **Content**: Diagram: Abilities (Tools) <-> Policies (Rules) <-> Agent (Executor).
*   **Layout**: `default`.
*   **Image**: `assets/images/slide9.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # Les Trois Piliers de Vincent

    <div class="grid grid-cols-2 gap-8">
      <div>
        <p>Vincent est un standard pour créer des agents autonomes et sécurisés. Il repose sur 3 piliers :</p>
        <ul>
          <li class="fragment"><b>Abilities (Capacités)</b>: Ce que l'agent <i>sait</i> faire.
            <ul><li>Ex: "Savoir comment faire un Swap sur Uniswap".</li></ul>
          </li>
          <li class="fragment"><b>Policies (Politiques)</b>: Ce que l'agent a le <i>droit</i> de faire.
            <ul><li>Ex: "Ne pas dépenser plus de 100$ par jour."</li></ul>
          </li>
          <li class="fragment"><b>Agent Wallet (Portefeuille)</b>: L'identité de l'agent, contrôlée par les politiques.</li>
        </ul>
      </div>
      <div>
        <img src="/assets/images/slide9.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 10: Le Workflow de Délégation (Visualisation)

*   **Content**: Animated workflow of a transaction via Vincent.
*   **Layout**: `default`.
*   **Image**: `assets/images/slide10.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # Le Workflow de Délégation

    <div class="grid grid-cols-2 gap-8">
      <div>
        <ol>
          <li class="fragment"><b>Initialisation</b>: L'utilisateur connecte son portefeuille et configure un agent avec des politiques.</li>
          <li class="fragment"><b>Délégation</b>: L'utilisateur signe un message qui autorise l'agent.</li>
          <li class="fragment"><b>Proposition</b>: L'agent détecte une opportunité et propose une transaction au réseau Lit.</li>
          <li class="fragment"><b>Vérification</b>: Les noeuds Lit exécutent la Lit Action qui vérifie la politique.</li>
          <li class="fragment"><b>Signature</b>: Si la politique est respectée, les noeuds signent la transaction.</li>
          <li class="fragment"><b>Exécution</b>: L'agent diffuse la transaction signée sur la blockchain.</li>
        </ol>
        <p class="fragment">L'utilisateur garde le contrôle ultime et peut révoquer l'accès à tout moment.</p>
      </div>
      <div>
        <img src="/assets/images/slide10.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 11: Cas Concret - Le DCA Intelligent

*   **Content**: Story of Alice buying BTC based on RSI.
*   **Layout**: `default`.
*   **Image**: `assets/images/slide11.png`.
*   **Implementation**:
    ```markdown
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
    ```

### Slide 12: L'Agent Cross-Chain

*   **Content**: An agent managing assets on Ethereum and Solana with a single identity.
*   **Layout**: `default`.
*   **Image**: `assets/images/slide12.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # L'Agent Cross-Chain

    <div class="grid grid-cols-2 gap-8">
      <div>
        <p>Une seule identité programmable (PKP) peut contrôler des adresses sur plusieurs blockchains (Ethereum, Solana, Bitcoin...).</p>
        <p class="fragment">Un agent peut orchestrer des stratégies complexes :</p>
        <ol class="fragment">
          <li>Prendre des profits sur un protocole DeFi sur <b>Ethereum</b>.</li>
          <li>Utiliser un service de messagerie pour transférer la valeur.</li>
          <li>Acheter un NFT sur <b>Solana</b>.</li>
        </ol>
        <p class="fragment">Ceci élimine le besoin de bridges risqués et met fin à la fragmentation de l'identité numérique.</p>
      </div>
      <div>
        <img src="/assets/images/slide12.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 13: Résumé des Avantages

*   **Content**: Summary table of Security / Flexibility / UX.
*   **Layout**: `default`.
*   **Image**: `assets/images/slide13.png`.
*   **Implementation**:
    ```markdown
    ---
    ---

    # Résumé des Avantages

    <div class="grid grid-cols-2 gap-8">
      <div>
        <ul>
          <li><b class="text-green-500">Sécurité</b>: Plus de clé privée unique exposée. Défense en profondeur (MPC+TEE).</li>
          <li><b class="text-blue-500">Souveraineté</b>: L'utilisateur garde le contrôle via des politiques révocables. Pas de custody.</li>
          <li><b class="text-yellow-500">Flexibilité</b>: Logique programmable et accès aux données du monde réel.</li>
          <li><b class="text-purple-500">Interopérabilité</b>: Agnostique à la blockchain. Une identité pour les gouverner toutes.</li>
          <li><b class="text-red-500">UX Améliorée</b>: Permet une automatisation complexe sans sacrifier la sécurité, ouvrant la voie à des applications Web3 grand public.</li>
        </ul>
      </div>
      <div>
        <img src="/assets/images/slide13.png" class="rounded-lg shadow-lg" />
      </div>
    </div>
    ```

### Slide 14: Vers l'Économie des Agents

*   **Content**: Vision of a future with personal "Digital Employees".
*   **Layout**: `center`.
*   **Image**: `how_it_works.png` (reusing an existing related image).
*   **Implementation**:
    ```markdown
    ---
    layout: center
    background: /assets/images/how_it_works.png
    ---

    # Vers l'Économie des Agents

    Un futur où nous avons tous des "Employés Numériques" personnels qui gèrent nos actifs digitaux de manière autonome, sécurisée et souveraine.
    ```

### Slide 15: Q&A et Ressources

*   **Content**: Call to action, links to docs, GitHub.
*   **Layout**: `center`.
*   **Implementation**:
    ```markdown
    ---
    layout: center
    ---

    # Questions & Ressources

    **Merci !**

    <br/>

    - **Documentation Lit Protocol**: [developer.litprotocol.com](https://developer.litprotocol.com)
    - **Framework Vincent**: [GitHub](https://github.com/LIT-Protocol/Vincent)
    - **Blog & Cas d'usage**: [spark.litprotocol.com](https://spark.litprotocol.com)

    ```
