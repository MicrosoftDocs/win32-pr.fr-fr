---
title: UI_PKEY_FontProperties_BackgroundColorType
description: Identifie la \_ \_ propriété FontProperties BackgroundColorType de l’interface utilisateur \_ .
ms.assetid: d93f4d9f-3d35-4066-be94-f6b6b4302bff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bbd2056087d584663c8ca716c4021554098dfa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443820"
---
# <a name="ui_pkey_fontproperties_backgroundcolortype"></a>IU \_ \_ FontProperties \_ BackgroundColorType

Identifie la \_ \_ propriété FontProperties BackgroundColorType de l’interface utilisateur \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_BackgroundColorType
   shellPKey = UI_PKEY_FontProperties_BackgroundColorType
   formatID = 00000311-7363-696e-8441798acf5aebb7
   propID = 311
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a>Remarques

L’interface utilisateur \_ \_ FontProperties \_ BackgroundColorType est utilisée par une application, conjointement avec [l’interface utilisateur de l’IU \_ \_ FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), pour interroger les paramètres de la Galerie de **couleurs de surbrillance du texte** .

La valeur de la propriété provient de l’énumération [**\_ SWATCHCOLORTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .

La valeur par défaut est `UI_SWATCHCOLORTYPE_RGB`.

Le tableau suivant décrit les valeurs des propriétés.



|   Propriété                             |   Description                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | L’application doit interroger la mesure système appropriée pour la valeur de couleur en général la **couleur d’arrière-plan** de la fenêtre de thème Windows actuelle qui est récupérée avec GetSysColor (fenêtre de couleur \_ ).                                                                                                                                                                                                                                                                 |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | Non pris en charge par [**FontControl**](windowsribbon-element-fontcontrol.md).                                                                                                                                                                                                                                                                                                                                                                                |
| `UI_SWATCHCOLORTYPE_RGB`       | L’application doit interroger l' [interface utilisateur \_ \_ FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) pour obtenir la valeur de couleur. La valeur de couleur de l' [interface utilisateur \_ \_ FontProperties \_ backgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor) est affichée dans le bouton **couleur de surbrillance du texte** et sélectionnée dans la Galerie de **couleurs de mise en surbrillance du texte** .<br/> |



 

L’interface utilisateur \_ \_ FontProperties \_ BackgroundColorType est transmise à la méthode de rappel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) lorsqu’un échantillon de couleur est sélectionné dans la Galerie de **couleurs de surbrillance du texte** [**FontControl**](windowsribbon-element-fontcontrol.md) .

> [!Note]  
> Il est fortement recommandé que l’application ne définisse qu’une valeur de **couleur de mise en surbrillance du texte** initiale et ne réaffecte pas cette valeur lorsque le curseur est repositionné dans un document. La dernière sélection doit être conservée pour éviter de devoir resélectionner la couleur souhaitée.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle de police](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**interface utilisateur \_ SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[Contrôle de police](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

