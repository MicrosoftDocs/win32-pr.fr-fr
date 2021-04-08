---
title: IVMAccountant DiskBytesWritten, propriété (VPCCOMInterfaces. h)
description: Nombre total d’octets écrits par tous les contrôleurs de stockage pour cet ordinateur virtuel.
ms.assetid: a2a5730b-a411-48b8-aca8-d09cf09432a9
keywords:
- DiskBytesWritten propriété Virtual PC
- DiskBytesWritten, propriété Virtual PC, IVMAccountant, interface
- IVMAccountant interface Virtual PC, propriété DiskBytesWritten
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesWritten
- IVMAccountant.get_DiskBytesWritten
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e9ad27acf538af25daec676289df5e7664b169
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844274"
---
# <a name="ivmaccountantdiskbyteswritten-property"></a><span data-ttu-id="7f844-106">IVMAccountant ::D propriété iskBytesWritten</span><span class="sxs-lookup"><span data-stu-id="7f844-106">IVMAccountant::DiskBytesWritten property</span></span>

<span data-ttu-id="7f844-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7f844-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7f844-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7f844-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7f844-109">Récupère le nombre total d’octets écrits par tous les contrôleurs de stockage pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7f844-109">Retrieves the total number of bytes written by all storage controllers for this virtual machine.</span></span>

<span data-ttu-id="7f844-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="7f844-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f844-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f844-111">Syntax</span></span>


```C++
HRESULT get_DiskBytesWritten(
  [out, retval] VARIANT *bytesWritten
);
```



## <a name="property-value"></a><span data-ttu-id="7f844-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7f844-112">Property value</span></span>

<span data-ttu-id="7f844-113">Nombre total d'octets lus.</span><span class="sxs-lookup"><span data-stu-id="7f844-113">The total number of bytes.</span></span> <span data-ttu-id="7f844-114">Ces données sont retournées sous la forme d’un **Variant** de type **VT \_ Decimal**.</span><span class="sxs-lookup"><span data-stu-id="7f844-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7f844-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7f844-115">Error codes</span></span>



| <span data-ttu-id="7f844-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="7f844-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7f844-117">Signification</span><span class="sxs-lookup"><span data-stu-id="7f844-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7f844-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7f844-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7f844-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="7f844-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="7f844-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7f844-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7f844-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7f844-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="7f844-122"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7f844-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="7f844-123">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7f844-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="7f844-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7f844-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7f844-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="7f844-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="7f844-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7f844-126">Remarks</span></span>

<span data-ttu-id="7f844-127">Notez que les statistiques d’e/s disque sont réinitialisées à zéro lorsqu’une machine virtuelle est mise sous tension, réinitialisée ou restaurée à partir de l’état enregistré.</span><span class="sxs-lookup"><span data-stu-id="7f844-127">Note that disk I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f844-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f844-128">Requirements</span></span>



| <span data-ttu-id="7f844-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f844-129">Requirement</span></span> | <span data-ttu-id="7f844-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f844-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f844-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f844-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7f844-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f844-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f844-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f844-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7f844-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f844-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7f844-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7f844-135">End of client support</span></span><br/>    | <span data-ttu-id="7f844-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7f844-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7f844-137">Produit</span><span class="sxs-lookup"><span data-stu-id="7f844-137">Product</span></span><br/>                  | <span data-ttu-id="7f844-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7f844-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7f844-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f844-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f844-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f844-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7f844-141">IID</span><span class="sxs-lookup"><span data-stu-id="7f844-141">IID</span></span><br/>                      | <span data-ttu-id="7f844-142">IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="7f844-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="7f844-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f844-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f844-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="7f844-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

