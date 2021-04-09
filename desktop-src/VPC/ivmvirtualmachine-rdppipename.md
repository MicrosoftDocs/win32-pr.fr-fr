---
title: IVMVirtualMachine RdpPipeName, propriété (VPCCOMInterfaces. h)
description: Récupère le nom du canal nommé de connexion RDP utilisé pour la vidéo et l’entrée.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- RdpPipeName propriété Virtual PC
- RdpPipeName, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété RdpPipeName
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032295"
---
# <a name="ivmvirtualmachinerdppipename-property"></a><span data-ttu-id="f8556-106">IVMVirtualMachine :: RdpPipeName, propriété</span><span class="sxs-lookup"><span data-stu-id="f8556-106">IVMVirtualMachine::RdpPipeName property</span></span>

<span data-ttu-id="f8556-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f8556-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f8556-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f8556-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f8556-109">Récupère le nom du canal nommé de connexion RDP utilisé pour la vidéo et l’entrée.</span><span class="sxs-lookup"><span data-stu-id="f8556-109">Retrieves the name of the RDP connection named pipe used for video and input.</span></span>

<span data-ttu-id="f8556-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f8556-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8556-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8556-111">Syntax</span></span>


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a><span data-ttu-id="f8556-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f8556-112">Property value</span></span>

<span data-ttu-id="f8556-113">Nom de la connexion RDP nommée canal utilisé pour la vidéo et l’entrée.</span><span class="sxs-lookup"><span data-stu-id="f8556-113">Name of the RDP connection named pipe used for video and input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f8556-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f8556-114">Error codes</span></span>

<span data-ttu-id="f8556-115">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f8556-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8556-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8556-116">Otherwise, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="f8556-117">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="f8556-117">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="f8556-118">Signification</span><span class="sxs-lookup"><span data-stu-id="f8556-118">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="f8556-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f8556-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="f8556-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f8556-120">The operation was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="f8556-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f8556-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="f8556-122">Le paramètre RdpPipeName a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f8556-122">The RdpPipeName parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="f8556-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f8556-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="f8556-124">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f8556-124">The virtual machine is not running.</span></span><br/>    |
| <dl> <span data-ttu-id="f8556-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f8556-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="f8556-126">Une erreur inconnue s'est produite.</span><span class="sxs-lookup"><span data-stu-id="f8556-126">An unknown error occurred.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="f8556-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8556-127">Requirements</span></span>



| <span data-ttu-id="f8556-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8556-128">Requirement</span></span> | <span data-ttu-id="f8556-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8556-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8556-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8556-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f8556-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8556-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f8556-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8556-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f8556-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8556-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f8556-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f8556-134">End of client support</span></span><br/>    | <span data-ttu-id="f8556-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8556-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f8556-136">Produit</span><span class="sxs-lookup"><span data-stu-id="f8556-136">Product</span></span><br/>                  | <span data-ttu-id="f8556-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f8556-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f8556-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8556-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8556-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8556-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f8556-140">IID</span><span class="sxs-lookup"><span data-stu-id="f8556-140">IID</span></span><br/>                      | <span data-ttu-id="f8556-141">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="f8556-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f8556-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8556-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8556-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="f8556-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

