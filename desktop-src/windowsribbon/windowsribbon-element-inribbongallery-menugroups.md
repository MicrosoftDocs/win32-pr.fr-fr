---
title: InRibbonGallery. MenuGroups, propriété
description: Représente un conteneur pour le jeu d’éléments de menu déroulant d’un contrôle In-Ribbon Gallery.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- Ruban Windows de la propriété InRibbonGallery. MenuGroups
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032920"
---
# <a name="inribbongallerymenugroups-property"></a><span data-ttu-id="6dc6b-104">InRibbonGallery. MenuGroups, propriété</span><span class="sxs-lookup"><span data-stu-id="6dc6b-104">InRibbonGallery.MenuGroups property</span></span>

<span data-ttu-id="6dc6b-105">Représente un conteneur pour le jeu d’éléments de menu déroulant d’un contrôle [de galerie dans le ruban](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc6b-105">Represents a container for the set of drop-down menu items of an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="6dc6b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="6dc6b-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="6dc6b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="6dc6b-107">Attributes</span></span>

<span data-ttu-id="6dc6b-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="6dc6b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6dc6b-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6dc6b-109">Child elements</span></span>



| <span data-ttu-id="6dc6b-110">Élément</span><span class="sxs-lookup"><span data-stu-id="6dc6b-110">Element</span></span>                                                         | <span data-ttu-id="6dc6b-111">Description</span><span class="sxs-lookup"><span data-stu-id="6dc6b-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="6dc6b-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="6dc6b-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="6dc6b-113">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="6dc6b-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6dc6b-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="6dc6b-114">Parent elements</span></span>



| <span data-ttu-id="6dc6b-115">Élément</span><span class="sxs-lookup"><span data-stu-id="6dc6b-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="6dc6b-116">**InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="6dc6b-116">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6dc6b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6dc6b-117">Remarks</span></span>

<span data-ttu-id="6dc6b-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="6dc6b-118">Optional.</span></span>

<span data-ttu-id="6dc6b-119">Peut se produire au plus une fois pour chaque élément [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc6b-119">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="6dc6b-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="6dc6b-120">Examples</span></span>

<span data-ttu-id="6dc6b-121">L’exemple suivant illustre le balisage de base pour un contrôle [de galerie dans le ruban](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc6b-121">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

<span data-ttu-id="6dc6b-122">Cette section de code illustre la déclaration de contrôle **InRibbonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="6dc6b-122">This section of code shows the **InRibbonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6dc6b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6dc6b-123">Requirements</span></span>



| <span data-ttu-id="6dc6b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6dc6b-124">Requirement</span></span> | <span data-ttu-id="6dc6b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6dc6b-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6dc6b-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dc6b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6dc6b-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dc6b-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6dc6b-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6dc6b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6dc6b-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6dc6b-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6dc6b-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6dc6b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dc6b-131">Contrôle de galerie dans le ruban</span><span class="sxs-lookup"><span data-stu-id="6dc6b-131">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="6dc6b-132">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="6dc6b-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="6dc6b-133">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="6dc6b-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





