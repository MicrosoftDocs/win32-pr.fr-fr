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
# <a name="ui_pkey_fontproperties_foregroundcolortype"></a><span data-ttu-id="c5ad5-103">IU \_ \_ FontProperties \_ ForegroundColorType</span><span class="sxs-lookup"><span data-stu-id="c5ad5-103">UI\_PKEY\_FontProperties\_ForegroundColorType</span></span>

<span data-ttu-id="c5ad5-104">Identifie la \_ \_ propriété FontProperties ForegroundColorType de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="c5ad5-104">Identifies the UI\_PKEY\_FontProperties\_ForegroundColorType property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ForegroundColorType
   shellPKey = UI_PKEY_FontProperties_ForegroundColorType
   formatID = 00000310-7363-696e-8441798acf5aebb7
   propID = 310
   typeInfo
      type = UI_SWATCHCOLORTYPE
```

## <a name="remarks"></a><span data-ttu-id="c5ad5-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5ad5-105">Remarks</span></span>

<span data-ttu-id="c5ad5-106">L’interface utilisateur \_ \_ FontProperties \_ ForegroundColorType est utilisée par une application, conjointement avec [l' \_ UI \_ hyperFontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), pour interroger les paramètres de la Galerie de **couleurs de texte** .</span><span class="sxs-lookup"><span data-stu-id="c5ad5-106">UI\_PKEY\_FontProperties\_ForegroundColorType is used by an application, in conjunction with [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), to query **Text color** gallery settings.</span></span>

<span data-ttu-id="c5ad5-107">La valeur de la propriété provient de l’énumération [**\_ SWATCHCOLORTYPE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) .</span><span class="sxs-lookup"><span data-stu-id="c5ad5-107">The property value is from the [**UI\_SWATCHCOLORTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype) enumeration.</span></span>

<span data-ttu-id="c5ad5-108">La valeur par défaut est `UI_SWATCHCOLORTYPE_RGB`.</span><span class="sxs-lookup"><span data-stu-id="c5ad5-108">The default value is `UI_SWATCHCOLORTYPE_RGB`.</span></span>

<span data-ttu-id="c5ad5-109">Le tableau suivant décrit les valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="c5ad5-109">The following table describes the property values.</span></span>



|     <span data-ttu-id="c5ad5-110">Value</span><span class="sxs-lookup"><span data-stu-id="c5ad5-110">Value</span></span>                           |     <span data-ttu-id="c5ad5-111">Description</span><span class="sxs-lookup"><span data-stu-id="c5ad5-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `UI_SWATCHCOLORTYPE_NOCOLOR`   | <span data-ttu-id="c5ad5-112">Non pris en charge par [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="c5ad5-112">Not supported by the [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>                                                                                                                                                                                                                                                                                                                                        |
| `UI_SWATCHCOLORTYPE_AUTOMATIC` | <span data-ttu-id="c5ad5-113">L’application doit interroger la mesure système appropriée pour la valeur de couleur en général la **couleur du texte** du thème Windows actuel qui est récupérée avec GETSYSCOLOR (couleur \_ WINDOWTEXT).</span><span class="sxs-lookup"><span data-stu-id="c5ad5-113">Application should query the appropriate system metric for the color value typically the current Windows theme **text color** that is retrieved with GetSysColor(COLOR\_WINDOWTEXT).</span></span>                                                                                                                                                                                                                                  |
| `UI_SWATCHCOLORTYPE_RGB`       | <span data-ttu-id="c5ad5-114">L’application doit interroger l' [interface utilisateur \_ \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) pour obtenir la valeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="c5ad5-114">Application should query [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) for the color value.</span></span> <span data-ttu-id="c5ad5-115">La valeur de couleur de l' [interface utilisateur \_ \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) est affichée sur le bouton **couleur de texte** et sélectionnée dans la Galerie de **couleurs de texte** .</span><span class="sxs-lookup"><span data-stu-id="c5ad5-115">The color value of [UI\_PKEY\_FontProperties\_ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md) is displayed on the **Text color** button and selected in the **Text color** gallery.</span></span><br/> |



 

<span data-ttu-id="c5ad5-116">L' \_ UI \_ FontProperties \_ ForegroundColorType est passé à la méthode de rappel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) lorsqu’un échantillon de couleur est sélectionné dans une galerie de **couleurs de texte** [**FontControl**](windowsribbon-element-fontcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="c5ad5-116">UI\_PKEY\_FontProperties\_ForegroundColorType is passed to the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) callback method when a color swatch is selected in a [**FontControl**](windowsribbon-element-fontcontrol.md) **Text color** gallery.</span></span>

> [!Note]  
> <span data-ttu-id="c5ad5-117">Il est fortement recommandé que l’application ne définisse qu’une valeur de **couleur de texte** initiale et ne réaffecte pas cette valeur lorsque le curseur est repositionné dans un document.</span><span class="sxs-lookup"><span data-stu-id="c5ad5-117">It is highly recommended that the application only set an initial **Text color** value and not re-set this value when the cursor is repositioned within a document.</span></span> <span data-ttu-id="c5ad5-118">La dernière sélection doit être conservée pour éviter de devoir resélectionner la couleur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c5ad5-118">The last selection should be maintained to avoid the need to re-select the desired color.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c5ad5-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5ad5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5ad5-120">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="c5ad5-120">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="c5ad5-121">**interface utilisateur \_ SWATCHCOLORTYPE**</span><span class="sxs-lookup"><span data-stu-id="c5ad5-121">**UI\_SWATCHCOLORTYPE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_swatchcolortype)
</dt> <dt>

[<span data-ttu-id="c5ad5-122">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="c5ad5-122">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

