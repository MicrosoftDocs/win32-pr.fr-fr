---
title: Propriété IVMVirtualPC UpTime (VPCCOMInterfaces. h)
description: Récupère le nombre de secondes d’exécution de l’application Windows Virtual PC.
ms.assetid: 3007a961-2e8c-4674-aab6-4424d0d73eca
keywords:
- Virtual PC de la propriété UpTime
- Propriété UpTime Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface Virtual PC, propriété UpTime
topic_type:
- apiref
api_name:
- IVMVirtualPC.UpTime
- IVMVirtualPC.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab07128380a097677e0ad8acca5208e5cef11da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743437"
---
# <a name="ivmvirtualpcuptime-property"></a><span data-ttu-id="a6204-106">IVMVirtualPC :: UpTime, propriété</span><span class="sxs-lookup"><span data-stu-id="a6204-106">IVMVirtualPC::UpTime property</span></span>

<span data-ttu-id="a6204-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a6204-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a6204-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a6204-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a6204-109">Récupère le nombre de secondes d’exécution de l’application Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a6204-109">Retrieves the number of seconds the Windows Virtual PC application has been running.</span></span>

<span data-ttu-id="a6204-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a6204-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6204-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6204-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="a6204-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a6204-112">Property value</span></span>

<span data-ttu-id="a6204-113">Nombre de secondes d’exécution de l’application Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="a6204-113">The number of seconds that the Windows Virtual PC application has been running.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a6204-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="a6204-114">Error codes</span></span>



| <span data-ttu-id="a6204-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="a6204-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="a6204-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a6204-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6204-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a6204-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="a6204-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a6204-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="a6204-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a6204-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="a6204-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a6204-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="a6204-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a6204-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="a6204-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a6204-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="a6204-123"><dt>Ordinateur virtuel \_ \_Virtualisation matérielle E \_ \_ désactivée</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="a6204-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="a6204-124">Le processeur ne prend pas en charge les extensions avez (Hardware Accelerated Virtualization).</span><span class="sxs-lookup"><span data-stu-id="a6204-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a6204-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6204-125">Requirements</span></span>



| <span data-ttu-id="a6204-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6204-126">Requirement</span></span> | <span data-ttu-id="a6204-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6204-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6204-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6204-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a6204-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6204-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6204-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6204-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a6204-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6204-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a6204-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a6204-132">End of client support</span></span><br/>    | <span data-ttu-id="a6204-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6204-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a6204-134">Produit</span><span class="sxs-lookup"><span data-stu-id="a6204-134">Product</span></span><br/>                  | <span data-ttu-id="a6204-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a6204-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a6204-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6204-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6204-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6204-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a6204-138">IID</span><span class="sxs-lookup"><span data-stu-id="a6204-138">IID</span></span><br/>                      | <span data-ttu-id="a6204-139">IID \_ IVMVirtualPC est défini en tant que 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="a6204-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a6204-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6204-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6204-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="a6204-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

