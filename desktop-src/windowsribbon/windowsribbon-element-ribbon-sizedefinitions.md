---
title: Propriété Ribbon. SizeDefinitions
description: Représente un conteneur pour les modèles de disposition personnalisés des contrôles du ruban.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Ruban de la propriété Ribbon. SizeDefinitions
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032442"
---
# <a name="ribbonsizedefinitions-property"></a><span data-ttu-id="c6c8d-104">Propriété Ribbon. SizeDefinitions</span><span class="sxs-lookup"><span data-stu-id="c6c8d-104">Ribbon.SizeDefinitions property</span></span>

<span data-ttu-id="c6c8d-105">Représente un conteneur pour les modèles de disposition personnalisés des contrôles du ruban.</span><span class="sxs-lookup"><span data-stu-id="c6c8d-105">Represents a container for custom layout templates of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="c6c8d-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="c6c8d-106">Usage</span></span>

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="c6c8d-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="c6c8d-107">Attributes</span></span>

<span data-ttu-id="c6c8d-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c6c8d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c6c8d-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c6c8d-109">Child elements</span></span>



| <span data-ttu-id="c6c8d-110">Élément</span><span class="sxs-lookup"><span data-stu-id="c6c8d-110">Element</span></span>                                                                   | <span data-ttu-id="c6c8d-111">Description</span><span class="sxs-lookup"><span data-stu-id="c6c8d-111">Description</span></span>                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="c6c8d-112">**SizeDefinition**</span><span class="sxs-lookup"><span data-stu-id="c6c8d-112">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> | <span data-ttu-id="c6c8d-113">Peut se produire une ou plusieurs fois</span><span class="sxs-lookup"><span data-stu-id="c6c8d-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="c6c8d-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c6c8d-114">Parent elements</span></span>



| <span data-ttu-id="c6c8d-115">Élément</span><span class="sxs-lookup"><span data-stu-id="c6c8d-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="c6c8d-116">**Ruban**</span><span class="sxs-lookup"><span data-stu-id="c6c8d-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c6c8d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c6c8d-117">Remarks</span></span>

<span data-ttu-id="c6c8d-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="c6c8d-118">Optional.</span></span>

<span data-ttu-id="c6c8d-119">Peut se produire au plus une fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="c6c8d-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c6c8d-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="c6c8d-120">Examples</span></span>

<span data-ttu-id="c6c8d-121">L’exemple de code suivant illustre un modèle personnalisé de base.</span><span class="sxs-lookup"><span data-stu-id="c6c8d-121">The following code example illustrates a basic custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a><span data-ttu-id="c6c8d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6c8d-122">Requirements</span></span>



| <span data-ttu-id="c6c8d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6c8d-123">Requirement</span></span> | <span data-ttu-id="c6c8d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6c8d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c6c8d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6c8d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c8d-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6c8d-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c6c8d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6c8d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c8d-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6c8d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6c8d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6c8d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c8d-130">Personnalisation d’un ruban à l’aide de définitions de taille et de stratégies de mise à l’échelle</span><span class="sxs-lookup"><span data-stu-id="c6c8d-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





