---
title: InRibbonGallery. MenuLayout, propriété
description: Représente un conteneur pour In-Ribbon mises en page de menu déroulant de la Galerie.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Ruban Windows de la propriété InRibbonGallery. MenuLayout
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032444"
---
# <a name="inribbongallerymenulayout-property"></a><span data-ttu-id="c1571-104">InRibbonGallery. MenuLayout, propriété</span><span class="sxs-lookup"><span data-stu-id="c1571-104">InRibbonGallery.MenuLayout property</span></span>

<span data-ttu-id="c1571-105">Représente un conteneur pour les dispositions des menus déroulants [de la galerie dans le ruban](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="c1571-105">Represents a container for [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="c1571-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c1571-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="c1571-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="c1571-107">Attributes</span></span>

<span data-ttu-id="c1571-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c1571-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c1571-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1571-109">Child elements</span></span>



| <span data-ttu-id="c1571-110">Élément</span><span class="sxs-lookup"><span data-stu-id="c1571-110">Element</span></span>                                                                           | <span data-ttu-id="c1571-111">Description</span><span class="sxs-lookup"><span data-stu-id="c1571-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="c1571-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="c1571-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="c1571-113">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="c1571-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="c1571-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="c1571-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="c1571-115">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="c1571-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c1571-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c1571-116">Parent elements</span></span>



| <span data-ttu-id="c1571-117">Élément</span><span class="sxs-lookup"><span data-stu-id="c1571-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="c1571-118">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="c1571-118">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c1571-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c1571-119">Remarks</span></span>

<span data-ttu-id="c1571-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="c1571-120">Optional.</span></span>

<span data-ttu-id="c1571-121">Peut se produire au plus une fois pour chaque élément [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="c1571-121">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="c1571-122">Un seul élément enfant ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) est autorisé.</span><span class="sxs-lookup"><span data-stu-id="c1571-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c1571-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="c1571-123">Examples</span></span>

<span data-ttu-id="c1571-124">L’exemple suivant illustre le balisage de base pour la [Galerie dans le ruban](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="c1571-124">The following example demonstrates the basic markup for the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="c1571-125">Cette section de code illustre la déclaration de contrôle **InRibbonGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="c1571-125">This section of code shows the **InRibbonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="c1571-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1571-126">Requirements</span></span>



| <span data-ttu-id="c1571-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1571-127">Requirement</span></span> | <span data-ttu-id="c1571-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1571-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c1571-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1571-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c1571-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1571-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c1571-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1571-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c1571-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1571-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1571-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1571-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1571-134">Contrôle de galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="c1571-134">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="c1571-135">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="c1571-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





