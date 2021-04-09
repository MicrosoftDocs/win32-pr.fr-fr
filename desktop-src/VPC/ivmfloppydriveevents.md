---
title: Interface IVMFloppyDriveEvents (VPCCOMInterfaces. h)
description: Définit l’interface d’événements sortants pour l’interface IVMFloppyDrive. Le client implémente ces méthodes pour recevoir les événements envoyés par IVMFloppyDrive.
ms.assetid: fbb66554-f042-4891-94be-1a12b8c179c2
keywords:
- Virtual PC de l’interface IVMFloppyDriveEvents
- IVMFloppyDriveEvents interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f9b799bd6227882c2991f9b310f39d38b20692d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106060"
---
# <a name="ivmfloppydriveevents-interface"></a><span data-ttu-id="dcdab-106">Interface IVMFloppyDriveEvents</span><span class="sxs-lookup"><span data-stu-id="dcdab-106">IVMFloppyDriveEvents interface</span></span>

<span data-ttu-id="dcdab-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="dcdab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="dcdab-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="dcdab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="dcdab-109">Définit l’interface d’événements sortants pour l’interface [**IVMFloppyDrive**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="dcdab-109">Defines the outgoing event interface for the [**IVMFloppyDrive**](ivmfloppydrive.md) interface.</span></span> <span data-ttu-id="dcdab-110">Le client implémente ces méthodes pour recevoir les événements envoyés par **IVMFloppyDrive**.</span><span class="sxs-lookup"><span data-stu-id="dcdab-110">The client implements these methods to receive events sent from **IVMFloppyDrive**.</span></span>

## <a name="members"></a><span data-ttu-id="dcdab-111">Membres</span><span class="sxs-lookup"><span data-stu-id="dcdab-111">Members</span></span>

<span data-ttu-id="dcdab-112">L’interface **IVMFloppyDriveEvents** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="dcdab-112">The **IVMFloppyDriveEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="dcdab-113">**IVMFloppyDriveEvents** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dcdab-113">**IVMFloppyDriveEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="dcdab-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dcdab-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dcdab-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dcdab-115">Methods</span></span>

<span data-ttu-id="dcdab-116">L’interface **IVMFloppyDriveEvents** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="dcdab-116">The **IVMFloppyDriveEvents** interface has these methods.</span></span>



| <span data-ttu-id="dcdab-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="dcdab-117">Method</span></span>                                                      | <span data-ttu-id="dcdab-118">Description</span><span class="sxs-lookup"><span data-stu-id="dcdab-118">Description</span></span>                                                                   |
|:------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="dcdab-119">**OnMediaEject**</span><span class="sxs-lookup"><span data-stu-id="dcdab-119">**OnMediaEject**</span></span>](ivmfloppydriveevents-onmediaeject.md)   | <span data-ttu-id="dcdab-120">Reçoit une notification indiquant que le média a été éjecté du lecteur.</span><span class="sxs-lookup"><span data-stu-id="dcdab-120">Receives notification that media has been ejected from the drive.</span></span><br/>  |
| [<span data-ttu-id="dcdab-121">**OnMediaInsert**</span><span class="sxs-lookup"><span data-stu-id="dcdab-121">**OnMediaInsert**</span></span>](ivmfloppydriveevents-onmediainsert.md) | <span data-ttu-id="dcdab-122">Reçoit une notification indiquant que le média a été inséré dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="dcdab-122">Receives notification that media has been inserted into the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dcdab-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dcdab-123">Requirements</span></span>



| <span data-ttu-id="dcdab-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dcdab-124">Requirement</span></span> | <span data-ttu-id="dcdab-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="dcdab-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdab-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcdab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dcdab-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dcdab-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcdab-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcdab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dcdab-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dcdab-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="dcdab-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="dcdab-130">End of client support</span></span><br/>    | <span data-ttu-id="dcdab-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="dcdab-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="dcdab-132">Produit</span><span class="sxs-lookup"><span data-stu-id="dcdab-132">Product</span></span><br/>                  | <span data-ttu-id="dcdab-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="dcdab-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="dcdab-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="dcdab-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcdab-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcdab-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="dcdab-136">IID</span><span class="sxs-lookup"><span data-stu-id="dcdab-136">IID</span></span><br/>                      | <span data-ttu-id="dcdab-137">DIID \_ IVMFloppyDriveEvents est défini comme a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span><span class="sxs-lookup"><span data-stu-id="dcdab-137">DIID\_IVMFloppyDriveEvents is defined as a9ed3401-4e09-4177-86ec-a13bf9fa7d4e</span></span><br/>      |



 

