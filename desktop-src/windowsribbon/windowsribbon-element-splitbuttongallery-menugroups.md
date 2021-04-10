---
title: SplitButtonGallery. MenuGroups, propriété
description: Représente un conteneur pour un ensemble d’éléments de menu déroulant dans un contrôle SplitButtonGallery.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- Ruban Windows de la propriété SplitButtonGallery. MenuGroups
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103642"
---
# <a name="splitbuttongallerymenugroups-property"></a><span data-ttu-id="3709c-104">SplitButtonGallery. MenuGroups, propriété</span><span class="sxs-lookup"><span data-stu-id="3709c-104">SplitButtonGallery.MenuGroups property</span></span>

<span data-ttu-id="3709c-105">Représente un conteneur pour un ensemble d’éléments de menu déroulant dans un contrôle [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="3709c-105">Represents a container for a set of drop-down menu items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="3709c-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="3709c-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="3709c-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="3709c-107">Attributes</span></span>

<span data-ttu-id="3709c-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="3709c-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3709c-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3709c-109">Child elements</span></span>



| <span data-ttu-id="3709c-110">Élément</span><span class="sxs-lookup"><span data-stu-id="3709c-110">Element</span></span>                                                         | <span data-ttu-id="3709c-111">Description</span><span class="sxs-lookup"><span data-stu-id="3709c-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="3709c-112">**MenuGroup**</span><span class="sxs-lookup"><span data-stu-id="3709c-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="3709c-113">Doit se produire au moins une fois</span><span class="sxs-lookup"><span data-stu-id="3709c-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="3709c-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3709c-114">Parent elements</span></span>



| <span data-ttu-id="3709c-115">Élément</span><span class="sxs-lookup"><span data-stu-id="3709c-115">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="3709c-116">**SplitButtonGallery**</span><span class="sxs-lookup"><span data-stu-id="3709c-116">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="3709c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3709c-117">Remarks</span></span>

<span data-ttu-id="3709c-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3709c-118">Required.</span></span>

<span data-ttu-id="3709c-119">Doit se produire une seule fois pour chaque élément [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="3709c-119">Must occur exactly once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="3709c-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="3709c-120">Examples</span></span>

<span data-ttu-id="3709c-121">L’exemple suivant illustre le balisage de base pour l’élément **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="3709c-121">The following example demonstrates the basic markup for the **SplitButtonGallery.MenuGroups** element.</span></span>

<span data-ttu-id="3709c-122">Cette section de code illustre la déclaration de contrôle **SplitButtonGallery. MenuGroups** .</span><span class="sxs-lookup"><span data-stu-id="3709c-122">This section of code shows the **SplitButtonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3709c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3709c-123">Requirements</span></span>



| <span data-ttu-id="3709c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3709c-124">Requirement</span></span> | <span data-ttu-id="3709c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="3709c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3709c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3709c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3709c-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3709c-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3709c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3709c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3709c-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3709c-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3709c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3709c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3709c-131">Contrôle de la Galerie des boutons partagés</span><span class="sxs-lookup"><span data-stu-id="3709c-131">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="3709c-132">Utilisation des galeries</span><span class="sxs-lookup"><span data-stu-id="3709c-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





