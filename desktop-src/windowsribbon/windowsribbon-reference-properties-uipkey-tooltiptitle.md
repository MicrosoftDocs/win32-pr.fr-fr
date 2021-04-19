---
title: UI_PKEY_TooltipTitle
description: Identifie la propriété TooltipTitle de l’interface utilisateur \_ \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513684"
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

## <a name="remarks"></a>Notes

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

 

 




