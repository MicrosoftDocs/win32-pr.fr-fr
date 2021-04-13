---
title: Propriété Ribbon. QuickAccessToolbar
description: Représente un conteneur pour la barre d’outils accès rapide (QAT).
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Ruban de la propriété Ribbon. QuickAccessToolbar
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383939"
---
# <a name="ribbonquickaccesstoolbar-property"></a><span data-ttu-id="bbd4b-104">Propriété Ribbon. QuickAccessToolbar</span><span class="sxs-lookup"><span data-stu-id="bbd4b-104">Ribbon.QuickAccessToolbar property</span></span>

<span data-ttu-id="bbd4b-105">Représente un conteneur pour la barre d’outils accès rapide (QAT).</span><span class="sxs-lookup"><span data-stu-id="bbd4b-105">Represents a container for the Quick Access Toolbar (QAT).</span></span>

## <a name="usage"></a><span data-ttu-id="bbd4b-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="bbd4b-106">Usage</span></span>

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="bbd4b-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="bbd4b-107">Attributes</span></span>

<span data-ttu-id="bbd4b-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="bbd4b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="bbd4b-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bbd4b-109">Child elements</span></span>



| <span data-ttu-id="bbd4b-110">Élément</span><span class="sxs-lookup"><span data-stu-id="bbd4b-110">Element</span></span>                                                                           | <span data-ttu-id="bbd4b-111">Description</span><span class="sxs-lookup"><span data-stu-id="bbd4b-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="bbd4b-112">**QuickAccessToolbar**</span><span class="sxs-lookup"><span data-stu-id="bbd4b-112">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> | <span data-ttu-id="bbd4b-113">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="bbd4b-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="bbd4b-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bbd4b-114">Parent elements</span></span>



| <span data-ttu-id="bbd4b-115">Élément</span><span class="sxs-lookup"><span data-stu-id="bbd4b-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="bbd4b-116">**Ruban**</span><span class="sxs-lookup"><span data-stu-id="bbd4b-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="bbd4b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="bbd4b-117">Remarks</span></span>

<span data-ttu-id="bbd4b-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="bbd4b-118">Required.</span></span>

<span data-ttu-id="bbd4b-119">Peut se produire une ou plusieurs fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="bbd4b-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bbd4b-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="bbd4b-120">Examples</span></span>

<span data-ttu-id="bbd4b-121">L’exemple suivant illustre le balisage de base pour l’élément **Ribbon. QuickAccessToolbar** .</span><span class="sxs-lookup"><span data-stu-id="bbd4b-121">The following example demonstrates the basic markup for the **Ribbon.QuickAccessToolbar** element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="bbd4b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbd4b-122">Requirements</span></span>



| <span data-ttu-id="bbd4b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbd4b-123">Requirement</span></span> | <span data-ttu-id="bbd4b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbd4b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bbd4b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbd4b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bbd4b-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbd4b-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bbd4b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbd4b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bbd4b-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbd4b-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





