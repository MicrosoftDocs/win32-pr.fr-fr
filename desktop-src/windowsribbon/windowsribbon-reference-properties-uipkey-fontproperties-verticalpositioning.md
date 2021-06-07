---
title: UI_PKEY_FontProperties_VerticalPositioning
description: Identifie la \_ \_ propriété FontProperties VerticalPositioning de l’interface utilisateur \_ .
ms.assetid: a92f845e-b0fc-4e23-9d06-ca16d2becf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 954b01ff3271b9f74fac2c130c697a70e910fc93
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444300"
---
# <a name="ui_pkey_fontproperties_verticalpositioning"></a>IU \_ \_ FontProperties \_ VerticalPositioning

Identifie la \_ \_ propriété FontProperties VerticalPositioning de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_VerticalPositioning
   shellPKey = UI_PKEY_FontProperties_VerticalPositioning
   formatID = 00000307-7363-696e-8441798acf5aebb7
   propID = 307
   typeInfo
      type = UI_FONTVERTICALPOSITION
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ FontProperties \_ VerticalPositioning est utilisée par une application pour interroger la valeur des contrôles **Superscript** et **indice** .

La valeur de la propriété provient de l’énumération [**\_ FONTVERTICALPOSITION de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition) .

La valeur par défaut est `UI_FONTVERTICALPOSITION_NOTSET`.

**La capture** d’écran suivante montre les boutons **exposant et indice** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/markup/fontcontrol-subsuper.png)

Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.



|     Propriété                           |          Résultat de l’interface utilisateur                                                                             |
|----------------------------------------|------------------------------------------------------------------------------------------------|
| `UI_FONTVERTICALPOSITION_NOTAVAILABLE` | Les boutons exposant et **indice** sont désactivés **et ne** peuvent être définis que par l’application. |
| `UI_FONTVERTICALPOSITION_NOTSET`       | **Les boutons exposant et** **indice** ne sont pas sélectionnés.                                    |
| `UI_FONTVERTICALPOSITION_SUPERSCRIPT`  | Le bouton **exposant** est sélectionné.                                                            |
| `UI_FONTVERTICALPOSITION_SUBSCRIPT`    | Le bouton d' **indice** est sélectionné.                                                              |



 

> [!Note]  
> Les  boutons exposant et **indice** ne peuvent pas être sélectionnés.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interface utilisateur \_ FONTVERTICALPOSITION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontverticalposition)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 