---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifie la propriété de l’interface utilisateur FontProperties de l’interface utilisateur \_ \_ \_ .
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404727"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>FontProperties de l’IU \_ \_ \_

Identifie la propriété de l’interface utilisateur FontProperties de l’interface utilisateur \_ \_ \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Notes

L’interface utilisateur \_ \_ FontProperties la valeur de l’option de type de variable \_ est utilisée par une application dans les cas où il n’est pas possible pour l’application de spécifier une valeur pour la **taille de police**, par exemple lorsqu’une série de texte de taille hétérogène est sélectionnée. Le contrôle de **taille de police** est défini sur vide et l’interface utilisateur FontProperties de l’interface utilisateur \_ \_ \_ est utilisée pour capturer l’interaction de l’utilisateur avec les boutons **agrandir la police** et **réduire la police** .

L’interface utilisateur de la FontProperties de l’interface utilisateur \_ \_ \_ est incluse dans [l’IU \_ \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).

La capture d’écran suivante montre les boutons **agrandir la police** et **réduire la police** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).

![capture d’écran des boutons agrandir la police et réduire la police sur le fontcontrol.](images/markup/fontcontrol-incdec.png)

Le tableau suivant décrit les valeurs des propriétés.



|     Valeur                 |  Description                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | L’utilisateur a cliqué sur le bouton **agrandir la police** .   |
| `UI_FONTDELTASIZE_SHRINK` | Clic sur le bouton **réduire la police** . |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interface utilisateur \_ FONTDELTASIZE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 