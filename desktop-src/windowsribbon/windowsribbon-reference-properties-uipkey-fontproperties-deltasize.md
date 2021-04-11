---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifie la propriété de l’interface utilisateur FontProperties de l’interface utilisateur \_ \_ \_ .
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031256"
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



|                           |                                 |
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

 

 