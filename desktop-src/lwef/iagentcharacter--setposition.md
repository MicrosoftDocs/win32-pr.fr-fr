---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028990"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter :: SetPosition

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Définit la position du cadre d’animation du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

Coordonnée d’écran du bord gauche du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

Coordonnée d’écran du bord supérieur du cadre d’animation de caractères, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

Le paramètre de cette propriété s’applique à tous les clients du caractère. Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.

> [!Note]  
> Contrairement à la méthode [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , cette fonction n’est pas mise en file d’attente.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: GetPosition**](iagentcharacter--getposition.md)


 

 




