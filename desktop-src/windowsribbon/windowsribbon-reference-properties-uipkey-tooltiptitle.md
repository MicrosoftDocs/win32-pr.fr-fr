---
title: UI_PKEY_TooltipTitle
description: Identifie la propriété TooltipTitle de l’interface utilisateur \_ \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6a9e479d2f963acd4041d23e2b1ca075db609f9d45b556cd2aab34e6b2c6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437784"
---
# <a name="ui_pkey_tooltiptitle"></a>IU \_ \_ TooltipTitle

Identifie la propriété TooltipTitle de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ TooltipTitle est utilisée par une application pour interroger l’info-bulle des onglets, des groupes, des boutons, des éléments de la Galerie et d’autres contrôles du ruban.

La valeur de la propriété est une chaîne limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.

> [!Note]  
> Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.

 

L’alignement à droite n’est pas pris en charge.

La longueur maximale de l’interface utilisateur \_ \_ TooltipTitle est illimitée.

Pour afficher une esperluette dans une info-bulle, échappez la désignation de caractères spéciaux par une double esperluette ( `&&` ), comme illustré dans l’exemple suivant.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la ressource](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Commande. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[IU \_ \_ TooltipDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




