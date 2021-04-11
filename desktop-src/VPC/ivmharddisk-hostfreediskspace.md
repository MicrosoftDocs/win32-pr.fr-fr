---
title: IVMHardDisk HostFreeDiskSpace, propriété (VPCCOMInterfaces. h)
description: Récupère la quantité d’espace disque restant disponible sur l’ordinateur hôte pour le disque dur virtuel.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- HostFreeDiskSpace propriété Virtual PC
- HostFreeDiskSpace, propriété Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, propriété HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105811"
---
# <a name="ivmharddiskhostfreediskspace-property"></a><span data-ttu-id="86950-106">IVMHardDisk :: HostFreeDiskSpace, propriété</span><span class="sxs-lookup"><span data-stu-id="86950-106">IVMHardDisk::HostFreeDiskSpace property</span></span>

<span data-ttu-id="86950-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="86950-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="86950-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="86950-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="86950-109">Récupère la quantité d’espace disque restant disponible sur l’ordinateur hôte pour le disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="86950-109">Retrieves the amount of remaining disk space available on the host for the virtual hard disk.</span></span>

<span data-ttu-id="86950-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="86950-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="86950-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86950-111">Syntax</span></span>


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a><span data-ttu-id="86950-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="86950-112">Property value</span></span>

<span data-ttu-id="86950-113">Quantité d’espace disque restant disponible sur l’ordinateur hôte pour le fichier image de disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="86950-113">The amount of remaining disk space available on the host computer for the current hard disk image file.</span></span> <span data-ttu-id="86950-114">Cette valeur est une **variante** de type VT \_ Decimal.</span><span class="sxs-lookup"><span data-stu-id="86950-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86950-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="86950-115">Error codes</span></span>



| <span data-ttu-id="86950-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="86950-116">Name/value</span></span>                                                                                                                                                                            | <span data-ttu-id="86950-117">Signification</span><span class="sxs-lookup"><span data-stu-id="86950-117">Meaning</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86950-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="86950-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                               | <span data-ttu-id="86950-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="86950-119">The operation was successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="86950-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="86950-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                 | <span data-ttu-id="86950-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="86950-121">The parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="86950-122">Valeur <dt>HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="86950-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl> | <span data-ttu-id="86950-123">Le chemin d’accès au fichier de disque dur virtuel actuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="86950-123">The path to the current virtual hard disk file is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="86950-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="86950-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                         | <span data-ttu-id="86950-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="86950-125">An unexpected error has occurred.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="86950-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86950-126">Requirements</span></span>



| <span data-ttu-id="86950-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86950-127">Requirement</span></span> | <span data-ttu-id="86950-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="86950-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="86950-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86950-129">Minimum supported client</span></span><br/> | <span data-ttu-id="86950-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86950-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="86950-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86950-131">Minimum supported server</span></span><br/> | <span data-ttu-id="86950-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="86950-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="86950-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="86950-133">End of client support</span></span><br/>    | <span data-ttu-id="86950-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="86950-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="86950-135">Produit</span><span class="sxs-lookup"><span data-stu-id="86950-135">Product</span></span><br/>                  | <span data-ttu-id="86950-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="86950-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="86950-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="86950-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="86950-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="86950-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="86950-139">IID</span><span class="sxs-lookup"><span data-stu-id="86950-139">IID</span></span><br/>                      | <span data-ttu-id="86950-140">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="86950-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="86950-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86950-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86950-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="86950-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

