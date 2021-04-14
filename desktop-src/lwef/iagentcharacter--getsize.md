---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311596"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter :: est à obtenir

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Récupère la taille du frame d’animation du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Adresse d’une variable qui reçoit la largeur du cadre d’animation de caractères en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Adresse d’une variable qui reçoit la hauteur du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: configure**](iagentcharacter--setsize.md)


 

 




