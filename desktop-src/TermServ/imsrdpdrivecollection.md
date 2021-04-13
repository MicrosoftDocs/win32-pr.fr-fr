---
title: Interface IMsRdpDriveCollection
description: Représente une collection d’objets Drive.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDriveCollection
- Services Bureau à distance de l’interface IMsRdpDriveCollection, Description
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465987"
---
# <a name="imsrdpdrivecollection-interface"></a><span data-ttu-id="fb9ed-105">Interface IMsRdpDriveCollection</span><span class="sxs-lookup"><span data-stu-id="fb9ed-105">IMsRdpDriveCollection interface</span></span>

<span data-ttu-id="fb9ed-106">Représente une collection d’objets Drive.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-106">Represents a collection of drive objects.</span></span>

## <a name="members"></a><span data-ttu-id="fb9ed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="fb9ed-107">Members</span></span>

<span data-ttu-id="fb9ed-108">L’interface **IMsRdpDriveCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fb9ed-108">The **IMsRdpDriveCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fb9ed-109">**IMsRdpDriveCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fb9ed-109">**IMsRdpDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="fb9ed-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb9ed-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="fb9ed-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb9ed-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fb9ed-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="fb9ed-112">Methods</span></span>

<span data-ttu-id="fb9ed-113">L’interface **IMsRdpDriveCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-113">The **IMsRdpDriveCollection** interface has these methods.</span></span>



| <span data-ttu-id="fb9ed-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="fb9ed-114">Method</span></span>                                                     | <span data-ttu-id="fb9ed-115">Description</span><span class="sxs-lookup"><span data-stu-id="fb9ed-115">Description</span></span>                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="fb9ed-116">**RescanDrives**</span><span class="sxs-lookup"><span data-stu-id="fb9ed-116">**RescanDrives**</span></span>](imsrdpdrivecollection-rescandrives.md) | <span data-ttu-id="fb9ed-117">Actualise la liste des objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fb9ed-118">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fb9ed-118">Properties</span></span>

<span data-ttu-id="fb9ed-119">L’interface **IMsRdpDriveCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-119">The **IMsRdpDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="fb9ed-120">Propriété</span><span class="sxs-lookup"><span data-stu-id="fb9ed-120">Property</span></span>                                                              | <span data-ttu-id="fb9ed-121">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="fb9ed-121">Access type</span></span>          | <span data-ttu-id="fb9ed-122">Description</span><span class="sxs-lookup"><span data-stu-id="fb9ed-122">Description</span></span>                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="fb9ed-123">**DriveByIndex**</span><span class="sxs-lookup"><span data-stu-id="fb9ed-123">**DriveByIndex**</span></span>](imsrdpdrivecollection-drivebyindex.md)<br/> | <span data-ttu-id="fb9ed-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb9ed-124">Read-only</span></span><br/> | <span data-ttu-id="fb9ed-125">Récupère le lecteur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-125">Retrieves the drive at the specified index.</span></span><br/>       |
| [<span data-ttu-id="fb9ed-126">**DriveCount**</span><span class="sxs-lookup"><span data-stu-id="fb9ed-126">**DriveCount**</span></span>](imsrdpdrivecollection-drivecount.md)<br/>     | <span data-ttu-id="fb9ed-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fb9ed-127">Read-only</span></span><br/> | <span data-ttu-id="fb9ed-128">Récupère le nombre d’objets dans la collection.</span><span class="sxs-lookup"><span data-stu-id="fb9ed-128">Retrieves the count of objects in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fb9ed-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb9ed-129">Requirements</span></span>



| <span data-ttu-id="fb9ed-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb9ed-130">Requirement</span></span> | <span data-ttu-id="fb9ed-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb9ed-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9ed-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb9ed-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9ed-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb9ed-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="fb9ed-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb9ed-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9ed-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb9ed-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fb9ed-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fb9ed-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb9ed-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb9ed-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="fb9ed-138">DLL</span><span class="sxs-lookup"><span data-stu-id="fb9ed-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb9ed-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb9ed-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="fb9ed-140">IID</span><span class="sxs-lookup"><span data-stu-id="fb9ed-140">IID</span></span><br/>                      | <span data-ttu-id="fb9ed-141">IID \_ IMsRdpDriveCollection est défini en tant que 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="fb9ed-141">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb9ed-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb9ed-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9ed-143">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="fb9ed-143">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="fb9ed-144">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="fb9ed-144">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

