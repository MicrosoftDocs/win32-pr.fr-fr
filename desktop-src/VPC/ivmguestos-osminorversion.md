---
title: IVMGuestOS OSMinorVersion, propriété (VPCCOMInterfaces. h)
description: Version mineure du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- OSMinorVersion propriété Virtual PC
- OSMinorVersion, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété OSMinorVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c068ee6d8112561f57d0644f6bc7bc4844096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509525"
---
# <a name="ivmguestososminorversion-property"></a><span data-ttu-id="69bfe-106">IVMGuestOS :: OSMinorVersion, propriété</span><span class="sxs-lookup"><span data-stu-id="69bfe-106">IVMGuestOS::OSMinorVersion property</span></span>

<span data-ttu-id="69bfe-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="69bfe-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="69bfe-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="69bfe-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="69bfe-109">Récupère la version mineure du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="69bfe-109">Retrieves the minor version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="69bfe-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="69bfe-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="69bfe-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69bfe-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="69bfe-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="69bfe-112">Property value</span></span>

<span data-ttu-id="69bfe-113">Version mineure.</span><span class="sxs-lookup"><span data-stu-id="69bfe-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="69bfe-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="69bfe-114">Error codes</span></span>



| <span data-ttu-id="69bfe-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="69bfe-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="69bfe-116">Signification</span><span class="sxs-lookup"><span data-stu-id="69bfe-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="69bfe-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="69bfe-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="69bfe-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="69bfe-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="69bfe-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="69bfe-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="69bfe-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="69bfe-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="69bfe-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="69bfe-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="69bfe-122">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="69bfe-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="69bfe-123"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="69bfe-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="69bfe-124">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="69bfe-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="69bfe-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="69bfe-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="69bfe-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="69bfe-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="69bfe-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69bfe-127">Requirements</span></span>



| <span data-ttu-id="69bfe-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69bfe-128">Requirement</span></span> | <span data-ttu-id="69bfe-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="69bfe-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="69bfe-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69bfe-130">Minimum supported client</span></span><br/> | <span data-ttu-id="69bfe-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69bfe-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="69bfe-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69bfe-132">Minimum supported server</span></span><br/> | <span data-ttu-id="69bfe-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="69bfe-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="69bfe-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="69bfe-134">End of client support</span></span><br/>    | <span data-ttu-id="69bfe-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69bfe-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="69bfe-136">Produit</span><span class="sxs-lookup"><span data-stu-id="69bfe-136">Product</span></span><br/>                  | <span data-ttu-id="69bfe-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="69bfe-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="69bfe-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="69bfe-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="69bfe-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="69bfe-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="69bfe-140">IID</span><span class="sxs-lookup"><span data-stu-id="69bfe-140">IID</span></span><br/>                      | <span data-ttu-id="69bfe-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="69bfe-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="69bfe-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69bfe-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69bfe-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="69bfe-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

