---
title: SplitButtonGallery. MenuLayout, propriété
description: Représente un conteneur pour les dispositions des menus déroulants de la Galerie de boutons partagés.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- Ruban Windows de la propriété SplitButtonGallery. MenuLayout
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510524"
---
# <a name="splitbuttongallerymenulayout-property"></a><span data-ttu-id="0c0b6-104">SplitButtonGallery. MenuLayout, propriété</span><span class="sxs-lookup"><span data-stu-id="0c0b6-104">SplitButtonGallery.MenuLayout property</span></span>

<span data-ttu-id="0c0b6-105">Représente un conteneur pour les dispositions des menus déroulants de la [Galerie de boutons partagés](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="0c0b6-105">Represents a container for [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="0c0b6-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="0c0b6-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="0c0b6-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="0c0b6-107">Attributes</span></span>

<span data-ttu-id="0c0b6-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0c0b6-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0c0b6-109">Child elements</span></span>



| <span data-ttu-id="0c0b6-110">Élément</span><span class="sxs-lookup"><span data-stu-id="0c0b6-110">Element</span></span>                                                                           | <span data-ttu-id="0c0b6-111">Description</span><span class="sxs-lookup"><span data-stu-id="0c0b6-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="0c0b6-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="0c0b6-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="0c0b6-113">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="0c0b6-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="0c0b6-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="0c0b6-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="0c0b6-115">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="0c0b6-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0c0b6-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="0c0b6-116">Parent elements</span></span>



| <span data-ttu-id="0c0b6-117">Élément</span><span class="sxs-lookup"><span data-stu-id="0c0b6-117">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="0c0b6-118">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="0c0b6-118">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0c0b6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="0c0b6-119">Remarks</span></span>

<span data-ttu-id="0c0b6-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-120">Optional.</span></span>

<span data-ttu-id="0c0b6-121">Peut se produire au plus une fois pour chaque élément [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="0c0b6-121">May occur at most once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="0c0b6-122">Un seul élément enfant ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) est autorisé.</span><span class="sxs-lookup"><span data-stu-id="0c0b6-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0c0b6-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="0c0b6-123">Examples</span></span>

<span data-ttu-id="0c0b6-124">L’exemple suivant illustre le balisage de base pour la [bibliothèque de boutons partagés](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="0c0b6-124">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="0c0b6-125">Cette section de code illustre la déclaration de contrôle **SplitButtonGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="0c0b6-125">This section of code shows the **SplitButtonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="0c0b6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c0b6-126">Requirements</span></span>



| <span data-ttu-id="0c0b6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c0b6-127">Requirement</span></span> | <span data-ttu-id="0c0b6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c0b6-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0c0b6-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c0b6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c0b6-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c0b6-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0c0b6-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c0b6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c0b6-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c0b6-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c0b6-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c0b6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c0b6-134">Contrôle de la Galerie des boutons partagés</span><span class="sxs-lookup"><span data-stu-id="0c0b6-134">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="0c0b6-135">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="0c0b6-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





