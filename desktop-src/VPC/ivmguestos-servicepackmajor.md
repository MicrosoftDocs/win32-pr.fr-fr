---
title: IVMGuestOS ServicePackMajor, propriété (VPCCOMInterfaces. h)
description: Version principale du Service Pack du système d’exploitation invité en cours d’exécution sur la machine virtuelle.
ms.assetid: 87dbc4cc-8a8d-468f-9a29-e5047029b032
keywords:
- ServicePackMajor propriété Virtual PC
- ServicePackMajor, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété ServicePackMajor
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMajor
- IVMGuestOS.get_ServicePackMajor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1fa89b51e26354ce2983ad42025b1b9a3922d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104110"
---
# <a name="ivmguestosservicepackmajor-property"></a><span data-ttu-id="b9872-106">IVMGuestOS :: ServicePackMajor, propriété</span><span class="sxs-lookup"><span data-stu-id="b9872-106">IVMGuestOS::ServicePackMajor property</span></span>

<span data-ttu-id="b9872-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b9872-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b9872-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b9872-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b9872-109">Version principale du Service Pack du système d’exploitation invité en cours d’exécution sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b9872-109">The major version of the service pack of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="b9872-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b9872-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9872-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9872-111">Syntax</span></span>


```C++
HRESULT get_ServicePackMajor(
  [out, retval] BSTR *servicePackMajor
);
```



## <a name="property-value"></a><span data-ttu-id="b9872-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b9872-112">Property value</span></span>

<span data-ttu-id="b9872-113">Numéro de version principale du dernier Service Pack installé.</span><span class="sxs-lookup"><span data-stu-id="b9872-113">The major version number of the latest Service Pack installed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b9872-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b9872-114">Error codes</span></span>



| <span data-ttu-id="b9872-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="b9872-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="b9872-116">Signification</span><span class="sxs-lookup"><span data-stu-id="b9872-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b9872-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b9872-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="b9872-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b9872-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="b9872-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b9872-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="b9872-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b9872-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="b9872-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b9872-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="b9872-122">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b9872-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="b9872-123"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="b9872-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="b9872-124">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b9872-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="b9872-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b9872-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="b9872-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b9872-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="b9872-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9872-127">Requirements</span></span>



| <span data-ttu-id="b9872-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9872-128">Requirement</span></span> | <span data-ttu-id="b9872-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9872-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9872-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9872-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b9872-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9872-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9872-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9872-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b9872-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9872-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b9872-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b9872-134">End of client support</span></span><br/>    | <span data-ttu-id="b9872-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9872-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b9872-136">Produit</span><span class="sxs-lookup"><span data-stu-id="b9872-136">Product</span></span><br/>                  | <span data-ttu-id="b9872-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b9872-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b9872-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9872-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9872-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9872-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b9872-140">IID</span><span class="sxs-lookup"><span data-stu-id="b9872-140">IID</span></span><br/>                      | <span data-ttu-id="b9872-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="b9872-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b9872-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9872-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9872-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="b9872-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

