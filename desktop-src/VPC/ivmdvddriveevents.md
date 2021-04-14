---
title: Interface IVMDVDDriveEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMDVDDrive.
ms.assetid: aa68fb6f-032d-4322-8553-b1e840ae63b8
keywords:
- Virtual PC de l’interface IVMDVDDriveEvents
- IVMDVDDriveEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b301a423f5272288c12a900d0fbd19c0a5d5170
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466838"
---
# <a name="ivmdvddriveevents-interface"></a><span data-ttu-id="4c2c4-105">Interface IVMDVDDriveEvents</span><span class="sxs-lookup"><span data-stu-id="4c2c4-105">IVMDVDDriveEvents interface</span></span>

<span data-ttu-id="4c2c4-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4c2c4-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4c2c4-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4c2c4-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4c2c4-108">Définit l’interface d’événements sortants pour l’interface [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="4c2c4-108">Defines the outgoing event interface for the [**IVMDVDDrive**](ivmdvddrive.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4c2c4-109">Membres</span><span class="sxs-lookup"><span data-stu-id="4c2c4-109">Members</span></span>

<span data-ttu-id="4c2c4-110">L’interface **IVMDVDDriveEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4c2c4-110">The **IVMDVDDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4c2c4-111">**IVMDVDDriveEvents** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4c2c4-111">**IVMDVDDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="4c2c4-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c2c4-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4c2c4-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4c2c4-113">Methods</span></span>

<span data-ttu-id="4c2c4-114">L’interface **IVMDVDDriveEvents** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4c2c4-114">The **IVMDVDDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="4c2c4-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="4c2c4-115">Method</span></span>                                                   | <span data-ttu-id="4c2c4-116">Description</span><span class="sxs-lookup"><span data-stu-id="4c2c4-116">Description</span></span>                                                                   |
|:---------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="4c2c4-117">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="4c2c4-117">**OnMediaEject**</span></span>](ivmdvddriveevents-onmediaeject.md)   | <span data-ttu-id="4c2c4-118">Reçoit une notification indiquant que le média a été éjecté du lecteur.</span><span class="sxs-lookup"><span data-stu-id="4c2c4-118">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="4c2c4-119">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="4c2c4-119">**OnMediaInsert**</span></span>](ivmdvddriveevents-onmediainsert.md) | <span data-ttu-id="4c2c4-120">Reçoit une notification indiquant que le média a été inséré dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="4c2c4-120">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4c2c4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c2c4-121">Requirements</span></span>



| <span data-ttu-id="4c2c4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c2c4-122">Requirement</span></span> | <span data-ttu-id="4c2c4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c2c4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c2c4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c2c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4c2c4-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c2c4-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c2c4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c2c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4c2c4-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c2c4-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4c2c4-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="4c2c4-128">End of client support</span></span><br/>    | <span data-ttu-id="4c2c4-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c2c4-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4c2c4-130">Produit</span><span class="sxs-lookup"><span data-stu-id="4c2c4-130">Product</span></span><br/>                  | <span data-ttu-id="4c2c4-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4c2c4-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4c2c4-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c2c4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c2c4-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c2c4-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4c2c4-134">IID</span><span class="sxs-lookup"><span data-stu-id="4c2c4-134">IID</span></span><br/>                      | <span data-ttu-id="4c2c4-135">DIID \_ IVMDVDDriveEvents est défini comme c2a7d8e9-E76C-4EB8-94f7-71a5122d249b</span><span class="sxs-lookup"><span data-stu-id="4c2c4-135">DIID\_IVMDVDDriveEvents is defined as c2a7d8e9-e76c-4eb8-94f7-71a5122d249b</span></span><br/>         |



 

