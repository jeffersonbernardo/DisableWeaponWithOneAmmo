# 📌 DisableWeaponWithOneAmmo

Este script é ideal para servidores SA-MP que utilizam sistemas onde armas e munições são gerenciadas separadamente. Ele não apenas evita que armas desapareçam da mão do jogador por falta de munição, mas também garante que jogadores não possam causar dano a outros quando estiverem com apenas uma bala restante, promovendo uma jogabilidade mais justa.

---

#### ⚙️ Funcionamento

- **Sem YSF:** O script utiliza um loop que percorre os 10 slots de armas do jogador para encontrar a arma correspondente e verificar sua munição.
- **Com YSF:** O script usa a função `GetWeaponSlot` para buscar diretamente o slot da arma e verificar a munição restante.
- **Reabastecimento de munição:** Se o jogador tiver apenas 1 bala restante, o código:
  - Reabastece a arma com 1 bala.
  - Define a arma ativa como desarmada (`SetPlayerArmedWeapon(playerid, 0)`).

---

#### 💡 Observação

Você pode modificar o código para personalizar o comportamento de reabastecimento de munição ou adicionar novas funcionalidades. Certifique-se de seguir as orientações do seu servidor e garantir que o código esteja em conformidade com as políticas de jogabilidade.
