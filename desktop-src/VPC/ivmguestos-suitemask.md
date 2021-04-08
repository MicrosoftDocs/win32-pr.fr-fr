---
title: IVMGuestOS SuiteMask, propriété (VPCCOMInterfaces. h)
description: Récupère le SuiteMask du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: 11d065c1-9d46-4c81-b843-776db3507a04
keywords:
- SuiteMask propriété Virtual PC
- SuiteMask, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété SuiteMask
topic_type:
- apiref
api_name:
- IVMGuestOS.SuiteMask
- IVMGuestOS.get_SuiteMask
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 348384dd729c5c7e63a45fcb8b3f05d0189a7fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743589"
---
# <a name="ivmguestossuitemask-property"></a><span data-ttu-id="f26a7-106">IVMGuestOS :: SuiteMask, propriété</span><span class="sxs-lookup"><span data-stu-id="f26a7-106">IVMGuestOS::SuiteMask property</span></span>

<span data-ttu-id="f26a7-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f26a7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f26a7-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f26a7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f26a7-109">Récupère le SuiteMask du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="f26a7-109">Retrieves the SuiteMask of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="f26a7-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f26a7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f26a7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f26a7-111">Syntax</span></span>


```C++
HRESULT get_SuiteMask(
  [out, retval] BSTR *suiteMask
);
```



## <a name="property-value"></a><span data-ttu-id="f26a7-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f26a7-112">Property value</span></span>

<span data-ttu-id="f26a7-113">Masque de suite.</span><span class="sxs-lookup"><span data-stu-id="f26a7-113">The suite mask.</span></span> <span data-ttu-id="f26a7-114">Les valeurs de chaîne suivantes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f26a7-114">The following string values are supported.</span></span>



| <span data-ttu-id="f26a7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f26a7-115">Value</span></span>                                                                                   | <span data-ttu-id="f26a7-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f26a7-116">Meaning</span></span>                                                                                                                                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f26a7-117"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-117"><dt>"0x00000004"</dt></span></span> </dl> | <span data-ttu-id="f26a7-118">Les composants Microsoft BackOffice sont installés.</span><span class="sxs-lookup"><span data-stu-id="f26a7-118">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="f26a7-119"><dt>"0x00000400"</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-119"><dt>"0x00000400"</dt></span></span> </dl> | <span data-ttu-id="f26a7-120">Windows Server 2003, Web Edition est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-120">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="f26a7-121"><dt>"0x00004000"</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-121"><dt>"0x00004000"</dt></span></span> </dl> | <span data-ttu-id="f26a7-122">Windows Server 2003, Compute Cluster Edition est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-122">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="f26a7-123"><dt>"0x00000080"</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-123"><dt>"0x00000080"</dt></span></span> </dl> | <span data-ttu-id="f26a7-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition ou Windows 2000 Datacenter Server est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-124">Windows Server 2008 R2 Datacenter, Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/> |
| <dl> <span data-ttu-id="f26a7-125"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-125"><dt>"0x00000002"</dt></span></span> </dl> | <span data-ttu-id="f26a7-126">Windows Server 2008 R2 Entreprise, Windows Server 2008 entreprise, Windows Server 2003, Enterprise Edition ou Windows 2000 Advanced Server est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-126">Windows Server 2008 R2 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span><br/>   |
| <dl> <span data-ttu-id="f26a7-127"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-127"><dt>"0x00000040"</dt></span></span> </dl> | <span data-ttu-id="f26a7-128">Windows XP Embedded est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-128">Windows XP Embedded is installed.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="f26a7-129"><dt>"0x00000200"</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-129"><dt>"0x00000200"</dt></span></span> </dl> | <span data-ttu-id="f26a7-130">Windows Vista Édition familiale Premium, Windows Vista Édition familiale basique ou Windows XP Édition familiale est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-130">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="f26a7-131"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-131"><dt>"0x00000100"</dt></span></span> </dl> | <span data-ttu-id="f26a7-132">Bureau à distance est pris en charge, mais une seule session interactive est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f26a7-132">Remote Desktop is supported, but only one interactive session is supported.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f26a7-133"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-133"><dt>"0x00000001"</dt></span></span> </dl> | <span data-ttu-id="f26a7-134">Microsoft Small Business Server a été installé sur le système, mais il a peut-être été mis à niveau vers une autre version de Windows.</span><span class="sxs-lookup"><span data-stu-id="f26a7-134">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f26a7-135"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-135"><dt>"0x00000020"</dt></span></span> </dl> | <span data-ttu-id="f26a7-136">Microsoft Small Business Server est installé avec la licence client restrictive en vigueur.</span><span class="sxs-lookup"><span data-stu-id="f26a7-136">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="f26a7-137"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-137"><dt>"0x00002000"</dt></span></span> </dl> | <span data-ttu-id="f26a7-138">Windows Storage Server 2003 R2 ou Windows Storage Server 2003 est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-138">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="f26a7-139"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-139"><dt>"0x00000010"</dt></span></span> </dl> | <span data-ttu-id="f26a7-140">Services Bureau à distance est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-140">Remote Desktop Services is installed.</span></span> <span data-ttu-id="f26a7-141">Cette valeur est toujours définie.</span><span class="sxs-lookup"><span data-stu-id="f26a7-141">This value is always set.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="f26a7-142"><dt>"0x00008000"</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-142"><dt>"0x00008000"</dt></span></span> </dl> | <span data-ttu-id="f26a7-143">Windows Server famille est installé.</span><span class="sxs-lookup"><span data-stu-id="f26a7-143">Windows Home Server is installed.</span></span><br/>                                                                                                                           |



 

## <a name="error-codes"></a><span data-ttu-id="f26a7-144">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f26a7-144">Error codes</span></span>



| <span data-ttu-id="f26a7-145">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="f26a7-145">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f26a7-146">Signification</span><span class="sxs-lookup"><span data-stu-id="f26a7-146">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f26a7-147"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-147"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="f26a7-148">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f26a7-148">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="f26a7-149"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-149"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="f26a7-150">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f26a7-150">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="f26a7-151"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-151"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="f26a7-152">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f26a7-152">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="f26a7-153"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-153"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="f26a7-154">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f26a7-154">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="f26a7-155"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-155"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="f26a7-156">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f26a7-156">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="f26a7-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f26a7-157">Requirements</span></span>



| <span data-ttu-id="f26a7-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f26a7-158">Requirement</span></span> | <span data-ttu-id="f26a7-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="f26a7-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f26a7-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f26a7-160">Minimum supported client</span></span><br/> | <span data-ttu-id="f26a7-161">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f26a7-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f26a7-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f26a7-162">Minimum supported server</span></span><br/> | <span data-ttu-id="f26a7-163">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f26a7-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f26a7-164">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f26a7-164">End of client support</span></span><br/>    | <span data-ttu-id="f26a7-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f26a7-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f26a7-166">Produit</span><span class="sxs-lookup"><span data-stu-id="f26a7-166">Product</span></span><br/>                  | <span data-ttu-id="f26a7-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f26a7-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f26a7-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="f26a7-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="f26a7-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f26a7-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f26a7-170">IID</span><span class="sxs-lookup"><span data-stu-id="f26a7-170">IID</span></span><br/>                      | <span data-ttu-id="f26a7-171">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="f26a7-171">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f26a7-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f26a7-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f26a7-173">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="f26a7-173">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

