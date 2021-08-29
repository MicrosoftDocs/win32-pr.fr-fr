---
title: UI_PKEY_TooltipDescription
description: Identifie la propriété TooltipDescription de l’interface utilisateur \_ \_ .
ms.assetid: 658e798a-f41e-4538-94ac-38a9cb20dd74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2962370c18e1c9b7d072d47d92292182097f9e31f17b45096907b7e6c7f92e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932528"
---
# <a name="ui_pkey_tooltipdescription"></a>IU \_ \_ TooltipDescription

Identifie la propriété TooltipDescription de l’interface utilisateur \_ \_ .

```
propertyDescription
   name = UI_PKEY_TooltipDescription
   shellPKey = UI_PKEY_TooltipDescription
   formatID = 00000005-7363-696e-8441798acf5aebb7
   propID = 5
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ TooltipDescription est utilisée par une application pour interroger la description associée à un [ \_ \_ TooltipTitle de l’interface utilisateur](windowsribbon-reference-properties-uipkey-tooltiptitle.md).

La valeur de la propriété est une chaîne limitée à toute séquence de caractères, y compris les espaces blancs et les sauts de ligne.

> [!Note]  
> Utilisez la référence de caractère XML UCS (Universal Character Set) `&#xA;` pour spécifier un saut de ligne.

 

La longueur maximale de l’interface utilisateur \_ \_ TooltipDescription est illimitée.

L’alignement à droite n’est pas pris en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés de la ressource](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Commande. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)
</dt> <dt>

[IU \_ \_ TooltipTitle](windowsribbon-reference-properties-uipkey-tooltiptitle.md)
</dt> </dl>

 

 




