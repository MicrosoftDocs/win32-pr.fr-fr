---
title: IVMGuestOS propriété MultipleUserSessionsAllowed
description: Détermine si plusieurs sessions utilisateur simultanées sont autorisées dans le système d’exploitation invité.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- MultipleUserSessionsAllowed propriété Virtual PC
- MultipleUserSessionsAllowed, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété MultipleUserSessionsAllowed
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103969"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a><span data-ttu-id="60ac8-106">IVMGuestOS :: MultipleUserSessionsAllowed, propriété</span><span class="sxs-lookup"><span data-stu-id="60ac8-106">IVMGuestOS::MultipleUserSessionsAllowed property</span></span>

<span data-ttu-id="60ac8-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="60ac8-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="60ac8-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="60ac8-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="60ac8-109">Détermine si plusieurs sessions utilisateur simultanées sont autorisées dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="60ac8-109">Determines whether multiple simultaneous user sessions are allowed in the guest operating system.</span></span>

<span data-ttu-id="60ac8-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="60ac8-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ac8-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60ac8-111">Syntax</span></span>


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a><span data-ttu-id="60ac8-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="60ac8-112">Property value</span></span>

<span data-ttu-id="60ac8-113">**Variante \_ TRUE** si plusieurs sessions utilisateur simultanées sont autorisées dans le système d’exploitation invité, **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="60ac8-113">**VARIANT\_TRUE** if multiple simultaneous user sessions are allowed in the guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="60ac8-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="60ac8-114">Error codes</span></span>



| <span data-ttu-id="60ac8-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="60ac8-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="60ac8-116">Signification</span><span class="sxs-lookup"><span data-stu-id="60ac8-116">Meaning</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60ac8-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="60ac8-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="60ac8-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="60ac8-118">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="60ac8-119"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="60ac8-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="60ac8-120">Services Bureau à distance (anciennement « services Terminal Server ») n’est pas encore initialisé dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="60ac8-120">Remote Desktop Services (formerly known as Terminal Services) is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="60ac8-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="60ac8-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="60ac8-122">Le paramètre *sessionStatus* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="60ac8-122">The *sessionStatus* parameter is **NULL**.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="60ac8-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="60ac8-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="60ac8-124">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="60ac8-124">The virtual machine is not running.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="60ac8-125"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="60ac8-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="60ac8-126">Les composants d’intégration ne sont pas installés sur cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="60ac8-126">Integration components are not installed in this virtual machine.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="60ac8-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="60ac8-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="60ac8-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="60ac8-128">An unexpected error has occurred.</span></span><br/>                                                                                   |



## <a name="remarks"></a><span data-ttu-id="60ac8-129">Notes</span><span class="sxs-lookup"><span data-stu-id="60ac8-129">Remarks</span></span>

<span data-ttu-id="60ac8-130">La valeur de cette propriété n’est pas valide, sauf si la propriété [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) est définie sur **\_ true**.</span><span class="sxs-lookup"><span data-stu-id="60ac8-130">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="60ac8-131">Pour les systèmes d’exploitation clients Windows, **MultipleUserSessionsAllowed** a la **\_ valeur true** si le changement rapide d’utilisateur est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="60ac8-131">For Windows client operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Fast User Switching is supported.</span></span> <span data-ttu-id="60ac8-132">Pour les systèmes d’exploitation Windows Server, **MultipleUserSessionsAllowed** a la **\_ valeur true** si services Bureau à distance (autrefois appelé « services Terminal Server ») est installé et activé.</span><span class="sxs-lookup"><span data-stu-id="60ac8-132">For Windows Server operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Remote Desktop Services (formerly called Terminal Services) is installed and enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="60ac8-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60ac8-133">Requirements</span></span>



| <span data-ttu-id="60ac8-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60ac8-134">Requirement</span></span> | <span data-ttu-id="60ac8-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="60ac8-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ac8-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ac8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="60ac8-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="60ac8-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="60ac8-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ac8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="60ac8-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="60ac8-139">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="60ac8-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="60ac8-140">End of client support</span></span><br/>    | <span data-ttu-id="60ac8-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="60ac8-141">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="60ac8-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="60ac8-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60ac8-143"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60ac8-143"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="60ac8-144">IID</span><span class="sxs-lookup"><span data-stu-id="60ac8-144">IID</span></span><br/>                      | <span data-ttu-id="60ac8-145">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="60ac8-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="60ac8-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60ac8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ac8-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="60ac8-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

