---
title: Élément Ribbon
description: Représente le contrôle de ruban dans la vue du ruban.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- Ruban des fenêtres d’élément de ruban
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a743fc354dfea73c525884ec5ffe1f9471f3752
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111445000"
---
# <a name="ribbon-element"></a><span data-ttu-id="3065e-104">Élément Ribbon</span><span class="sxs-lookup"><span data-stu-id="3065e-104">Ribbon element</span></span>

<span data-ttu-id="3065e-105">Représente le contrôle de ruban dans la vue du ruban.</span><span class="sxs-lookup"><span data-stu-id="3065e-105">Represents the ribbon control in the Ribbon View.</span></span>

## <a name="usage"></a><span data-ttu-id="3065e-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3065e-106">Usage</span></span>

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a><span data-ttu-id="3065e-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3065e-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3065e-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="3065e-108">Attribute</span></span></th>
<th><span data-ttu-id="3065e-109">Type</span><span class="sxs-lookup"><span data-stu-id="3065e-109">Type</span></span></th>
<th><span data-ttu-id="3065e-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3065e-110">Required</span></span></th>
<th><span data-ttu-id="3065e-111">Description</span><span class="sxs-lookup"><span data-stu-id="3065e-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3065e-112"><strong>GroupSpacing</strong></span><span class="sxs-lookup"><span data-stu-id="3065e-112"><strong>GroupSpacing</strong></span></span><br/></td>
<td><span data-ttu-id="3065e-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="3065e-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="3065e-114">Non</span><span class="sxs-lookup"><span data-stu-id="3065e-114">No</span></span><br/></td>
<td><span data-ttu-id="3065e-115"><dt><span></span><span></span><strong></strong> Small</span><span class="sxs-lookup"><span data-stu-id="3065e-115"><dt><span></span><span></span><strong></strong> (Small)</span></span><br/> </dt> <dd> <span data-ttu-id="3065e-116">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="3065e-116">Default.</span></span> <br/> </dd> <span data-ttu-id="3065e-117"><dt><span></span><span></span><strong></strong> Médias</span><span class="sxs-lookup"><span data-stu-id="3065e-117"><dt><span></span><span></span><strong></strong> (Medium)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="3065e-118"><dt><span></span><span></span><strong></strong> Conséquent</span><span class="sxs-lookup"><span data-stu-id="3065e-118"><dt><span></span><span></span><strong></strong> (Large)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3065e-119"><strong>Nom</strong></span><span class="sxs-lookup"><span data-stu-id="3065e-119"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="3065e-120">xs:string</span><span class="sxs-lookup"><span data-stu-id="3065e-120">xs:string</span></span><br/></td>
<td><span data-ttu-id="3065e-121">Non</span><span class="sxs-lookup"><span data-stu-id="3065e-121">No</span></span><br/></td>
<td><span data-ttu-id="3065e-122">Utilisé pour annoter l’élément Command.</span><span class="sxs-lookup"><span data-stu-id="3065e-122">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="3065e-123">
<dt><span></span><span></span><strong></strong> (XS : String)</span><span class="sxs-lookup"><span data-stu-id="3065e-123">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="3065e-124">Toute séquence de zéro ou plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="3065e-124">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="3065e-125">La longueur maximale est illimitée.</span><span class="sxs-lookup"><span data-stu-id="3065e-125">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="3065e-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3065e-126">Child elements</span></span>



| <span data-ttu-id="3065e-127">Élément</span><span class="sxs-lookup"><span data-stu-id="3065e-127">Element</span></span>                                                                                         | <span data-ttu-id="3065e-128">Description</span><span class="sxs-lookup"><span data-stu-id="3065e-128">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="3065e-129">**Ruban. ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="3065e-129">**Ribbon.ApplicationMenu**</span></span>](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | <span data-ttu-id="3065e-130">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3065e-130">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3065e-131">**Ruban. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="3065e-131">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | <span data-ttu-id="3065e-132">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3065e-132">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3065e-133">**Ruban. HelpButton**</span><span class="sxs-lookup"><span data-stu-id="3065e-133">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | <span data-ttu-id="3065e-134">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3065e-134">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3065e-135">**Ruban. QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="3065e-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | <span data-ttu-id="3065e-136">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3065e-136">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3065e-137">**Ruban. SizeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="3065e-137">**Ribbon.SizeDefinitions**</span></span>](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | <span data-ttu-id="3065e-138">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3065e-138">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="3065e-139">**Ruban. tabulations**</span><span class="sxs-lookup"><span data-stu-id="3065e-139">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)<br/>                             | <span data-ttu-id="3065e-140">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="3065e-140">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3065e-141">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3065e-141">Parent elements</span></span>



| <span data-ttu-id="3065e-142">Élément</span><span class="sxs-lookup"><span data-stu-id="3065e-142">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="3065e-143">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="3065e-143">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3065e-144">Remarques</span><span class="sxs-lookup"><span data-stu-id="3065e-144">Remarks</span></span>

<span data-ttu-id="3065e-145">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3065e-145">Required.</span></span>

<span data-ttu-id="3065e-146">Doit se produire exactement une fois pour chaque élément [**application. views**](windowsribbon-element-application-views.md) .</span><span class="sxs-lookup"><span data-stu-id="3065e-146">Must occur exactly once for each [**Application.Views**](windowsribbon-element-application-views.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="3065e-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="3065e-147">Examples</span></span>

<span data-ttu-id="3065e-148">L’exemple suivant illustre le balisage de base pour une vue de **ruban** .</span><span class="sxs-lookup"><span data-stu-id="3065e-148">The following example demonstrates the basic markup for a **Ribbon** View.</span></span>


```XML
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a><span data-ttu-id="3065e-149">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3065e-149">Element information</span></span>




* <span data-ttu-id="3065e-150">**Système minimal pris en charge**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="3065e-150">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="3065e-151">**Peut être vide**: non</span><span class="sxs-lookup"><span data-stu-id="3065e-151">**Can be empty**: No</span></span>



 

 





