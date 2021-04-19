---
title: Propriété Ribbon. ApplicationMenu
description: Représente le menu de l’application. | Propriété Ribbon. ApplicationMenu
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Ruban de la propriété Ribbon. ApplicationMenu
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531303"
---
# <a name="ribbonapplicationmenu-property"></a><span data-ttu-id="76a34-105">Propriété Ribbon. ApplicationMenu</span><span class="sxs-lookup"><span data-stu-id="76a34-105">Ribbon.ApplicationMenu property</span></span>

<span data-ttu-id="76a34-106">Représente le menu de l’application.</span><span class="sxs-lookup"><span data-stu-id="76a34-106">Represents the Application Menu.</span></span>

## <a name="usage"></a><span data-ttu-id="76a34-107">Utilisation</span><span class="sxs-lookup"><span data-stu-id="76a34-107">Usage</span></span>

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="76a34-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="76a34-108">Attributes</span></span>

<span data-ttu-id="76a34-109">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="76a34-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="76a34-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="76a34-110">Child elements</span></span>



| <span data-ttu-id="76a34-111">Élément</span><span class="sxs-lookup"><span data-stu-id="76a34-111">Element</span></span>                                                                     | <span data-ttu-id="76a34-112">Description</span><span class="sxs-lookup"><span data-stu-id="76a34-112">Description</span></span>                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="76a34-113">**ApplicationMenu**</span><span class="sxs-lookup"><span data-stu-id="76a34-113">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> | <span data-ttu-id="76a34-114">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="76a34-114">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="76a34-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="76a34-115">Parent elements</span></span>



| <span data-ttu-id="76a34-116">Élément</span><span class="sxs-lookup"><span data-stu-id="76a34-116">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="76a34-117">**Ruban**</span><span class="sxs-lookup"><span data-stu-id="76a34-117">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="76a34-118">Notes</span><span class="sxs-lookup"><span data-stu-id="76a34-118">Remarks</span></span>

<span data-ttu-id="76a34-119">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="76a34-119">Required.</span></span>

<span data-ttu-id="76a34-120">Peut se produire au plus une fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="76a34-120">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="76a34-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="76a34-121">Examples</span></span>

<span data-ttu-id="76a34-122">L’exemple suivant illustre le balisage de base pour l’élément **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="76a34-122">The following example demonstrates the basic markup for the **Ribbon.ApplicationMenu** element.</span></span>

<span data-ttu-id="76a34-123">Cette section de code affiche la déclaration de contrôle **Ribbon. ApplicationMenu** .</span><span class="sxs-lookup"><span data-stu-id="76a34-123">This section of code shows the **Ribbon.ApplicationMenu** control declaration.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a><span data-ttu-id="76a34-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76a34-124">Requirements</span></span>



| <span data-ttu-id="76a34-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76a34-125">Requirement</span></span> | <span data-ttu-id="76a34-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="76a34-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="76a34-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a34-127">Minimum supported client</span></span><br/> | <span data-ttu-id="76a34-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a34-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="76a34-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a34-129">Minimum supported server</span></span><br/> | <span data-ttu-id="76a34-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a34-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





