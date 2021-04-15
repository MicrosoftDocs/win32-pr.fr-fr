---
title: ApplicationMenu. RecentItems, propriété
description: Représente un conteneur pour le contrôle d’éléments récents dans le menu de l’application.
ms.assetid: 26ed38b6-17de-423f-a113-ccbaf3780a91
keywords:
- Ruban Windows de la propriété ApplicationMenu. RecentItems
topic_type:
- apiref
api_name:
- ApplicationMenu.RecentItems
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 473ab6436eabd7fcbbbfb533a8ae4afc07098c81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384728"
---
# <a name="applicationmenurecentitems-property"></a><span data-ttu-id="1b8c8-104">ApplicationMenu. RecentItems, propriété</span><span class="sxs-lookup"><span data-stu-id="1b8c8-104">ApplicationMenu.RecentItems property</span></span>

<span data-ttu-id="1b8c8-105">Représente un conteneur pour le contrôle d' [éléments récents](windowsribbon-controls-recentitems.md) dans le menu de l' [application](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="1b8c8-105">Represents a container for the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="1b8c8-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="1b8c8-106">Usage</span></span>

``` syntax
<ApplicationMenu.RecentItems
  CommandName = "xs:positiveInteger or xs:string"
>
  child elements
</ApplicationMenu.RecentItems>
```

## <a name="attributes"></a><span data-ttu-id="1b8c8-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="1b8c8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b8c8-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="1b8c8-108">Attribute</span></span></th>
<th><span data-ttu-id="1b8c8-109">Type</span><span class="sxs-lookup"><span data-stu-id="1b8c8-109">Type</span></span></th>
<th><span data-ttu-id="1b8c8-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1b8c8-110">Required</span></span></th>
<th><span data-ttu-id="1b8c8-111">Description</span><span class="sxs-lookup"><span data-stu-id="1b8c8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b8c8-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="1b8c8-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="1b8c8-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="1b8c8-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="1b8c8-114">Non</span><span class="sxs-lookup"><span data-stu-id="1b8c8-114">No</span></span><br/></td>
<td><span data-ttu-id="1b8c8-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1b8c8-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="1b8c8-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="1b8c8-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="1b8c8-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="1b8c8-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="1b8c8-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="1b8c8-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="1b8c8-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="1b8c8-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="1b8c8-120">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1b8c8-120">Child elements</span></span>



| <span data-ttu-id="1b8c8-121">Élément</span><span class="sxs-lookup"><span data-stu-id="1b8c8-121">Element</span></span>                                                             | <span data-ttu-id="1b8c8-122">Description</span><span class="sxs-lookup"><span data-stu-id="1b8c8-122">Description</span></span>                                    |
|---------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="1b8c8-123">**RecentItems**</span><span class="sxs-lookup"><span data-stu-id="1b8c8-123">**RecentItems**</span></span>](windowsribbon-element-recentitems.md)<br/> | <span data-ttu-id="1b8c8-124">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="1b8c8-124">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="1b8c8-125">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1b8c8-125">Parent elements</span></span>



| <span data-ttu-id="1b8c8-126">Élément</span><span class="sxs-lookup"><span data-stu-id="1b8c8-126">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="1b8c8-127">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="1b8c8-127">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="1b8c8-128">Notes</span><span class="sxs-lookup"><span data-stu-id="1b8c8-128">Remarks</span></span>

<span data-ttu-id="1b8c8-129">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="1b8c8-129">Optional.</span></span>

<span data-ttu-id="1b8c8-130">Peut se produire au plus une fois pour chaque élément [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8c8-130">May occur at most once for each [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) element.</span></span>

<span data-ttu-id="1b8c8-131">Le contrôle [éléments récents](windowsribbon-controls-recentitems.md) affiche la liste des éléments utilisés le plus récemment (MRU) de l’application ruban.</span><span class="sxs-lookup"><span data-stu-id="1b8c8-131">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="1b8c8-132">Exemples</span><span class="sxs-lookup"><span data-stu-id="1b8c8-132">Examples</span></span>

<span data-ttu-id="1b8c8-133">L’exemple suivant illustre le balisage de base pour le contrôle d' [éléments récents](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8c8-133">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="1b8c8-134">L’exemple suivant illustre une déclaration de commande [**RecentItems**](windowsribbon-element-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8c8-134">The following example shows a [**RecentItems**](windowsribbon-element-recentitems.md) Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="1b8c8-135">L’exemple suivant illustre la déclaration des contrôles **ApplicationMenu. RecentItems** et [**RecentItems**](windowsribbon-element-recentitems.md) associés.</span><span class="sxs-lookup"><span data-stu-id="1b8c8-135">The following example shows the associated **ApplicationMenu.RecentItems** and [**RecentItems**](windowsribbon-element-recentitems.md) controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="requirements"></a><span data-ttu-id="1b8c8-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b8c8-136">Requirements</span></span>



| <span data-ttu-id="1b8c8-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b8c8-137">Requirement</span></span> | <span data-ttu-id="1b8c8-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b8c8-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="1b8c8-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b8c8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1b8c8-140">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b8c8-140">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="1b8c8-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b8c8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1b8c8-142">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b8c8-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1b8c8-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b8c8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b8c8-144">Contrôle de menu de l’application</span><span class="sxs-lookup"><span data-stu-id="1b8c8-144">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="1b8c8-145">Contrôle des éléments récents</span><span class="sxs-lookup"><span data-stu-id="1b8c8-145">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





