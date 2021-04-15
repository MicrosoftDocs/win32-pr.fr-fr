---
title: UI_PKEY_FontProperties_Underline
description: Identifie la \_ propriété de \_ soulignement FontProperties de l’interface utilisateur \_ .
ms.assetid: 88492558-ab19-4606-8fe0-5f100677b88a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 380c3fdadb636775f80b789a585c42ff2369234a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463379"
---
# <a name="ui_pkey_fontproperties_underline"></a><span data-ttu-id="d804c-103">IU \_ \_ FontProperties \_ souligné</span><span class="sxs-lookup"><span data-stu-id="d804c-103">UI\_PKEY\_FontProperties\_Underline</span></span>

<span data-ttu-id="d804c-104">Identifie la \_ propriété de \_ soulignement FontProperties de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="d804c-104">Identifies the UI\_PKEY\_FontProperties\_Underline property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Underline
   shellPKey = UI_PKEY_FontProperties_Underline
   formatID = 00000305-7363-696e-8441798acf5aebb7
   propID = 305
   typeInfo
      type = UI_FONTUNDERLINE
```

## <a name="remarks"></a><span data-ttu-id="d804c-105">Notes</span><span class="sxs-lookup"><span data-stu-id="d804c-105">Remarks</span></span>

<span data-ttu-id="d804c-106">IU \_ \_ FontProperties \_ souligné est utilisé par une application pour interroger l’état du bouton **souligné** .</span><span class="sxs-lookup"><span data-stu-id="d804c-106">UI\_PKEY\_FontProperties\_Underline is used by an application to query the state of the **Underline** button.</span></span>

<span data-ttu-id="d804c-107">La valeur de la propriété provient de l’énumération [**\_ FONTUNDERLINE de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) .</span><span class="sxs-lookup"><span data-stu-id="d804c-107">The property value is from the [**UI\_FONTUNDERLINE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline) enumeration.</span></span>

<span data-ttu-id="d804c-108">La valeur par défaut est `UI_FONTUNDERLINE_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="d804c-108">The default value is `UI_FONTUNDERLINE_NOTSET`.</span></span>

<span data-ttu-id="d804c-109">La capture d’écran suivante montre le bouton **souligné** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="d804c-109">The following screen shot shows the **Underline** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/markup/fontcontrol-underline.png)

<span data-ttu-id="d804c-111">Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d804c-111">The following table describes the properties and the UI result.</span></span>



|                                 |                                                                          |
|---------------------------------|--------------------------------------------------------------------------|
| `UI_FONTUNDERLINE_NOTAVAILABLE` | <span data-ttu-id="d804c-112">Le bouton **souligné** est désactivé et ne peut être défini que par l’application.</span><span class="sxs-lookup"><span data-stu-id="d804c-112">**Underline** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTUNDERLINE_NOTSET`       | <span data-ttu-id="d804c-113">Le bouton **souligné** n’est pas sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d804c-113">**Underline** button is not selected.</span></span>                                    |
| `UI_FONTUNDERLINE_SET`          | <span data-ttu-id="d804c-114">Bouton **souligné** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d804c-114">**Underline** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="d804c-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d804c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d804c-116">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="d804c-116">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="d804c-117">**IU \_ FONTUNDERLINE**</span><span class="sxs-lookup"><span data-stu-id="d804c-117">**UI\_FONTUNDERLINE**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontunderline)
</dt> <dt>

[<span data-ttu-id="d804c-118">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="d804c-118">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 