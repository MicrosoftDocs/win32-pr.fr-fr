---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089226f98969594a1d19afc7f3bb529c30943e06ec4083364dc5ae2f9850c9c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848519"
---
# <a name="iagentcharactersetsize"></a>IAgentCharacter :: configure

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

Définit la taille du cadre d’animation du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

Largeur, en pixels, du cadre d’animation du caractère.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

Hauteur, en pixels, du cadre d’animation du caractère.

</dd> </dl>

La modification de la taille du cadre du caractère met à l’échelle le caractère sur la taille définie avec cette méthode. Le paramètre de cette propriété s’applique à tous les clients du caractère.

Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur son cadre d’animation rectangulaire.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: est à obtenir**](iagentcharacter--getsize.md)


 

 




