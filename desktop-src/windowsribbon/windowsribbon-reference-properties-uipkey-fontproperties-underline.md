---
title: UI_PKEY_FontProperties_Underline
description: Identifie la \_ propriété de \_ soulignement FontProperties de l’interface utilisateur \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066027e5f62416667619937eea7dbe493a3ff279
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443780"
---
# <a name="ui_pkey_fontproperties_underline"></a>IU \_ \_ FontProperties \_ souligné

Identifie la \_ propriété de \_ soulignement FontProperties de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a>Remarques

IU \_ \_ FontProperties \_ souligné est utilisé par une application pour interroger l’état du bouton **souligné** .

La valeur de la propriété provient de l’énumération [**\_ FONTUNDERLINE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .

La valeur par défaut est `UI_FONTUNDERLINE_NOTSET`.

La capture d’écran suivante montre le bouton **souligné** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/markup/fontcontrol-underline.png)

Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.



|      Propriété                   |       Résultat de l’interface utilisateur                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | Le bouton **souligné** est désactivé et ne peut être défini que par l’application. |
| `UI_FONTUNDERLINE_NOTSET`       | Le bouton **souligné** n’est pas sélectionné.                                    |
| `UI_FONTUNDERLINE_SET`          | Bouton **souligné** est sélectionné.                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**IU \_ FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 