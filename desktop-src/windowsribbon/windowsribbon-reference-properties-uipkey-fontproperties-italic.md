---
title: UI_PKEY_FontProperties_Italic
description: Identifie la \_ \_ propriété FontProperties italique de l’interface utilisateur \_ .
ms.assetid: 53edd88e-ed7e-4385-9fd9-bfa90be348cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00825807c57632b1bbea69c47bc9b90d705efa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382097"
---
# <a name="ui_pkey_fontproperties_italic"></a><span data-ttu-id="51e65-103">IU \_ \_ FontProperties \_ italique</span><span class="sxs-lookup"><span data-stu-id="51e65-103">UI\_PKEY\_FontProperties\_Italic</span></span>

<span data-ttu-id="51e65-104">Identifie la \_ \_ propriété FontProperties italique de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="51e65-104">Identifies the UI\_PKEY\_FontProperties\_Italic property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_Italic
   shellPKey = UI_PKEY_FontProperties_Italic
   formatID = 00000304-7363-696e-8441798acf5aebb7
   propID = 304
   typeInfo
      type = UI_FONTPROPERTIES
```

## <a name="remarks"></a><span data-ttu-id="51e65-105">Notes</span><span class="sxs-lookup"><span data-stu-id="51e65-105">Remarks</span></span>

<span data-ttu-id="51e65-106">IU \_ \_ FontProperties \_ italique est utilisé par une application pour interroger l’état du bouton **italique** .</span><span class="sxs-lookup"><span data-stu-id="51e65-106">UI\_PKEY\_FontProperties\_Italic is used by an application to query the state of the **Italic** button.</span></span>

<span data-ttu-id="51e65-107">La valeur de la propriété provient de l’énumération [**\_ FONTPROPERTIES de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) .</span><span class="sxs-lookup"><span data-stu-id="51e65-107">The property value is from the [**UI\_FONTPROPERTIES**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties) enumeration.</span></span>

<span data-ttu-id="51e65-108">La valeur par défaut est `UI_FONTPROPERTIES_NOTSET`.</span><span class="sxs-lookup"><span data-stu-id="51e65-108">The default value is `UI_FONTPROPERTIES_NOTSET`.</span></span>

<span data-ttu-id="51e65-109">Le tableau suivant décrit les propriétés et le résultat de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="51e65-109">The following table describes the properties and the UI result.</span></span>



|                                  |                                                                       |
|----------------------------------|-----------------------------------------------------------------------|
| `UI_FONTPROPERTIES_NOTAVAILABLE` | <span data-ttu-id="51e65-110">Le bouton **italique** est désactivé et ne peut être défini que par l’application.</span><span class="sxs-lookup"><span data-stu-id="51e65-110">**Italic** button is disabled and can only be set by the application.</span></span> |
| `UI_FONTPROPERTIES_NOTSET`       | <span data-ttu-id="51e65-111">Le bouton **italique** n’est pas sélectionné.</span><span class="sxs-lookup"><span data-stu-id="51e65-111">**Italic** button is not selected.</span></span>                                    |
| `UI_FONTPROPERTIES_SET`          | <span data-ttu-id="51e65-112">Le bouton **italique** est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="51e65-112">**Italic** button is selected.</span></span>                                        |



 

## <a name="related-topics"></a><span data-ttu-id="51e65-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="51e65-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51e65-114">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="51e65-114">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="51e65-115">**interface utilisateur \_ FONTPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="51e65-115">**UI\_FONTPROPERTIES**</span></span>](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontproperties)
</dt> <dt>

[<span data-ttu-id="51e65-116">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="51e65-116">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 