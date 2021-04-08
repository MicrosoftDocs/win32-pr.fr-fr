---
title: Élément d’application
description: Représente l’élément de niveau supérieur dans la spécification de balisage de l’infrastructure de ruban Windows.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Ruban des fenêtres d’élément d’application
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734716"
---
# <a name="application-element"></a><span data-ttu-id="38b1d-104">Élément d’application</span><span class="sxs-lookup"><span data-stu-id="38b1d-104">Application element</span></span>

<span data-ttu-id="38b1d-105">Représente l’élément de niveau supérieur dans la spécification de balisage de l’infrastructure de ruban Windows.</span><span class="sxs-lookup"><span data-stu-id="38b1d-105">Represents the top-level element in the Windows Ribbon framework markup specification.</span></span>

## <a name="usage"></a><span data-ttu-id="38b1d-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="38b1d-106">Usage</span></span>

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a><span data-ttu-id="38b1d-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="38b1d-107">Attributes</span></span>



| <span data-ttu-id="38b1d-108">Attribut</span><span class="sxs-lookup"><span data-stu-id="38b1d-108">Attribute</span></span>            | <span data-ttu-id="38b1d-109">Type</span><span class="sxs-lookup"><span data-stu-id="38b1d-109">Type</span></span>                 | <span data-ttu-id="38b1d-110">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="38b1d-110">Required</span></span>       | <span data-ttu-id="38b1d-111">Description</span><span class="sxs-lookup"><span data-stu-id="38b1d-111">Description</span></span>                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b1d-112">**xmlns**</span><span class="sxs-lookup"><span data-stu-id="38b1d-112">**xmlns**</span></span><br/> | <span data-ttu-id="38b1d-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="38b1d-113">xs:string</span></span><br/> | <span data-ttu-id="38b1d-114">Oui</span><span class="sxs-lookup"><span data-stu-id="38b1d-114">Yes</span></span><br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> <span data-ttu-id="38b1d-115">URI de la liaison d’espace de noms du balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="38b1d-115">The URI for the Ribbon markup namespace binding.</span></span> <br/> </dd> </dl> |



## <a name="child-elements"></a><span data-ttu-id="38b1d-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="38b1d-116">Child elements</span></span>



| <span data-ttu-id="38b1d-117">Élément</span><span class="sxs-lookup"><span data-stu-id="38b1d-117">Element</span></span>                                                                               | <span data-ttu-id="38b1d-118">Description</span><span class="sxs-lookup"><span data-stu-id="38b1d-118">Description</span></span>                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="38b1d-119">**Application. commandes**</span><span class="sxs-lookup"><span data-stu-id="38b1d-119">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> | <span data-ttu-id="38b1d-120">Peut se produire au plus une fois</span><span class="sxs-lookup"><span data-stu-id="38b1d-120">May occur at most once</span></span><br/> <br/>  |
| [<span data-ttu-id="38b1d-121">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="38b1d-121">**Application.Views**</span></span>](windowsribbon-element-application-views.md)<br/>       | <span data-ttu-id="38b1d-122">Doit se produire exactement une fois</span><span class="sxs-lookup"><span data-stu-id="38b1d-122">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="38b1d-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="38b1d-123">Parent elements</span></span>

<span data-ttu-id="38b1d-124">Il n’y a pas d’éléments parents.</span><span class="sxs-lookup"><span data-stu-id="38b1d-124">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="38b1d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="38b1d-125">Remarks</span></span>

<span data-ttu-id="38b1d-126">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="38b1d-126">Required.</span></span>

<span data-ttu-id="38b1d-127">Doit se produire exactement une fois comme conteneur pour l’ensemble du balisage du ruban.</span><span class="sxs-lookup"><span data-stu-id="38b1d-127">Must occur exactly once as the container for all of the Ribbon markup.</span></span>

<span data-ttu-id="38b1d-128">Les éléments enfants de l’élément **application** doivent se produire dans l’ordre spécifié :</span><span class="sxs-lookup"><span data-stu-id="38b1d-128">The child elements of the **Application** element must occur in the specified order:</span></span>

1.  [<span data-ttu-id="38b1d-129">**Application. commandes**</span><span class="sxs-lookup"><span data-stu-id="38b1d-129">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
2.  [<span data-ttu-id="38b1d-130">**Application. views**</span><span class="sxs-lookup"><span data-stu-id="38b1d-130">**Application.Views**</span></span>](windowsribbon-element-application-views.md)

## <a name="examples"></a><span data-ttu-id="38b1d-131">Exemples</span><span class="sxs-lookup"><span data-stu-id="38b1d-131">Examples</span></span>

<span data-ttu-id="38b1d-132">L’exemple suivant illustre une déclaration d’élément d' **application** .</span><span class="sxs-lookup"><span data-stu-id="38b1d-132">The following example shows an **Application** element declaration.</span></span>


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a><span data-ttu-id="38b1d-133">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="38b1d-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="38b1d-134">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38b1d-134">Minimum supported system</span></span><br/> | <span data-ttu-id="38b1d-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="38b1d-135">Windows 7</span></span> |
| <span data-ttu-id="38b1d-136">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="38b1d-136">Can be empty</span></span>                        | <span data-ttu-id="38b1d-137">Non</span><span class="sxs-lookup"><span data-stu-id="38b1d-137">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="38b1d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38b1d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b1d-139">Déclaration des commandes et des contrôles avec le balisage du ruban</span><span class="sxs-lookup"><span data-stu-id="38b1d-139">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 





