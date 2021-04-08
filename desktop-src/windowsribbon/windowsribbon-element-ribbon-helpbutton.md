---
title: Propriété Ribbon. HelpButton
description: Représente un conteneur pour le bouton aide.
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Ruban de la propriété Ribbon. HelpButton
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742293"
---
# <a name="ribbonhelpbutton-property"></a><span data-ttu-id="d0313-104">Propriété Ribbon. HelpButton</span><span class="sxs-lookup"><span data-stu-id="d0313-104">Ribbon.HelpButton property</span></span>

<span data-ttu-id="d0313-105">Représente un conteneur pour le [bouton aide](windowsribbon-controls-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="d0313-105">Represents a container for the [Help Button](windowsribbon-controls-helpbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d0313-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="d0313-106">Usage</span></span>

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a><span data-ttu-id="d0313-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="d0313-107">Attributes</span></span>

<span data-ttu-id="d0313-108">Il n’y a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d0313-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d0313-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d0313-109">Child elements</span></span>



| <span data-ttu-id="d0313-110">Élément</span><span class="sxs-lookup"><span data-stu-id="d0313-110">Element</span></span>                                                           | <span data-ttu-id="d0313-111">Description</span><span class="sxs-lookup"><span data-stu-id="d0313-111">Description</span></span>                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="d0313-112">**HelpButton**</span><span class="sxs-lookup"><span data-stu-id="d0313-112">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)<br/> | <span data-ttu-id="d0313-113">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="d0313-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="d0313-114">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d0313-114">Parent elements</span></span>



| <span data-ttu-id="d0313-115">Élément</span><span class="sxs-lookup"><span data-stu-id="d0313-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="d0313-116">**Ruban**</span><span class="sxs-lookup"><span data-stu-id="d0313-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d0313-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d0313-117">Remarks</span></span>

<span data-ttu-id="d0313-118">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d0313-118">Optional.</span></span>

<span data-ttu-id="d0313-119">Peut se produire au plus une fois pour chaque [**ruban**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="d0313-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d0313-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="d0313-120">Examples</span></span>

<span data-ttu-id="d0313-121">L’exemple suivant illustre le balisage de base requis pour implémenter un bouton d’aide du ruban.</span><span class="sxs-lookup"><span data-stu-id="d0313-121">The following example demonstrates the basic markup that is required to implement a Ribbon Help button.</span></span>

<span data-ttu-id="d0313-122">Cette section de code affiche la déclaration de commande **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="d0313-122">This section of code shows the **Ribbon.HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="d0313-123">Cette section de code affiche la déclaration de contrôle **Ribbon. HelpButton** .</span><span class="sxs-lookup"><span data-stu-id="d0313-123">This section of code shows the **Ribbon.HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a><span data-ttu-id="d0313-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0313-124">Requirements</span></span>



| <span data-ttu-id="d0313-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0313-125">Requirement</span></span> | <span data-ttu-id="d0313-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0313-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d0313-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0313-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d0313-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0313-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d0313-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0313-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d0313-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0313-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





