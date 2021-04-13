---
title: IVMGuestOS OSName, propriété (VPCCOMInterfaces. h)
description: Nom du système d’exploitation invité en cours d’exécution sur la machine virtuelle.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- OSName propriété Virtual PC
- OSName, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété OSName
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672c7b2c852bcbb1ec39b61889b03738e3a2df23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465199"
---
# <a name="ivmguestososname-property"></a><span data-ttu-id="d5672-106">IVMGuestOS :: OSName, propriété</span><span class="sxs-lookup"><span data-stu-id="d5672-106">IVMGuestOS::OSName property</span></span>

<span data-ttu-id="d5672-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d5672-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d5672-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d5672-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d5672-109">Récupère le nom du système d’exploitation invité en cours d’exécution sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d5672-109">Retrieves the name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="d5672-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d5672-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5672-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5672-111">Syntax</span></span>


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a><span data-ttu-id="d5672-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d5672-112">Property value</span></span>

<span data-ttu-id="d5672-113">Nom complet (y compris le nom de la suite) du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="d5672-113">The full name (including suite name) of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d5672-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d5672-114">Error codes</span></span>



| <span data-ttu-id="d5672-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="d5672-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="d5672-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d5672-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d5672-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d5672-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="d5672-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d5672-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="d5672-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d5672-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="d5672-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="d5672-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="d5672-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d5672-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="d5672-122">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d5672-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="d5672-123"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="d5672-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="d5672-124">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d5672-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d5672-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d5672-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="d5672-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d5672-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="d5672-127">Notes</span><span class="sxs-lookup"><span data-stu-id="d5672-127">Remarks</span></span>

<span data-ttu-id="d5672-128">La machine virtuelle doit être en cours d’exécution (c’est-à-dire être entièrement amorcée et ne pas s’arrêter) et des composants d’intégration doivent être installés lorsque cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="d5672-128">The VM must be running (that is, fully booted and not shutting down) and integration components must be installed when this method is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5672-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5672-129">Requirements</span></span>



| <span data-ttu-id="d5672-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5672-130">Requirement</span></span> | <span data-ttu-id="d5672-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5672-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5672-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5672-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d5672-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5672-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d5672-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5672-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d5672-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5672-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d5672-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d5672-136">End of client support</span></span><br/>    | <span data-ttu-id="d5672-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5672-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d5672-138">Produit</span><span class="sxs-lookup"><span data-stu-id="d5672-138">Product</span></span><br/>                  | <span data-ttu-id="d5672-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d5672-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d5672-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5672-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5672-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5672-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d5672-142">IID</span><span class="sxs-lookup"><span data-stu-id="d5672-142">IID</span></span><br/>                      | <span data-ttu-id="d5672-143">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="d5672-143">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d5672-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5672-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5672-145">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="d5672-145">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

