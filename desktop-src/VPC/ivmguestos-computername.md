---
title: IVMGuestOS ComputerName, propriété (VPCCOMInterfaces. h)
description: Nom d’ordinateur du système d’exploitation invité en cours d’exécution sur l’ordinateur virtuel.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- Nom_ordinateur Virtual PC
- Nom_ordinateur, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété ComputerName
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b266c238809284b340095dd25390d6e5f3d2b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466834"
---
# <a name="ivmguestoscomputername-property"></a><span data-ttu-id="d88bb-106">IVMGuestOS :: ComputerName, propriété</span><span class="sxs-lookup"><span data-stu-id="d88bb-106">IVMGuestOS::ComputerName property</span></span>

<span data-ttu-id="d88bb-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d88bb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d88bb-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d88bb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d88bb-109">Récupère le nom d’ordinateur du système d’exploitation invité en cours d’exécution sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d88bb-109">Retrieves the computer name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="d88bb-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d88bb-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88bb-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d88bb-111">Syntax</span></span>


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a><span data-ttu-id="d88bb-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d88bb-112">Property value</span></span>

<span data-ttu-id="d88bb-113">Nom d’ordinateur du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="d88bb-113">The computer name of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d88bb-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d88bb-114">Error codes</span></span>



| <span data-ttu-id="d88bb-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="d88bb-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="d88bb-116">Signification</span><span class="sxs-lookup"><span data-stu-id="d88bb-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="d88bb-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d88bb-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="d88bb-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="d88bb-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="d88bb-119"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d88bb-119"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="d88bb-120">Le paramètre n’est pas valide ou n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="d88bb-120">The parameter is not valid or not specified.</span></span><br/>         |
| <dl> <span data-ttu-id="d88bb-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d88bb-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="d88bb-122">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d88bb-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="d88bb-123"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="d88bb-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="d88bb-124">Les composants d’intégration ne sont pas installés sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="d88bb-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="d88bb-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d88bb-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="d88bb-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="d88bb-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="d88bb-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d88bb-127">Requirements</span></span>



| <span data-ttu-id="d88bb-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d88bb-128">Requirement</span></span> | <span data-ttu-id="d88bb-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="d88bb-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d88bb-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d88bb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d88bb-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d88bb-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d88bb-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d88bb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d88bb-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d88bb-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d88bb-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d88bb-134">End of client support</span></span><br/>    | <span data-ttu-id="d88bb-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d88bb-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d88bb-136">Produit</span><span class="sxs-lookup"><span data-stu-id="d88bb-136">Product</span></span><br/>                  | <span data-ttu-id="d88bb-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d88bb-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d88bb-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="d88bb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d88bb-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d88bb-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d88bb-140">IID</span><span class="sxs-lookup"><span data-stu-id="d88bb-140">IID</span></span><br/>                      | <span data-ttu-id="d88bb-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="d88bb-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="d88bb-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d88bb-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88bb-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="d88bb-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

