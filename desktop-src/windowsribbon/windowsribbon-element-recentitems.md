---
title: Élément RecentItems
description: Représente le contrôle éléments récents dans le menu de l’application.
ms.assetid: a3df0bb0-e0f8-413a-879d-8e39164535d0
keywords:
- Ruban des fenêtres d’élément RecentItems
topic_type:
- apiref
api_name:
- RecentItems
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17269342521a5da5db8d7a852a985c29ed7e2e98
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104030747"
---
# <a name="recentitems-element"></a><span data-ttu-id="194ef-104">Élément RecentItems</span><span class="sxs-lookup"><span data-stu-id="194ef-104">RecentItems element</span></span>

<span data-ttu-id="194ef-105">Représente le contrôle [éléments récents](windowsribbon-controls-recentitems.md) dans le [menu](windowsribbon-controls-applicationmenu.md)de l’application.</span><span class="sxs-lookup"><span data-stu-id="194ef-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="194ef-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="194ef-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="194ef-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="194ef-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="194ef-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="194ef-108">Attribute</span></span></th>
<th><span data-ttu-id="194ef-109">Type</span><span class="sxs-lookup"><span data-stu-id="194ef-109">Type</span></span></th>
<th><span data-ttu-id="194ef-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="194ef-110">Required</span></span></th>
<th><span data-ttu-id="194ef-111">Description</span><span class="sxs-lookup"><span data-stu-id="194ef-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="194ef-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="194ef-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="194ef-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="194ef-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="194ef-114">Non</span><span class="sxs-lookup"><span data-stu-id="194ef-114">No</span></span><br/></td>
<td><span data-ttu-id="194ef-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="194ef-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="194ef-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="194ef-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="194ef-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="194ef-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="194ef-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="194ef-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="194ef-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="194ef-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="194ef-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="194ef-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="194ef-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="194ef-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="194ef-122">Non</span><span class="sxs-lookup"><span data-stu-id="194ef-122">No</span></span><br/></td>
<td><span data-ttu-id="194ef-123">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="194ef-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="194ef-124">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="194ef-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="194ef-125">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="194ef-125">Default.</span></span> <br/> </dd> <span data-ttu-id="194ef-126"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="194ef-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="194ef-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="194ef-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="194ef-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="194ef-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="194ef-129">Non</span><span class="sxs-lookup"><span data-stu-id="194ef-129">No</span></span><br/></td>
<td><span data-ttu-id="194ef-130">Nombre d’éléments récents à afficher.</span><span class="sxs-lookup"><span data-stu-id="194ef-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="194ef-131">
<dt><span></span><span></span><strong></strong> (XS : nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="194ef-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="194ef-132">Valeur entière égale ou supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="194ef-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="194ef-133">La valeur par défaut est <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="194ef-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="194ef-134">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="194ef-134">Child elements</span></span>

<span data-ttu-id="194ef-135">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="194ef-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="194ef-136">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="194ef-136">Parent elements</span></span>



| <span data-ttu-id="194ef-137">Élément</span><span class="sxs-lookup"><span data-stu-id="194ef-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="194ef-138">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="194ef-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="194ef-139">Notes</span><span class="sxs-lookup"><span data-stu-id="194ef-139">Remarks</span></span>

<span data-ttu-id="194ef-140">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="194ef-140">Required.</span></span>

<span data-ttu-id="194ef-141">Doit se produire une seule fois pour chaque élément [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="194ef-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="194ef-142">Le contrôle [éléments récents](windowsribbon-controls-recentitems.md) affiche la liste des éléments utilisés le plus récemment (MRU) de l’application ruban.</span><span class="sxs-lookup"><span data-stu-id="194ef-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="194ef-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="194ef-143">Examples</span></span>

<span data-ttu-id="194ef-144">L’exemple suivant illustre le balisage de base pour le contrôle d' [éléments récents](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="194ef-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="194ef-145">L’exemple suivant illustre une déclaration de commande **RecentItems** .</span><span class="sxs-lookup"><span data-stu-id="194ef-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="194ef-146">L’exemple suivant illustre la déclaration de contrôles **RecentItems** associée.</span><span class="sxs-lookup"><span data-stu-id="194ef-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="194ef-147">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="194ef-147">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="194ef-148">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="194ef-148">Minimum supported system</span></span><br/> | <span data-ttu-id="194ef-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="194ef-149">Windows 7</span></span> |
| <span data-ttu-id="194ef-150">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="194ef-150">Can be empty</span></span>                        | <span data-ttu-id="194ef-151">Oui</span><span class="sxs-lookup"><span data-stu-id="194ef-151">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="194ef-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="194ef-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194ef-153">Contrôle de menu de l’application</span><span class="sxs-lookup"><span data-stu-id="194ef-153">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="194ef-154">Contrôle des éléments récents</span><span class="sxs-lookup"><span data-stu-id="194ef-154">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





