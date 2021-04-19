---
title: UI_PKEY_RecentItems
description: Identifie la propriété RecentItems de l’interface utilisateur \_ \_ .
ms.assetid: 54e7ad1f-86b3-45e0-a0f4-5ee0d08e9d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07410d3152fb49b55460ec15c6914c53f3b6850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510074"
---
# <a name="ui_pkey_recentitems"></a><span data-ttu-id="9affd-103">IU \_ \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="9affd-103">UI\_PKEY\_RecentItems</span></span>

<span data-ttu-id="9affd-104">Identifie la propriété RecentItems de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9affd-104">Identifies the UI\_PKEY\_RecentItems property.</span></span>

```
propertyDescription
   name = UI_PKEY_RecentItems
   shellPKey = UI_PKEY_RecentItems
   formatID = 00000350-7363-696e-8441798acf5aebb7
   propID = 350
   typeInfo
      type = VT_ARRAY | VT_UNKNOWN
```

## <a name="remarks"></a><span data-ttu-id="9affd-105">Notes</span><span class="sxs-lookup"><span data-stu-id="9affd-105">Remarks</span></span>

<span data-ttu-id="9affd-106">[Interface utilisateur \_ Le \_ ](windowsribbon-reference-properties-uipkey-pinned.md) groupe de lignes ajouté est utilisé par une application pour interroger le tableau d’éléments dans la collection d’éléments utilisés le plus récemment (MRU) du menu de l' [application](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="9affd-106">[UI\_PKEY\_Pinned](windowsribbon-reference-properties-uipkey-pinned.md) is used by an application to query the array of items in the most recently used (MRU) items collection of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span> <span data-ttu-id="9affd-107">Les informations de chaque élément MRU sont encapsulées dans un objet [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) et incluent les trois clés de propriété suivantes :</span><span class="sxs-lookup"><span data-stu-id="9affd-107">The information for each MRU item is encapsulated in an [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object and includes the following three property keys:</span></span>

-   [<span data-ttu-id="9affd-108">\_Étiquette de nom de l’interface utilisateur \_</span><span class="sxs-lookup"><span data-stu-id="9affd-108">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)
-   [<span data-ttu-id="9affd-109">IU \_ \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="9affd-109">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)
-   [<span data-ttu-id="9affd-110">IU de l’IU \_ \_ épinglé</span><span class="sxs-lookup"><span data-stu-id="9affd-110">UI\_PKEY\_Pinned</span></span>](windowsribbon-reference-properties-uipkey-pinned.md)

<span data-ttu-id="9affd-111">La liste des éléments utilisés récemment est transmise à l’application hôte du ruban sous la forme d’un **SAFEARRAY** de pointeurs [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pour les implémentations respectives dans l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="9affd-111">The list of MRU items is passed to the Ribbon host application as a **SAFEARRAY** of [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) pointers to respective implementations in the host application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9affd-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9affd-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9affd-113">Propriétés de l’État</span><span class="sxs-lookup"><span data-stu-id="9affd-113">State Properties</span></span>](windowsribbon-reference-properties-state.md)
</dt> </dl>

 

 