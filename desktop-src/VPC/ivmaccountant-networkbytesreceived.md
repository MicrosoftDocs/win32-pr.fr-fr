---
title: IVMAccountant NetworkBytesReceived, propriété (VPCCOMInterfaces. h)
description: Nombre total d’octets reçus par toutes les cartes réseau virtuelles de cet ordinateur virtuel.
ms.assetid: 6f6b32e6-d99b-405c-a788-ed646b3a7593
keywords:
- NetworkBytesReceived propriété Virtual PC
- NetworkBytesReceived, propriété Virtual PC, IVMAccountant, interface
- IVMAccountant interface Virtual PC, propriété NetworkBytesReceived
topic_type:
- apiref
api_name:
- IVMAccountant.NetworkBytesReceived
- IVMAccountant.get_NetworkBytesReceived
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e14d7454516ff4e83771744c74f31ee594aa67f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466839"
---
# <a name="ivmaccountantnetworkbytesreceived-property"></a><span data-ttu-id="01811-106">IVMAccountant :: NetworkBytesReceived, propriété</span><span class="sxs-lookup"><span data-stu-id="01811-106">IVMAccountant::NetworkBytesReceived property</span></span>

<span data-ttu-id="01811-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="01811-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="01811-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="01811-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="01811-109">Récupère le nombre total d’octets reçus par toutes les cartes réseau virtuelles de cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="01811-109">Retrieves the total number of bytes received by all virtual network adapters for this virtual machine.</span></span>

<span data-ttu-id="01811-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="01811-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="01811-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01811-111">Syntax</span></span>


```C++
HRESULT get_NetworkBytesReceived(
  [out, retval] VARIANT *bytesReceived
);
```



## <a name="property-value"></a><span data-ttu-id="01811-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="01811-112">Property value</span></span>

<span data-ttu-id="01811-113">Nombre total d’octets reçus.</span><span class="sxs-lookup"><span data-stu-id="01811-113">The total number of bytes received.</span></span> <span data-ttu-id="01811-114">Ces données sont retournées sous la forme d’un **Variant** de type **VT \_ Decimal**.</span><span class="sxs-lookup"><span data-stu-id="01811-114">This data is returned as a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="01811-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="01811-115">Error codes</span></span>



| <span data-ttu-id="01811-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="01811-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="01811-117">Signification</span><span class="sxs-lookup"><span data-stu-id="01811-117">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="01811-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="01811-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="01811-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="01811-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="01811-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="01811-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="01811-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="01811-121">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="01811-122"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="01811-122"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="01811-123">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="01811-123">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="01811-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="01811-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="01811-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="01811-125">An unexpected error has occurred.</span></span><br/>   |



## <a name="remarks"></a><span data-ttu-id="01811-126">Notes</span><span class="sxs-lookup"><span data-stu-id="01811-126">Remarks</span></span>

<span data-ttu-id="01811-127">Notez que les statistiques d’e/s réseau sont réinitialisées à zéro lorsqu’une machine virtuelle est mise sous tension, réinitialisée ou restaurée à partir de l’état enregistré.</span><span class="sxs-lookup"><span data-stu-id="01811-127">Note that network I/O statistics are reset to zero when a virtual machine is powered up, reset, or restored from saved state.</span></span>

## <a name="requirements"></a><span data-ttu-id="01811-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01811-128">Requirements</span></span>



| <span data-ttu-id="01811-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01811-129">Requirement</span></span> | <span data-ttu-id="01811-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="01811-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="01811-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01811-131">Minimum supported client</span></span><br/> | <span data-ttu-id="01811-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01811-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="01811-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01811-133">Minimum supported server</span></span><br/> | <span data-ttu-id="01811-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="01811-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="01811-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="01811-135">End of client support</span></span><br/>    | <span data-ttu-id="01811-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="01811-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="01811-137">Produit</span><span class="sxs-lookup"><span data-stu-id="01811-137">Product</span></span><br/>                  | <span data-ttu-id="01811-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="01811-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="01811-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="01811-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="01811-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="01811-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="01811-141">IID</span><span class="sxs-lookup"><span data-stu-id="01811-141">IID</span></span><br/>                      | <span data-ttu-id="01811-142">IID \_ IVMAccountant est défini en tant que 6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="01811-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="01811-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01811-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01811-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="01811-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

