---
description: Classe de collection
ms.assetid: 2b2a70ff-2b49-44b2-b506-b0b2cc953ec4
title: Collection (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Collection
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: cf9c5fc6b01574b930b7b8b74186243d00fa5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319217"
---
# <a name="collection-object"></a><span data-ttu-id="ee860-103">Collection (objet)</span><span class="sxs-lookup"><span data-stu-id="ee860-103">Collection object</span></span>

<span data-ttu-id="ee860-104">Classe de collection</span><span class="sxs-lookup"><span data-stu-id="ee860-104">Collection Class</span></span>

## <a name="members"></a><span data-ttu-id="ee860-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ee860-105">Members</span></span>

<span data-ttu-id="ee860-106">L’objet **collection** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ee860-106">The **Collection** object has these types of members:</span></span>

-   [<span data-ttu-id="ee860-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee860-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ee860-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ee860-108">Properties</span></span>

<span data-ttu-id="ee860-109">L’objet **collection** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ee860-109">The **Collection** object has these properties.</span></span>



| <span data-ttu-id="ee860-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="ee860-110">Property</span></span>                                           | <span data-ttu-id="ee860-111">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="ee860-111">Access type</span></span>          | <span data-ttu-id="ee860-112">Description</span><span class="sxs-lookup"><span data-stu-id="ee860-112">Description</span></span>                                                |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="ee860-113">**Saut**</span><span class="sxs-lookup"><span data-stu-id="ee860-113">**Count**</span></span>](-wia-icollection-count.md)<br/> | <span data-ttu-id="ee860-114">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee860-114">Read-only</span></span><br/> | <span data-ttu-id="ee860-115">Retourne le nombre de membres de la collection</span><span class="sxs-lookup"><span data-stu-id="ee860-115">Returns the number of members in the collection</span></span><br/> |
| [<span data-ttu-id="ee860-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ee860-116">**Item**</span></span>](-wia-icollection-item.md)<br/>   | <span data-ttu-id="ee860-117">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ee860-117">Read-only</span></span><br/> | <span data-ttu-id="ee860-118">Retourne l’élément spécifié dans la collection</span><span class="sxs-lookup"><span data-stu-id="ee860-118">Returns the specified item in the collection</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="ee860-119">Notes</span><span class="sxs-lookup"><span data-stu-id="ee860-119">Remarks</span></span>

### <a name="creationaccess-functions"></a><span data-ttu-id="ee860-120">Fonctions d’accès de création \\</span><span class="sxs-lookup"><span data-stu-id="ee860-120">Creation\\Access Functions</span></span>

<span data-ttu-id="ee860-121">Utilisez l’une des méthodes suivantes pour récupérer une référence à l’objet :</span><span class="sxs-lookup"><span data-stu-id="ee860-121">Use any of the following to retrieve a reference to the object:</span></span>



[<span data-ttu-id="ee860-122">**GetItemsFromUI**</span><span class="sxs-lookup"><span data-stu-id="ee860-122">**GetItemsFromUI**</span></span>](-wia-iwiadispatchitem-getitemsfromui.md)

[<span data-ttu-id="ee860-123">**Children**</span><span class="sxs-lookup"><span data-stu-id="ee860-123">**Children**</span></span>](-wia-iwiadispatchitem-children.md)

[<span data-ttu-id="ee860-124">**Appareils**</span><span class="sxs-lookup"><span data-stu-id="ee860-124">**Devices**</span></span>](-wia-iwia-devices.md)



 

## <a name="requirements"></a><span data-ttu-id="ee860-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee860-125">Requirements</span></span>



| <span data-ttu-id="ee860-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee860-126">Requirement</span></span> | <span data-ttu-id="ee860-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee860-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee860-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee860-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ee860-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee860-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ee860-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee860-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ee860-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee860-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ee860-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ee860-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee860-133"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ee860-133"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




