---
title: IVMGuestOS CSDVersion, propriété (VPCCOMInterfaces. h)
description: CSDVersion du système d’exploitation invité en cours d’exécution sur la machine virtuelle.
ms.assetid: 6f1d8dd6-6feb-4bdf-a553-631d55c18076
keywords:
- CSDVersion propriété Virtual PC
- CSDVersion, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété CSDVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.CSDVersion
- IVMGuestOS.get_CSDVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d82b3939f581edf328902f7fd0a26e1916abe1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942784"
---
# <a name="ivmguestoscsdversion-property"></a><span data-ttu-id="acfef-106">IVMGuestOS :: CSDVersion, propriété</span><span class="sxs-lookup"><span data-stu-id="acfef-106">IVMGuestOS::CSDVersion property</span></span>

<span data-ttu-id="acfef-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="acfef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="acfef-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="acfef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="acfef-109">Récupère le CSDVersion du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="acfef-109">Retrieves the CSDVersion of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="acfef-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="acfef-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="acfef-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acfef-111">Syntax</span></span>


```C++
HRESULT get_CSDVersion(
  [out, retval] BSTR *csdVersion
);
```



## <a name="property-value"></a><span data-ttu-id="acfef-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="acfef-112">Property value</span></span>

<span data-ttu-id="acfef-113">Chaîne terminée par le caractère null, telle que « Service Pack 3 », qui indique le dernier Service Pack installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="acfef-113">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="acfef-114">Si aucun Service Pack n’a été installé, la chaîne est vide.</span><span class="sxs-lookup"><span data-stu-id="acfef-114">If no Service Pack has been installed, the string is empty.</span></span>

## <a name="error-codes"></a><span data-ttu-id="acfef-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="acfef-115">Error codes</span></span>



| <span data-ttu-id="acfef-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="acfef-116">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="acfef-117">Signification</span><span class="sxs-lookup"><span data-stu-id="acfef-117">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="acfef-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="acfef-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="acfef-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="acfef-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="acfef-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="acfef-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="acfef-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="acfef-121">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="acfef-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="acfef-122"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="acfef-123">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="acfef-123">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="acfef-124"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="acfef-124"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="acfef-125">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="acfef-125">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="acfef-126"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="acfef-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="acfef-127">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="acfef-127">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="acfef-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acfef-128">Requirements</span></span>



| <span data-ttu-id="acfef-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acfef-129">Requirement</span></span> | <span data-ttu-id="acfef-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="acfef-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="acfef-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acfef-131">Minimum supported client</span></span><br/> | <span data-ttu-id="acfef-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acfef-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="acfef-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acfef-133">Minimum supported server</span></span><br/> | <span data-ttu-id="acfef-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="acfef-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="acfef-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="acfef-135">End of client support</span></span><br/>    | <span data-ttu-id="acfef-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="acfef-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="acfef-137">Produit</span><span class="sxs-lookup"><span data-stu-id="acfef-137">Product</span></span><br/>                  | <span data-ttu-id="acfef-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="acfef-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="acfef-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="acfef-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="acfef-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="acfef-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="acfef-141">IID</span><span class="sxs-lookup"><span data-stu-id="acfef-141">IID</span></span><br/>                      | <span data-ttu-id="acfef-142">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="acfef-142">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="acfef-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acfef-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acfef-144">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="acfef-144">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

