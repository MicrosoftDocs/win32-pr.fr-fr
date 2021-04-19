---
title: Application. views, propriété
description: Représente un conteneur pour chaque vue de l’infrastructure du ruban, en particulier le ruban et le ContextPopup.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Ruban Windows de la propriété application. views
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511153"
---
# <a name="applicationviews-property"></a><span data-ttu-id="db18d-104">Application. views, propriété</span><span class="sxs-lookup"><span data-stu-id="db18d-104">Application.Views property</span></span>

<span data-ttu-id="db18d-105">Représente un conteneur pour chaque vue de l’infrastructure du ruban, en particulier le [**ruban**](windowsribbon-element-ribbon.md) et le [**ContextPopup**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="db18d-105">Represents a container for each Ribbon framework View, specifically the [**Ribbon**](windowsribbon-element-ribbon.md) and the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="usage"></a><span data-ttu-id="db18d-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="db18d-106">Usage</span></span>

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a><span data-ttu-id="db18d-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="db18d-107">Attributes</span></span>

<span data-ttu-id="db18d-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="db18d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="db18d-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="db18d-109">Child elements</span></span>



| <span data-ttu-id="db18d-110">Élément</span><span class="sxs-lookup"><span data-stu-id="db18d-110">Element</span></span>                                                               | <span data-ttu-id="db18d-111">Description</span><span class="sxs-lookup"><span data-stu-id="db18d-111">Description</span></span>                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="db18d-112">**ContextPopup**</span><span class="sxs-lookup"><span data-stu-id="db18d-112">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> | <span data-ttu-id="db18d-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="db18d-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="db18d-114">**Ruban**</span><span class="sxs-lookup"><span data-stu-id="db18d-114">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/>             | <span data-ttu-id="db18d-115">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="db18d-115">Must occur exactly once</span></span><br/> <br/>     |



## <a name="parent-elements"></a><span data-ttu-id="db18d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="db18d-116">Parent elements</span></span>



| <span data-ttu-id="db18d-117">Élément</span><span class="sxs-lookup"><span data-stu-id="db18d-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="db18d-118">**Application**</span><span class="sxs-lookup"><span data-stu-id="db18d-118">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="db18d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="db18d-119">Remarks</span></span>

<span data-ttu-id="db18d-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="db18d-120">Required.</span></span>

<span data-ttu-id="db18d-121">Doit se produire exactement une fois pour chaque élément d' [**application**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="db18d-121">Must occur exactly once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="db18d-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="db18d-122">Examples</span></span>

<span data-ttu-id="db18d-123">L’exemple suivant montre un élément **application. views** qui contient un manifeste de contrôles de ruban, chacun avec une référence à une commande déclarée dans l’élément [**application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="db18d-123">The following example shows an **Application.Views** element that contains a manifest of Ribbon controls, each with a reference to a Command declared in the [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a><span data-ttu-id="db18d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db18d-124">Requirements</span></span>



| <span data-ttu-id="db18d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db18d-125">Requirement</span></span> | <span data-ttu-id="db18d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="db18d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="db18d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db18d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="db18d-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db18d-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="db18d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db18d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="db18d-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db18d-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="db18d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db18d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db18d-132">**Application. commandes**</span><span class="sxs-lookup"><span data-stu-id="db18d-132">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





