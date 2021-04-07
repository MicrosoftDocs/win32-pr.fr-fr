---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029026"
---
# <a name="iagentcharacterexgetoriginalsize"></a>IAgentCharacterEx::GetOriginalSize

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Récupère la taille d’origine du frame d’animation du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Adresse d’une variable qui reçoit la largeur d’origine du cadre d’animation de caractères en pixels.

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Adresse d’une variable qui reçoit la hauteur d’origine du cadre d’animation de caractères en pixels.

</dd> </dl>

Cet appel retourne la taille d’origine de la trame de caractères telle qu’elle est créée dans l’éditeur de caractères Microsoft Agent.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: est à obtenir**](iagentcharacter--getsize.md)


 

 




