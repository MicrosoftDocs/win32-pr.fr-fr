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
ms.openlocfilehash: a433e2f04eae8607b0c14c5494c734ad0f0dd83a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444110"
---
# <a name="recentitems-element"></a><span data-ttu-id="281c8-104">Élément RecentItems</span><span class="sxs-lookup"><span data-stu-id="281c8-104">RecentItems element</span></span>

<span data-ttu-id="281c8-105">Représente le contrôle [éléments récents](windowsribbon-controls-recentitems.md) dans le [menu](windowsribbon-controls-applicationmenu.md)de l’application.</span><span class="sxs-lookup"><span data-stu-id="281c8-105">Represents the [Recent Items](windowsribbon-controls-recentitems.md) control in the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

## <a name="usage"></a><span data-ttu-id="281c8-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="281c8-106">Usage</span></span>

``` syntax
<RecentItems
  CommandName = "xs:positiveInteger or xs:string"
  MaxCount = "xs:nonNegativeInteger"
  EnablePinning = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="281c8-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="281c8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="281c8-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="281c8-108">Attribute</span></span></th>
<th><span data-ttu-id="281c8-109">Type</span><span class="sxs-lookup"><span data-stu-id="281c8-109">Type</span></span></th>
<th><span data-ttu-id="281c8-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="281c8-110">Required</span></span></th>
<th><span data-ttu-id="281c8-111">Description</span><span class="sxs-lookup"><span data-stu-id="281c8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="281c8-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="281c8-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="281c8-113">XS : positiveInteger ou XS : String</span><span class="sxs-lookup"><span data-stu-id="281c8-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="281c8-114">Non</span><span class="sxs-lookup"><span data-stu-id="281c8-114">No</span></span><br/></td>
<td><span data-ttu-id="281c8-115">Associe l’élément à une <a href="windowsribbon-element-command.md"><strong>commande</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="281c8-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="281c8-116">
<dt><span></span><span></span><strong></strong> (XS : positiveInteger ou XS : String)</span><span class="sxs-lookup"><span data-stu-id="281c8-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="281c8-117">Chaîne, valeur entière comprise entre 2 et 59999, inclusive, ou valeur hexadécimale comprise entre 0X2 et 0xea5f inclus.</span><span class="sxs-lookup"><span data-stu-id="281c8-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="281c8-118">La valeur doit être unique dans le document XML du ruban.</span><span class="sxs-lookup"><span data-stu-id="281c8-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="281c8-119">Longueur maximale : 100 caractères.</span><span class="sxs-lookup"><span data-stu-id="281c8-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="281c8-120"><strong>EnablePinning</strong></span><span class="sxs-lookup"><span data-stu-id="281c8-120"><strong>EnablePinning</strong></span></span><br/></td>
<td><span data-ttu-id="281c8-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="281c8-121">Boolean</span></span><br/></td>
<td><span data-ttu-id="281c8-122">Non</span><span class="sxs-lookup"><span data-stu-id="281c8-122">No</span></span><br/></td>
<td><span data-ttu-id="281c8-123">Limité à l’une des valeurs suivantes (0 et 1 ne sont pas valides) :</span><span class="sxs-lookup"><span data-stu-id="281c8-123">Restricted to one of the following values (0 and 1 are not valid):</span></span><br/> <br/><span data-ttu-id="281c8-124">
<dt><span></span><span></span><strong></strong> :</span><span class="sxs-lookup"><span data-stu-id="281c8-124">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="281c8-125">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="281c8-125">Default.</span></span> <br/> </dd> <span data-ttu-id="281c8-126"><dt><span></span><span></span><strong></strong> fausses</span><span class="sxs-lookup"><span data-stu-id="281c8-126"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="281c8-127"><strong>MaxCount</strong></span><span class="sxs-lookup"><span data-stu-id="281c8-127"><strong>MaxCount</strong></span></span><br/></td>
<td><span data-ttu-id="281c8-128">xs:nonNegativeInteger</span><span class="sxs-lookup"><span data-stu-id="281c8-128">xs:nonNegativeInteger</span></span><br/></td>
<td><span data-ttu-id="281c8-129">Non</span><span class="sxs-lookup"><span data-stu-id="281c8-129">No</span></span><br/></td>
<td><span data-ttu-id="281c8-130">Nombre d’éléments récents à afficher.</span><span class="sxs-lookup"><span data-stu-id="281c8-130">The number of recent items to display.</span></span><br/> <br/><span data-ttu-id="281c8-131">
<dt><span></span><span></span><strong></strong> (XS : nonNegativeInteger)</span><span class="sxs-lookup"><span data-stu-id="281c8-131">
<dt><span></span><span></span><strong></strong> (xs:nonNegativeInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="281c8-132">Valeur entière égale ou supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="281c8-132">An integer value of 0 or greater.</span></span><br/> <span data-ttu-id="281c8-133">La valeur par défaut est <strong>10</strong>.</span><span class="sxs-lookup"><span data-stu-id="281c8-133">Default is <strong>10</strong>.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="281c8-134">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="281c8-134">Child elements</span></span>

<span data-ttu-id="281c8-135">Il n’y a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="281c8-135">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="281c8-136">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="281c8-136">Parent elements</span></span>



| <span data-ttu-id="281c8-137">Élément</span><span class="sxs-lookup"><span data-stu-id="281c8-137">Element</span></span>                                                                                             |
|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="281c8-138">**ApplicationMenu.RecentItems**</span><span class="sxs-lookup"><span data-stu-id="281c8-138">**ApplicationMenu.RecentItems**</span></span>](windowsribbon-element-applicationmenu-recentitems.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="281c8-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="281c8-139">Remarks</span></span>

<span data-ttu-id="281c8-140">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="281c8-140">Required.</span></span>

<span data-ttu-id="281c8-141">Doit se produire une seule fois pour chaque élément [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="281c8-141">Must occur exactly once for each [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) element.</span></span>

<span data-ttu-id="281c8-142">Le contrôle [éléments récents](windowsribbon-controls-recentitems.md) affiche la liste des éléments utilisés le plus récemment (MRU) de l’application ruban.</span><span class="sxs-lookup"><span data-stu-id="281c8-142">The [Recent Items](windowsribbon-controls-recentitems.md) control displays the most recently used (MRU) items list of the Ribbon application.</span></span>

## <a name="examples"></a><span data-ttu-id="281c8-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="281c8-143">Examples</span></span>

<span data-ttu-id="281c8-144">L’exemple suivant illustre le balisage de base pour le contrôle d' [éléments récents](windowsribbon-controls-recentitems.md) .</span><span class="sxs-lookup"><span data-stu-id="281c8-144">The following example demonstrates the basic markup for the [Recent Items](windowsribbon-controls-recentitems.md) control.</span></span>

<span data-ttu-id="281c8-145">L’exemple suivant illustre une déclaration de commande **RecentItems** .</span><span class="sxs-lookup"><span data-stu-id="281c8-145">The following example shows a **RecentItems** Command declaration.</span></span>


```XML
<!-- Command declaration for most recently used items. -->
<Command Name="cmdMRUItems"
         Symbol="ID_FILE_MRUITEMS"
         Id="25050"/>
```



<span data-ttu-id="281c8-146">L’exemple suivant illustre la déclaration de contrôles **RecentItems** associée.</span><span class="sxs-lookup"><span data-stu-id="281c8-146">The following example shows the associated **RecentItems** controls declaration.</span></span>


```XML
<!-- Most recently used items collection. -->
<ApplicationMenu.RecentItems>
  <RecentItems CommandName="cmdMRUItems"/>
</ApplicationMenu.RecentItems>
```



## <a name="element-information"></a><span data-ttu-id="281c8-147">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="281c8-147">Element information</span></span>

* <span data-ttu-id="281c8-148">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="281c8-148">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="281c8-149">**Peut être vide**: Oui</span><span class="sxs-lookup"><span data-stu-id="281c8-149">**Can be empty**: Yes</span></span>


## <a name="see-also"></a><span data-ttu-id="281c8-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="281c8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="281c8-151">Contrôle de menu de l’application</span><span class="sxs-lookup"><span data-stu-id="281c8-151">Application Menu control</span></span>](windowsribbon-controls-applicationmenu.md)
</dt> <dt>

[<span data-ttu-id="281c8-152">Contrôle des éléments récents</span><span class="sxs-lookup"><span data-stu-id="281c8-152">Recent Items control</span></span>](windowsribbon-controls-recentitems.md)
</dt> </dl>

 

 





