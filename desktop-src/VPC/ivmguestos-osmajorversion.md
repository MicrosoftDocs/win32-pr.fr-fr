---
title: IVMGuestOS OSMajorVersion, propriété (VPCCOMInterfaces. h)
description: Version principale du système d’exploitation invité en cours d’exécution sur la machine virtuelle.
ms.assetid: c9be8b4e-15fe-402d-8396-30be6b065b73
keywords:
- OSMajorVersion propriété Virtual PC
- OSMajorVersion, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété OSMajorVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMajorVersion
- IVMGuestOS.get_OSMajorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f76e3105c4917141c8a5304082d55f383ee947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465202"
---
# <a name="ivmguestososmajorversion-property"></a><span data-ttu-id="22ab2-106">IVMGuestOS :: OSMajorVersion, propriété</span><span class="sxs-lookup"><span data-stu-id="22ab2-106">IVMGuestOS::OSMajorVersion property</span></span>

<span data-ttu-id="22ab2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="22ab2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="22ab2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="22ab2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="22ab2-109">Récupère la version principale du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="22ab2-109">Retrieves the major version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="22ab2-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="22ab2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="22ab2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22ab2-111">Syntax</span></span>


```C++
HRESULT get_OSMajorVersion(
  [out, retval] BSTR *majorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="22ab2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="22ab2-112">Property value</span></span>

<span data-ttu-id="22ab2-113">Version principale.</span><span class="sxs-lookup"><span data-stu-id="22ab2-113">The major version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="22ab2-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="22ab2-114">Error codes</span></span>



| <span data-ttu-id="22ab2-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="22ab2-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="22ab2-116">Signification</span><span class="sxs-lookup"><span data-stu-id="22ab2-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="22ab2-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="22ab2-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="22ab2-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="22ab2-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="22ab2-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="22ab2-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="22ab2-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="22ab2-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="22ab2-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="22ab2-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="22ab2-122">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22ab2-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="22ab2-123"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="22ab2-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="22ab2-124">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="22ab2-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="22ab2-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="22ab2-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="22ab2-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="22ab2-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="22ab2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22ab2-127">Requirements</span></span>



| <span data-ttu-id="22ab2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22ab2-128">Requirement</span></span> | <span data-ttu-id="22ab2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="22ab2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ab2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22ab2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="22ab2-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22ab2-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22ab2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22ab2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="22ab2-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="22ab2-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="22ab2-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="22ab2-134">End of client support</span></span><br/>    | <span data-ttu-id="22ab2-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="22ab2-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="22ab2-136">Produit</span><span class="sxs-lookup"><span data-stu-id="22ab2-136">Product</span></span><br/>                  | <span data-ttu-id="22ab2-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="22ab2-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="22ab2-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="22ab2-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="22ab2-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="22ab2-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="22ab2-140">IID</span><span class="sxs-lookup"><span data-stu-id="22ab2-140">IID</span></span><br/>                      | <span data-ttu-id="22ab2-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="22ab2-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="22ab2-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22ab2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22ab2-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="22ab2-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

