---
title: UI_PKEY_RecentColorsCategoryLabel
description: Identifie la propriété RecentColorsCategoryLabel de l’interface utilisateur \_ \_ .
ms.assetid: e9336b98-59ae-4118-8535-009fc0fda4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bcb2e3f5df1ba66204a8df6b088ca3a2808ced
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674221"
---
# <a name="ui_pkey_recentcolorscategorylabel"></a><span data-ttu-id="00d85-103">IU \_ \_ RecentColorsCategoryLabel</span><span class="sxs-lookup"><span data-stu-id="00d85-103">UI\_PKEY\_RecentColorsCategoryLabel</span></span>

<span data-ttu-id="00d85-104">Identifie la propriété RecentColorsCategoryLabel de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="00d85-104">Identifies the UI\_PKEY\_RecentColorsCategoryLabel property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentColorsCategoryLabel
   shellPKey = UI_PKEY_RecentColorsCategoryLabel
   formatID = 00000405-7363-696e-8441798acf5aebb7
   propID = 405
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a><span data-ttu-id="00d85-105">Notes</span><span class="sxs-lookup"><span data-stu-id="00d85-105">Remarks</span></span>

<span data-ttu-id="00d85-106">L’interface utilisateur \_ \_ RecentColorsCategoryLabel est utilisée par une application pour interroger la valeur de l’étiquette associée à la catégorie de **couleurs récentes** d’un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="00d85-106">UI\_PKEY\_RecentColorsCategoryLabel is used by an application to query the value of the label associated with the **Recent Colors** category of a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

<span data-ttu-id="00d85-107">L’interface utilisateur \_ \_ RecentColorsCategoryLabel est valide uniquement pour un [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) où `ThemeColors` est spécifié comme valeur de l’attribut **ColorTemplate** (il s’agit du seul modèle qui contient des catégories étiquetées).</span><span class="sxs-lookup"><span data-stu-id="00d85-107">UI\_PKEY\_RecentColorsCategoryLabel is valid only for a [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) where `ThemeColors` is specified as the value of the **ColorTemplate** attribute (this is the only template that contains labeled categories).</span></span>

<span data-ttu-id="00d85-108">La capture d’écran suivante montre un `ThemeColors`  [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span><span class="sxs-lookup"><span data-stu-id="00d85-108">The following screen shot shows a `ThemeColors` [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md).</span></span>

![capture d’écran de l’élément dropdowncolorpicker avec l’attribut colortemplate défini sur ThemeColors.](images/markup/colortemplate.themedcolors.recentcolors.png)

## <a name="related-topics"></a><span data-ttu-id="00d85-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="00d85-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00d85-111">Propriétés du sélecteur de couleurs</span><span class="sxs-lookup"><span data-stu-id="00d85-111">Color Picker Properties</span></span>](windowsribbon-reference-properties-colorpicker.md)
</dt> </dl>

 

 




