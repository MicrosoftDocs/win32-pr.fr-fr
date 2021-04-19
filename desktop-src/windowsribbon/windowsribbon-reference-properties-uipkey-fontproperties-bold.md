---
title: UI_PKEY_FontProperties_Bold
description: Identifie la \_ \_ propriété FontProperties gras de l’interface utilisateur \_ .
ms.assetid: 9d33142a-bd63-423e-ba77-083c86bce1e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dca8a58b9c5bfa51cfba8d80a477dafb744dfb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510696"
---
# <a name="ui_pkey_fontproperties_bold"></a><span data-ttu-id="173db-103">IU \_ \_ FontProperties \_ gras</span><span class="sxs-lookup"><span data-stu-id="173db-103">UI\_PKEY\_FontProperties\_Bold</span></span>

<span data-ttu-id="173db-104">Identifie la \_ \_ propriété FontProperties gras de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="173db-104">Identifies the UI\_PKEY\_FontProperties\_Bold property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Bold
   shellPKey = UI_PKEY_FontProperties_Bold
   formatID = 00000303-7363-696e-8441798acf5aebb7
   propID = 303
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="173db-105">Notes</span><span class="sxs-lookup"><span data-stu-id="173db-105">Remarks</span></span>

<span data-ttu-id="173db-106">IU \_ \_ FontProperties \_ gras est utilisé par une application pour interroger l’état du bouton **gras** .</span><span class="sxs-lookup"><span data-stu-id="173db-106">UI\_PKEY\_FontProperties\_Bold is used by an application to query the state of the **Bold** button.</span></span>

<span data-ttu-id="173db-107">La valeur de la propriété provient de l’énumération [**\_ FONTPROPERTIES de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="173db-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="173db-108">La valeur par défaut est `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="173db-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="173db-109">Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="173db-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                     |
|----------------------------------|---------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="173db-110">Le bouton **gras** est désactivé et ne peut être défini que par l’application.</span><span class="sxs-lookup"><span data-stu-id="173db-110">**Bold** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="173db-111">Le bouton **gras** n’est pas sélectionné.</span><span class="sxs-lookup"><span data-stu-id="173db-111">**Bold** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="173db-112">Le bouton **gras** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="173db-112">**Bold** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="173db-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="173db-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="173db-114">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="173db-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="173db-115">**interface utilisateur \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="173db-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="173db-116">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="173db-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 