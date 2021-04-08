---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840362"
---
# <a name="iagentcharacterexshowpopupmenu"></a>IAgentCharacterEx::ShowPopupMenu

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

Affiche le menu contextuel du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée x du menu contextuel du caractère, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée y du menu contextuel du caractère, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

Lorsque vous affectez à [**IAgentCharacterEx :: SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) la **valeur false**, le serveur n’affiche plus automatiquement le menu lorsque vous cliquez avec le bouton droit sur le caractère ou sur son icône de barre des tâches. Vous pouvez utiliser cette méthode pour afficher le menu.

Le menu s’affiche jusqu’à ce que l’utilisateur sélectionne une commande ou affiche un autre menu. Un seul menu contextuel peut être affiché à la fois ; par conséquent, les appels à cette méthode annulent (supprime) le menu précédent.

Cette méthode ne doit être appelée que lorsque votre application cliente est le client actif du caractère ; dans le cas contraire, elle échoue.

[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)

 

 




