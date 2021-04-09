---
title: IVMAccountant NetworkBytesSent, propriété (VPCCOMInterfaces. h)
description: Nombre total d’octets envoyés par toutes les cartes réseau virtuelles pour cet ordinateur virtuel.
ms.assetid: 3b5c3fa2-48c6-46c8-bbb6-5d1a9769308a
keywords:
- NetworkBytesSent propriété Virtual PC
- NetworkBytesSent, propriété Virtual PC, IVMAccountant, interface
- IVMAccountant interface Virtual PC, propriété NetworkBytesSent
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesSent
- IVMAccountant.get_NetworkBytesSent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d25a6c0a9ee784af8bfab196fc9aaef0d1474d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942222"
---
# <a name="ivmaccountantnetworkbytessent-property"></a><span data-ttu-id="2b38e-106">IVMAccountant :: NetworkBytesSent, propriété</span><span class="sxs-lookup"><span data-stu-id="2b38e-106">IVMAccountant::NetworkBytesSent property</span></span>

<span data-ttu-id="2b38e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2b38e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2b38e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2b38e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2b38e-109">Récupère le nombre total d’octets envoyés par toutes les cartes réseau virtuelles pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2b38e-109">Retrieves the total number of bytes sent by all virtual network adapters for this virtual machine.</span></span>

<span data-ttu-id="2b38e-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2b38e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b38e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2b38e-111">Syntax</span></span>


```C++
HRESULT get_NetworkBytesSent(
  [out, retval] VARIANT *bytesSent
);
```



## <a name="property-value"></a><span data-ttu-id="2b38e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2b38e-112">Property value</span></span>

<span data-ttu-id="2b38e-113">Nombre total d’octets envoyés par toutes les cartes d’interface réseau virtuelle pour cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2b38e-113">The total number of bytes sent by all virtual network interface cards for this virtual machine.</span></span> <span data-ttu-id="2b38e-114">Elle est retournée en tant que **Variant** de type **VT \_ Decimal**.</span><span class="sxs-lookup"><span data-stu-id="2b38e-114">It is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2b38e-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2b38e-115">Error codes</span></span>



| <span data-ttu-id="2b38e-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="2b38e-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="2b38e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="2b38e-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="2b38e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2b38e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="2b38e-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2b38e-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="2b38e-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2b38e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="2b38e-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2b38e-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="2b38e-122"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2b38e-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="2b38e-123">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2b38e-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="2b38e-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2b38e-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="2b38e-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2b38e-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="2b38e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2b38e-126">Remarks</span></span>

<span data-ttu-id="2b38e-127">Notez que les statistiques d’e/s réseau sont réinitialisées à zéro lorsqu’une machine virtuelle est mise sous tension, réinitialisée ou restaurée à partir de l’état enregistré.</span><span class="sxs-lookup"><span data-stu-id="2b38e-127">Note that network I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b38e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2b38e-128">Requirements</span></span>



| <span data-ttu-id="2b38e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2b38e-129">Requirement</span></span> | <span data-ttu-id="2b38e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="2b38e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b38e-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b38e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="2b38e-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2b38e-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b38e-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b38e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="2b38e-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2b38e-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2b38e-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2b38e-135">End of client support</span></span><br/>    | <span data-ttu-id="2b38e-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2b38e-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2b38e-137">Produit</span><span class="sxs-lookup"><span data-stu-id="2b38e-137">Product</span></span><br/>                  | <span data-ttu-id="2b38e-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2b38e-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2b38e-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="2b38e-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b38e-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b38e-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2b38e-141">IID</span><span class="sxs-lookup"><span data-stu-id="2b38e-141">IID</span></span><br/>                      | <span data-ttu-id="2b38e-142">IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="2b38e-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="2b38e-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b38e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b38e-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="2b38e-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

