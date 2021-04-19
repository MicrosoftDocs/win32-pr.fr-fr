---
title: DropDownGallery. MenuGroups, propriété
description: Représente un conteneur pour un ensemble d’éléments de menu déroulants dans un contrôle de Galerie de Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Ruban Windows de la propriété DropDownGallery. MenuGroups
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510564"
---
# <a name="dropdowngallerymenugroups-property"></a><span data-ttu-id="ed36e-104">DropDownGallery. MenuGroups, propriété</span><span class="sxs-lookup"><span data-stu-id="ed36e-104">DropDownGallery.MenuGroups property</span></span>

<span data-ttu-id="ed36e-105">Représente un conteneur pour un ensemble d’éléments de menu déroulants dans un contrôle de [Galerie](windowsribbon-controls-dropdowngallery.md) déroulante.</span><span class="sxs-lookup"><span data-stu-id="ed36e-105">Represents a container for a set of drop-down menu items in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="ed36e-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="ed36e-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="ed36e-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="ed36e-107">Attributes</span></span>

<span data-ttu-id="ed36e-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="ed36e-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ed36e-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ed36e-109">Child elements</span></span>



| <span data-ttu-id="ed36e-110">Élément</span><span class="sxs-lookup"><span data-stu-id="ed36e-110">Element</span></span>                                                         | <span data-ttu-id="ed36e-111">Description</span><span class="sxs-lookup"><span data-stu-id="ed36e-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="ed36e-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="ed36e-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="ed36e-113">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="ed36e-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ed36e-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ed36e-114">Parent elements</span></span>



| <span data-ttu-id="ed36e-115">Élément</span><span class="sxs-lookup"><span data-stu-id="ed36e-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ed36e-116">**DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="ed36e-116">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ed36e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ed36e-117">Remarks</span></span>

<span data-ttu-id="ed36e-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ed36e-118">Required.</span></span>

<span data-ttu-id="ed36e-119">Doit se produire une seule fois pour chaque élément [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ed36e-119">Must occur exactly once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="ed36e-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="ed36e-120">Examples</span></span>

<span data-ttu-id="ed36e-121">L’exemple suivant illustre le balisage de base pour l’élément **DropDownGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="ed36e-121">The following example demonstrates the basic markup for the **DropDownGallery.MenuGroups** element.</span></span>

<span data-ttu-id="ed36e-122">Cette section de code illustre la déclaration de contrôle **DropDownGallery. MenuGroups** dans un espace de commandes de [la Galerie déroulante](windowsribbon-controls-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ed36e-122">This section of code shows the **DropDownGallery.MenuGroups** control declaration in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) Command Space.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ed36e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed36e-123">Requirements</span></span>



| <span data-ttu-id="ed36e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed36e-124">Requirement</span></span> | <span data-ttu-id="ed36e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed36e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ed36e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed36e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ed36e-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed36e-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ed36e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed36e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ed36e-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed36e-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed36e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed36e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed36e-131">**Contrôle de la Galerie déroulante**</span><span class="sxs-lookup"><span data-stu-id="ed36e-131">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="ed36e-132">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="ed36e-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





