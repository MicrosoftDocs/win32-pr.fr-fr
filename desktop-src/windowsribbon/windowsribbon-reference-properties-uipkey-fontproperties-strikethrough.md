---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifie la \_ \_ propriété Strikethrough FontProperties barré de l’interface utilisateur \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746172ec2209861615375e73dee3f2336950a2dd93e76b33893190e9f7e8bc18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850303"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a>IU \_ \_ FontProperties \_ barré

Identifie la \_ \_ propriété Strikethrough FontProperties barré de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ FontProperties \_ barré est utilisée par une application pour interroger l’état du bouton **barré** .

La valeur de la propriété provient de l’énumération [**\_ FONTPROPERTIES de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .

La valeur par défaut est `UI_FONTPROPERTIES_NOTSET`.

La capture d’écran suivante montre le bouton **barré** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/markup/fontcontrol-strikethrough.png)

Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.



|   Propriété                       |    Résultat de l’interface utilisateur                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | Le bouton **barré** est désactivé et ne peut être défini que par l’application. |
| `UI_FONTPROPERTIES_NOTSET`       | Le bouton **barré** n’est pas sélectionné.                                    |
| `UI_FONTPROPERTIES_SET`          | Le bouton **barré** est sélectionné.                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interface utilisateur \_ FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 