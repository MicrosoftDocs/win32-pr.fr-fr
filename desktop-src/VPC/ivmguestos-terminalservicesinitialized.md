---
title: IVMGuestOS TerminalServicesInitialized, propriété (VPCCOMInterfaces. h)
description: État de Services Bureau à distance dans le système d’exploitation invité.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- TerminalServicesInitialized propriété Virtual PC
- TerminalServicesInitialized, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété TerminalServicesInitialized
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92ce23b4b07f3e2d06f605f4598c8b31e4c70692
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509334"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a><span data-ttu-id="05ecb-106">IVMGuestOS :: TerminalServicesInitialized, propriété</span><span class="sxs-lookup"><span data-stu-id="05ecb-106">IVMGuestOS::TerminalServicesInitialized property</span></span>

<span data-ttu-id="05ecb-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05ecb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05ecb-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05ecb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05ecb-109">Récupère l’état des Services Bureau à distance (anciennement services Terminal Server) dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="05ecb-109">Retrieves the status of Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="05ecb-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="05ecb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ecb-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05ecb-111">Syntax</span></span>


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a><span data-ttu-id="05ecb-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="05ecb-112">Property value</span></span>

<span data-ttu-id="05ecb-113">État d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="05ecb-113">The initialization status.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05ecb-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="05ecb-114">Error codes</span></span>



| <span data-ttu-id="05ecb-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="05ecb-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="05ecb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="05ecb-116">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05ecb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05ecb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="05ecb-118">L’opération a réussi et Services Bureau à distance a été initialisée.</span><span class="sxs-lookup"><span data-stu-id="05ecb-118">The operation was successful and Remote Desktop Services has been initialized.</span></span> <span data-ttu-id="05ecb-119">La valeur de propriété retournée indique si Services Bureau à distance est disponible dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="05ecb-119">The returned property value indicates whether Remote Desktop Services is available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="05ecb-120"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="05ecb-120"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="05ecb-121">La fonctionnalité composants d’intégration est en cours d’exécution, mais Services Bureau à distance n’est pas encore initialisée.</span><span class="sxs-lookup"><span data-stu-id="05ecb-121">The integration components feature is running, but Remote Desktop Services is not yet initialized.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="05ecb-122"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="05ecb-122"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="05ecb-123">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="05ecb-123">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="05ecb-124"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="05ecb-124"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="05ecb-125">L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="05ecb-125">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="05ecb-126"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="05ecb-126"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="05ecb-127">La fonctionnalité composants d’intégration n’est pas en cours d’exécution dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="05ecb-127">The integration components feature is not running in the guest operating system.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="05ecb-128"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="05ecb-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="05ecb-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="05ecb-129">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="05ecb-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05ecb-130">Requirements</span></span>



| <span data-ttu-id="05ecb-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05ecb-131">Requirement</span></span> | <span data-ttu-id="05ecb-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="05ecb-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05ecb-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05ecb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="05ecb-134">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="05ecb-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05ecb-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05ecb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="05ecb-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05ecb-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="05ecb-137">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="05ecb-137">End of client support</span></span><br/>    | <span data-ttu-id="05ecb-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05ecb-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="05ecb-139">Produit</span><span class="sxs-lookup"><span data-stu-id="05ecb-139">Product</span></span><br/>                  | <span data-ttu-id="05ecb-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05ecb-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="05ecb-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="05ecb-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="05ecb-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="05ecb-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="05ecb-143">IID</span><span class="sxs-lookup"><span data-stu-id="05ecb-143">IID</span></span><br/>                      | <span data-ttu-id="05ecb-144">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="05ecb-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="05ecb-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05ecb-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ecb-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="05ecb-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

