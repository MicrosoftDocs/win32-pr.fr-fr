---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55abb64a8466b13ee41119e2a8a359ceeb182c92f7b4d2b1071547df07110052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750517"
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


 

 




