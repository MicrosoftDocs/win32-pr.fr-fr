---
title: UI_PKEY_FontProperties_Strikethrough
description: Identifie la \_ \_ propriété Strikethrough FontProperties barré de l’interface utilisateur \_ .
ms.assetid: 18ee653d-db01-4615-a85d-ad4ac6a0f422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b684704fdd90a8dd1b88b14db2b52540b15fccb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443790"
---
# <a name="ui_pkey_fontproperties_strikethrough"></a><span data-ttu-id="50a4e-103">IU \_ \_ FontProperties \_ barré</span><span class="sxs-lookup"><span data-stu-id="50a4e-103">UI\_PKEY\_FontProperties\_Strikethrough</span></span>

<span data-ttu-id="50a4e-104">Identifie la \_ \_ propriété Strikethrough FontProperties barré de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="50a4e-104">Identifies the UI\_PKEY\_FontProperties\_Strikethrough property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Strikethrough
   shellPKey = UI_PKEY_FontProperties_Strikethrough
   formatID = 00000306-7363-696e-8441798acf5aebb7
   propID = 306
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="50a4e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="50a4e-105">Remarks</span></span>

<span data-ttu-id="50a4e-106">L’interface utilisateur \_ \_ FontProperties \_ barré est utilisée par une application pour interroger l’état du bouton **barré** .</span><span class="sxs-lookup"><span data-stu-id="50a4e-106">UI\_PKEY\_FontProperties\_Strikethrough is used by an application to query the state of the **Strikethrough** button.</span></span>

<span data-ttu-id="50a4e-107">La valeur de la propriété provient de l’énumération [**\_ FONTPROPERTIES de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="50a4e-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="50a4e-108">La valeur par défaut est `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="50a4e-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="50a4e-109">La capture d’écran suivante montre le bouton **barré** du ruban [**FontControl**](windowsribbon-element-fontcontrol.md).</span><span class="sxs-lookup"><span data-stu-id="50a4e-109">The following screen shot shows the **Strikethrough** button of the Ribbon [**FontControl**](windowsribbon-element-fontcontrol.md).</span></span>

![capture d’écran de l’élément fontcontrol avec l’attribut richfont défini sur true.](images/markup/fontcontrol-strikethrough.png)

<span data-ttu-id="50a4e-111">Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50a4e-111">The following table describes the properties and the UI result.</span></span>



|   <span data-ttu-id="50a4e-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="50a4e-112">Property</span></span>                       |    <span data-ttu-id="50a4e-113">Résultat de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="50a4e-113">UI Result</span></span>                                                                 |
|----------------------------------|------------------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="50a4e-114">Le bouton **barré** est désactivé et ne peut être défini que par l’application.</span><span class="sxs-lookup"><span data-stu-id="50a4e-114">**Strikethrough** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="50a4e-115">Le bouton **barré** n’est pas sélectionné.</span><span class="sxs-lookup"><span data-stu-id="50a4e-115">**Strikethrough** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="50a4e-116">Le bouton **barré** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="50a4e-116">**Strikethrough** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="50a4e-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50a4e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50a4e-118">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="50a4e-118">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="50a4e-119">**interface utilisateur \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="50a4e-119">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="50a4e-120">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="50a4e-120">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 