---
title: IVMGuestOS ScreenLocked, propriété (VPCCOMInterfaces. h)
description: Indique si l’écran dans le système d’exploitation invité est verrouillé.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- ScreenLocked propriété Virtual PC
- ScreenLocked, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété ScreenLocked
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032960"
---
# <a name="ivmguestosscreenlocked-property"></a><span data-ttu-id="6306f-106">IVMGuestOS :: ScreenLocked, propriété</span><span class="sxs-lookup"><span data-stu-id="6306f-106">IVMGuestOS::ScreenLocked property</span></span>

<span data-ttu-id="6306f-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6306f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6306f-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6306f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6306f-109">Indique si l’écran dans le système d’exploitation invité est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="6306f-109">Indicates whether the screen in the guest operating system is locked.</span></span>

<span data-ttu-id="6306f-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6306f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6306f-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6306f-111">Syntax</span></span>


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a><span data-ttu-id="6306f-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6306f-112">Property value</span></span>

<span data-ttu-id="6306f-113">**Variante \_ TRUE** si l’écran est verrouillé dans le système d’exploitation invité, **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6306f-113">**VARIANT\_TRUE** if screen is locked in guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6306f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6306f-114">Error codes</span></span>



| <span data-ttu-id="6306f-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="6306f-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="6306f-116">Signification</span><span class="sxs-lookup"><span data-stu-id="6306f-116">Meaning</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6306f-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6306f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="6306f-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6306f-118">The operation was successful.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="6306f-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6306f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="6306f-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6306f-120">The parameter is **NULL**.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="6306f-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="6306f-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="6306f-122">L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="6306f-122">The virtual machine (VM) must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="6306f-123"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="6306f-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="6306f-124">La fonctionnalité composants d’intégration n’est pas activée dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="6306f-124">The integration components feature is not enabled in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="6306f-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6306f-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="6306f-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6306f-126">An unexpected error has occurred.</span></span><br/>                                                |



## <a name="requirements"></a><span data-ttu-id="6306f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6306f-127">Requirements</span></span>



| <span data-ttu-id="6306f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6306f-128">Requirement</span></span> | <span data-ttu-id="6306f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6306f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6306f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6306f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6306f-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6306f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6306f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6306f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6306f-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6306f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6306f-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6306f-134">End of client support</span></span><br/>    | <span data-ttu-id="6306f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6306f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6306f-136">Produit</span><span class="sxs-lookup"><span data-stu-id="6306f-136">Product</span></span><br/>                  | <span data-ttu-id="6306f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6306f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6306f-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="6306f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6306f-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6306f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6306f-140">IID</span><span class="sxs-lookup"><span data-stu-id="6306f-140">IID</span></span><br/>                      | <span data-ttu-id="6306f-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="6306f-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="6306f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6306f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6306f-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="6306f-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

