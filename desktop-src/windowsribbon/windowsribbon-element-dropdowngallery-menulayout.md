---
title: DropDownGallery. MenuLayout, propriété
description: Représente un conteneur pour les dispositions de menus déroulants DropDownGallery.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- Ruban Windows de la propriété DropDownGallery. MenuLayout
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510563"
---
# <a name="dropdowngallerymenulayout-property"></a><span data-ttu-id="131d2-104">DropDownGallery. MenuLayout, propriété</span><span class="sxs-lookup"><span data-stu-id="131d2-104">DropDownGallery.MenuLayout property</span></span>

<span data-ttu-id="131d2-105">Représente un conteneur pour les dispositions de menus déroulants [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="131d2-105">Represents a container for [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="131d2-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="131d2-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="131d2-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="131d2-107">Attributes</span></span>

<span data-ttu-id="131d2-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="131d2-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="131d2-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="131d2-109">Child elements</span></span>



| <span data-ttu-id="131d2-110">Élément</span><span class="sxs-lookup"><span data-stu-id="131d2-110">Element</span></span>                                                                           | <span data-ttu-id="131d2-111">Description</span><span class="sxs-lookup"><span data-stu-id="131d2-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="131d2-112">**FlowMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="131d2-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="131d2-113">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="131d2-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="131d2-114">**VerticalMenuLayout**</span><span class="sxs-lookup"><span data-stu-id="131d2-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="131d2-115">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="131d2-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="131d2-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="131d2-116">Parent elements</span></span>



| <span data-ttu-id="131d2-117">Élément</span><span class="sxs-lookup"><span data-stu-id="131d2-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="131d2-118">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="131d2-118">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="131d2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="131d2-119">Remarks</span></span>

<span data-ttu-id="131d2-120">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="131d2-120">Optional.</span></span>

<span data-ttu-id="131d2-121">Peut se produire au plus une fois pour chaque élément [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="131d2-121">May occur at most once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="131d2-122">Un seul élément enfant ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) ou [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) est autorisé.</span><span class="sxs-lookup"><span data-stu-id="131d2-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="131d2-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="131d2-123">Examples</span></span>

<span data-ttu-id="131d2-124">L’exemple suivant illustre le balisage de base pour [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="131d2-124">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="131d2-125">Cette section de code illustre la déclaration de contrôle **DropDownGallery. MenuLayout** .</span><span class="sxs-lookup"><span data-stu-id="131d2-125">This section of code shows the **DropDownGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="131d2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="131d2-126">Requirements</span></span>



| <span data-ttu-id="131d2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="131d2-127">Requirement</span></span> | <span data-ttu-id="131d2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="131d2-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="131d2-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="131d2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="131d2-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="131d2-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="131d2-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="131d2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="131d2-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="131d2-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="131d2-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="131d2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="131d2-134">**Contrôle de la Galerie déroulante**</span><span class="sxs-lookup"><span data-stu-id="131d2-134">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="131d2-135">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="131d2-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





