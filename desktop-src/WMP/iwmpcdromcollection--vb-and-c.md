---
title: Interface IWMPCdromCollection (VB et C) (WMP. h)
description: Fournit un moyen d’organiser et d’accéder à une collection de lecteurs de CD ou DVD. L’interface IWMPCdromCollection expose la propriété suivante.
ms.assetid: 60874603-d9c8-4ed1-a92a-bd069bd0c253
keywords:
- IWMPCdromCollection (VB et C) interface Windows Media Player
- Interface IWMPCdromCollection (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPCdromCollection (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3fbc9c053c186b6d542e201f7bee5d2331b649
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530982"
---
# <a name="iwmpcdromcollection-vb-and-c-interface"></a><span data-ttu-id="5cc08-105">Interface IWMPCdromCollection (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="5cc08-105">IWMPCdromCollection (VB and C#) interface</span></span>

<span data-ttu-id="5cc08-106">Fournit un moyen d’organiser et d’accéder à une collection de lecteurs de CD ou DVD.</span><span class="sxs-lookup"><span data-stu-id="5cc08-106">Provides a way to organize and access a collection of CD or DVD drives.</span></span>

<span data-ttu-id="5cc08-107">L’interface **IWMPCdromCollection** expose la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="5cc08-107">The **IWMPCdromCollection** interface exposes the following property.</span></span>

## <a name="members"></a><span data-ttu-id="5cc08-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5cc08-108">Members</span></span>

<span data-ttu-id="5cc08-109">L’interface **IWMPCdromCollection (VB et C#)** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5cc08-109">The **IWMPCdromCollection (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="5cc08-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5cc08-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5cc08-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5cc08-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5cc08-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5cc08-112">Methods</span></span>

<span data-ttu-id="5cc08-113">L’interface **IWMPCdromCollection (VB et C#)** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5cc08-113">The **IWMPCdromCollection (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="5cc08-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="5cc08-114">Method</span></span>                                                                                                     | <span data-ttu-id="5cc08-115">Description</span><span class="sxs-lookup"><span data-stu-id="5cc08-115">Description</span></span>                                                                              |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cc08-116">**getByDriveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="5cc08-116">**getByDriveSpecifier**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md) | <span data-ttu-id="5cc08-117">Retourne une interface **IWMPCdrom** associée à une lettre de lecteur particulière.</span><span class="sxs-lookup"><span data-stu-id="5cc08-117">Returns an **IWMPCdrom** interface associated with a particular drive letter.</span></span><br/> |
| [<span data-ttu-id="5cc08-118">**Élément**</span><span class="sxs-lookup"><span data-stu-id="5cc08-118">**Item**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-item--vb-and-c.md)                               | <span data-ttu-id="5cc08-119">Retourne une interface **IWMPCdrom** à l’index donné.</span><span class="sxs-lookup"><span data-stu-id="5cc08-119">Returns an **IWMPCdrom** interface at the given index.</span></span><br/>                        |



 

### <a name="properties"></a><span data-ttu-id="5cc08-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5cc08-120">Properties</span></span>

<span data-ttu-id="5cc08-121">L’interface **IWMPCdromCollection (VB et C#)** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5cc08-121">The **IWMPCdromCollection (VB and C#)** interface has these properties.</span></span>



| <span data-ttu-id="5cc08-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="5cc08-122">Property</span></span>                                                                                  | <span data-ttu-id="5cc08-123">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="5cc08-123">Access type</span></span>          | <span data-ttu-id="5cc08-124">Description</span><span class="sxs-lookup"><span data-stu-id="5cc08-124">Description</span></span>                                                              |
|:------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="5cc08-125">**count**</span><span class="sxs-lookup"><span data-stu-id="5cc08-125">**count**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)<br/> | <span data-ttu-id="5cc08-126">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5cc08-126">Read-only</span></span><br/> | <span data-ttu-id="5cc08-127">Obtient le nombre de lecteurs de CD et de DVD disponibles sur le système.</span><span class="sxs-lookup"><span data-stu-id="5cc08-127">Gets the number of available CD and DVD drives on the system.</span></span><br/> |



 

<span data-ttu-id="5cc08-128">Procurez-vous une interface **IWMPCdromCollection** à l’aide de la propriété suivante.</span><span class="sxs-lookup"><span data-stu-id="5cc08-128">Get an **IWMPCdromCollection** interface by using the following property.</span></span>



| <span data-ttu-id="5cc08-129">Object</span><span class="sxs-lookup"><span data-stu-id="5cc08-129">Object</span></span>                                                                   | <span data-ttu-id="5cc08-130">Propriété</span><span class="sxs-lookup"><span data-stu-id="5cc08-130">Property</span></span>                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cc08-131">Objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="5cc08-131">AxWindowsMediaPlayer Object</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="5cc08-132">**cdromCollection**</span><span class="sxs-lookup"><span data-stu-id="5cc08-132">**cdromCollection**</span></span>](axwmplib-axwindowsmediaplayer-cdromcollection--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="5cc08-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cc08-133">Requirements</span></span>



| <span data-ttu-id="5cc08-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cc08-134">Requirement</span></span> | <span data-ttu-id="5cc08-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cc08-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5cc08-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5cc08-136">Header</span></span><br/> | <dl> <span data-ttu-id="5cc08-137"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cc08-137"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5cc08-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cc08-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cc08-139">**Interfaces pour Visual Basic .NET et C #**</span><span class="sxs-lookup"><span data-stu-id="5cc08-139">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="5cc08-140">**Interface IWMPCdrom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="5cc08-140">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> </dl>

 

 





