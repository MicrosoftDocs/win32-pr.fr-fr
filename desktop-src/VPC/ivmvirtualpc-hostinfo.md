---
title: IVMVirtualPC HostInfo, propriété (VPCCOMInterfaces. h)
description: Récupère des informations sur l’ordinateur physique.
ms.assetid: 9efefea1-e608-48db-a91a-e3808b420fc2
keywords:
- HostInfo Propriété Virtual PC
- HostInfo, propriété Virtual PC, IVMVirtualPC, interface
- IVMVirtualPC interface Virtual PC, propriété HostInfo
topic_type:
- apiref
api_name:
- IVMVirtualPC.HostInfo
- IVMVirtualPC.get_HostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 351da69a19fd691b037a607a57136576e3b64011
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105196"
---
# <a name="ivmvirtualpchostinfo-property"></a><span data-ttu-id="555fc-106">IVMVirtualPC :: HostInfo, propriété</span><span class="sxs-lookup"><span data-stu-id="555fc-106">IVMVirtualPC::HostInfo property</span></span>

<span data-ttu-id="555fc-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="555fc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="555fc-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="555fc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="555fc-109">Récupère des informations sur l’ordinateur physique.</span><span class="sxs-lookup"><span data-stu-id="555fc-109">Retrieves information about the physical computer.</span></span>

<span data-ttu-id="555fc-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="555fc-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="555fc-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="555fc-111">Syntax</span></span>


```C++
HRESULT get_HostInfo(
  [out, retval] IVMHostInfo **hostInfo
);
```



## <a name="property-value"></a><span data-ttu-id="555fc-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="555fc-112">Property value</span></span>

<span data-ttu-id="555fc-113">Objet [**IVMHostInfo**](ivmhostinfo.md) contenant des informations sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="555fc-113">The [**IVMHostInfo**](ivmhostinfo.md) object containing information about the host machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="555fc-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="555fc-114">Error codes</span></span>



| <span data-ttu-id="555fc-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="555fc-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="555fc-116">Signification</span><span class="sxs-lookup"><span data-stu-id="555fc-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="555fc-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="555fc-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="555fc-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="555fc-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="555fc-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="555fc-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="555fc-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="555fc-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="555fc-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="555fc-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="555fc-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="555fc-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="555fc-123"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="555fc-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="555fc-124">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="555fc-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="555fc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="555fc-125">Requirements</span></span>



| <span data-ttu-id="555fc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="555fc-126">Requirement</span></span> | <span data-ttu-id="555fc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="555fc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="555fc-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="555fc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="555fc-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="555fc-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="555fc-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="555fc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="555fc-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="555fc-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="555fc-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="555fc-132">End of client support</span></span><br/>    | <span data-ttu-id="555fc-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="555fc-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="555fc-134">Produit</span><span class="sxs-lookup"><span data-stu-id="555fc-134">Product</span></span><br/>                  | <span data-ttu-id="555fc-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="555fc-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="555fc-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="555fc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="555fc-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="555fc-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="555fc-138">IID</span><span class="sxs-lookup"><span data-stu-id="555fc-138">IID</span></span><br/>                      | <span data-ttu-id="555fc-139">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="555fc-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="555fc-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="555fc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="555fc-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="555fc-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

