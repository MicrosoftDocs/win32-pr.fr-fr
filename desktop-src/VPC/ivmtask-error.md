---
title: Propriété d’erreur IVMTask (VPCCOMInterfaces. h)
description: Récupère l’erreur enregistrée pour cette tâche.
ms.assetid: 9023e24b-679b-43e4-8db4-b8510a582382
keywords:
- Propriété d’erreur Virtual PC
- Propriété d’erreur Virtual PC, interface IVMTask
- IVMTask interface Virtual PC, propriété Error
topic_type:
- apiref
api_name:
- IVMTask.Error
- IVMTask.get_Error
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d75c4748678fb2ba500ae7a772afe9fb4a8147
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510146"
---
# <a name="ivmtaskerror-property"></a><span data-ttu-id="70e0f-106">IVMTask :: Error, propriété</span><span class="sxs-lookup"><span data-stu-id="70e0f-106">IVMTask::Error property</span></span>

<span data-ttu-id="70e0f-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="70e0f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="70e0f-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="70e0f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="70e0f-109">Récupère l’erreur enregistrée pour cette tâche.</span><span class="sxs-lookup"><span data-stu-id="70e0f-109">Retrieves the error recorded for this task.</span></span>

<span data-ttu-id="70e0f-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="70e0f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="70e0f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70e0f-111">Syntax</span></span>


```C++
HRESULT get_Error(
  [out, retval] long *outError
);
```



## <a name="property-value"></a><span data-ttu-id="70e0f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="70e0f-112">Property value</span></span>

<span data-ttu-id="70e0f-113">Erreur enregistrée.</span><span class="sxs-lookup"><span data-stu-id="70e0f-113">The recorded error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="70e0f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="70e0f-114">Error codes</span></span>

<span data-ttu-id="70e0f-115">Les instances de [**IVMTask**](ivmtask.md) retournées par d’autres interfaces peuvent retourner des valeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="70e0f-115">Instances of [**IVMTask**](ivmtask.md) returned by other interfaces may return additional values.</span></span> <span data-ttu-id="70e0f-116">Pour plus d’informations, consultez la documentation des méthodes qui retournent une instance **IVMTask** .</span><span class="sxs-lookup"><span data-stu-id="70e0f-116">For details, see the documentation of the methods that return a **IVMTask** instance.</span></span>



| <span data-ttu-id="70e0f-117">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="70e0f-117">Name/value</span></span>                                                                                                                                                                        | <span data-ttu-id="70e0f-118">Signification</span><span class="sxs-lookup"><span data-stu-id="70e0f-118">Meaning</span></span>                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="70e0f-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="70e0f-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                           | <span data-ttu-id="70e0f-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="70e0f-120">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="70e0f-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="70e0f-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                             | <span data-ttu-id="70e0f-122">La valeur du paramètre est **null**.</span><span class="sxs-lookup"><span data-stu-id="70e0f-122">The parameter value is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="70e0f-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="70e0f-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                     | <span data-ttu-id="70e0f-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="70e0f-124">An unexpected error has occurred.</span></span><br/>                          |
| <dl> <span data-ttu-id="70e0f-125"><dt>Ordinateur virtuel \_ E \_ VMVIRTUALPC \_ plus ancienne \_ version</dt> <dt>0xA0040952</dt></span><span class="sxs-lookup"><span data-stu-id="70e0f-125"><dt>VM\_E\_VMVIRTUALPC\_OLDER\_VERSION</dt> <dt>0xA0040952</dt></span></span> </dl>     | <span data-ttu-id="70e0f-126">Virtual PC 2007 et Windows Virtual PC sont tous deux installés.</span><span class="sxs-lookup"><span data-stu-id="70e0f-126">Both Virtual PC 2007 and Windows Virtual PC are installed.</span></span><br/> |
| <dl> <span data-ttu-id="70e0f-127"><dt>Ordinateur virtuel \_ 0xA0040953 d' \_ autres \_ \_ logiciels de virtualisation</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70e0f-127"><dt>VM\_E\_OTHER\_VIRTUALIZATION\_SOFTWARE</dt> <dt>0xA0040953</dt></span></span> </dl> | <span data-ttu-id="70e0f-128">D’autres logiciels de virtualisation sont installés.</span><span class="sxs-lookup"><span data-stu-id="70e0f-128">Other virtualization software is installed.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="70e0f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70e0f-129">Requirements</span></span>



| <span data-ttu-id="70e0f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70e0f-130">Requirement</span></span> | <span data-ttu-id="70e0f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="70e0f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="70e0f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70e0f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="70e0f-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70e0f-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70e0f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70e0f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="70e0f-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="70e0f-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="70e0f-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="70e0f-136">End of client support</span></span><br/>    | <span data-ttu-id="70e0f-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="70e0f-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="70e0f-138">Produit</span><span class="sxs-lookup"><span data-stu-id="70e0f-138">Product</span></span><br/>                  | <span data-ttu-id="70e0f-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="70e0f-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="70e0f-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="70e0f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e0f-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e0f-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="70e0f-142">IID</span><span class="sxs-lookup"><span data-stu-id="70e0f-142">IID</span></span><br/>                      | <span data-ttu-id="70e0f-143">IID \_ IVMTask est défini en tant que ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="70e0f-143">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="70e0f-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70e0f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70e0f-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="70e0f-145">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

