---
title: UI_PKEY_FontProperties_ForegroundColorType
description: Identifie la \_ \_ propriété FontProperties ForegroundColorType de l’interface utilisateur \_ .
ms.assetid: ab04c0b0-911f-4649-9ce8-5ecd847abf9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f261256a36ee7a387c6c3a695d8c1182898690c2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444350"
---
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a>IU \_ \_ FontProperties \_ ForegroundColorType

Identifie la \_ \_ propriété FontProperties ForegroundColorType de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ FontProperties \_ ForegroundColorType est utilisée par une application, conjointement avec [l' \_ UI \_ hyperFontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), pour interroger les paramètres de la Galerie de **couleurs de texte** .

La valeur de la propriété provient de l’énumération [**\_ SWATCHCOLORTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

La valeur par défaut est `UI_SWATCHCOLORTYPE_RGB`.

Le tableau suivant décrit les valeurs des propriétés.



|     Value                           |     Description                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | Non pris en charge par [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | L’application doit interroger la mesure système appropriée pour la valeur de couleur en général la **couleur du texte** du thème Windows actuel qui est récupérée avec GETSYSCOLOR (couleur \_ WINDOWTEXT).                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | L’application doit interroger l' [interface utilisateur \_ \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) pour obtenir la valeur de couleur. La valeur de couleur de l' [interface utilisateur \_ \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) est affichée sur le bouton **couleur de texte** et sélectionnée dans la Galerie de **couleurs de texte** .<br/> |



 

L' \_ UI \_ FontProperties \_ ForegroundColorType est passé à la méthode de rappel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) lorsqu’un échantillon de couleur est sélectionné dans une galerie de **couleurs de texte** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> Il est fortement recommandé que l’application ne définisse qu’une valeur de **couleur de texte** initiale et ne réaffecte pas cette valeur lorsque le curseur est repositionné dans un document. La dernière sélection doit être conservée pour éviter de devoir resélectionner la couleur souhaitée.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interface utilisateur \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

