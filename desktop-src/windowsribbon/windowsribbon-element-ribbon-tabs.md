---
title: Ruban. Tabs, propriété
description: Représente un conteneur pour tous les onglets principaux dans un ruban.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Ruban de la fenêtre de propriétés ruban. Tabs
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464442"
---
# <a name="ribbontabs-property"></a><span data-ttu-id="a4cde-104">Ruban. Tabs, propriété</span><span class="sxs-lookup"><span data-stu-id="a4cde-104">Ribbon.Tabs property</span></span>

<span data-ttu-id="a4cde-105">Représente un conteneur pour tous les onglets principaux dans un ruban.</span><span class="sxs-lookup"><span data-stu-id="a4cde-105">Represents a container for all core tabs in a Ribbon.</span></span>

## <a name="usage"></a><span data-ttu-id="a4cde-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="a4cde-106">Usage</span></span>

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a><span data-ttu-id="a4cde-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="a4cde-107">Attributes</span></span>

<span data-ttu-id="a4cde-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="a4cde-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a4cde-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a4cde-109">Child elements</span></span>



| <span data-ttu-id="a4cde-110">Élément</span><span class="sxs-lookup"><span data-stu-id="a4cde-110">Element</span></span>                                             | <span data-ttu-id="a4cde-111">Description</span><span class="sxs-lookup"><span data-stu-id="a4cde-111">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="a4cde-112">**Onglet**</span><span class="sxs-lookup"><span data-stu-id="a4cde-112">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="a4cde-113">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="a4cde-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a4cde-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a4cde-114">Parent elements</span></span>



| <span data-ttu-id="a4cde-115">Élément</span><span class="sxs-lookup"><span data-stu-id="a4cde-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="a4cde-116">**Ruban**</span><span class="sxs-lookup"><span data-stu-id="a4cde-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a4cde-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a4cde-117">Remarks</span></span>

<span data-ttu-id="a4cde-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4cde-118">Required.</span></span>

<span data-ttu-id="a4cde-119">Peut se produire une ou plusieurs fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="a4cde-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="a4cde-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="a4cde-120">Examples</span></span>

<span data-ttu-id="a4cde-121">L’exemple suivant illustre le balisage de base pour un élément **ruban. Tabs** avec une déclaration de l' [**onglet**](windowsribbon-element-tab.md) de **base** .</span><span class="sxs-lookup"><span data-stu-id="a4cde-121">The following example demonstrates the basic markup for a **Ribbon.Tabs** element with a **Home** [**Tab**](windowsribbon-element-tab.md) declaration.</span></span>


```C++
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
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
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



## <a name="requirements"></a><span data-ttu-id="a4cde-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4cde-122">Requirements</span></span>



| <span data-ttu-id="a4cde-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4cde-123">Requirement</span></span> | <span data-ttu-id="a4cde-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4cde-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a4cde-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4cde-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a4cde-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4cde-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a4cde-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4cde-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a4cde-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4cde-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4cde-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4cde-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4cde-130">**Ruban. ContextualTabs**</span><span class="sxs-lookup"><span data-stu-id="a4cde-130">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





