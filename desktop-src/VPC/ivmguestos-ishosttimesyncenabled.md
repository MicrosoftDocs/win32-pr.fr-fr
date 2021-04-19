---
title: IVMGuestOS IsHostTimeSyncEnabled, propriété (VPCCOMInterfaces. h)
description: Indique si les composants d’intégration de cette machine virtuelle doivent synchroniser l’horloge de l’invité avec l’horloge de l’hôte.
ms.assetid: 57e3d49c-4acf-402f-9332-58ea443b363b
keywords:
- IsHostTimeSyncEnabled propriété Virtual PC
- IsHostTimeSyncEnabled, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété IsHostTimeSyncEnabled
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHostTimeSyncEnabled
- IVMGuestOS.get_IsHostTimeSyncEnabled
- IVMGuestOS.put_IsHostTimeSyncEnabled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87afddb2e3bc940c5dba7e2548e4355d36142012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509325"
---
# <a name="ivmguestosishosttimesyncenabled-property"></a><span data-ttu-id="f2625-106">IVMGuestOS :: IsHostTimeSyncEnabled, propriété</span><span class="sxs-lookup"><span data-stu-id="f2625-106">IVMGuestOS::IsHostTimeSyncEnabled property</span></span>

<span data-ttu-id="f2625-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f2625-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f2625-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f2625-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f2625-109">Indique si les composants d’intégration de cette machine virtuelle doivent synchroniser l’horloge de l’invité avec l’horloge de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f2625-109">Indicates whether the Integration Components in this virtual machine (VM) should synchronize the guest's clock with the host's clock.</span></span>

<span data-ttu-id="f2625-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f2625-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2625-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2625-111">Syntax</span></span>


```C++
HRESULT put_IsHostTimeSyncEnabled(
  [in]          VARIANT_BOOL shouldEnable
);

HRESULT get_IsHostTimeSyncEnabled(
  [out, retval] VARIANT_BOOL *isEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="f2625-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f2625-112">Property value</span></span>

<span data-ttu-id="f2625-113">Utilisez la **variante \_ true** si les composants d’intégration de cette machine virtuelle doivent synchroniser l’horloge de l’invité avec l’horloge de l’hôte et la **variante \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f2625-113">Use **VARIANT\_TRUE** if the integration components in this VM should synchronize the guest's clock with the host's clock and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2625-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f2625-114">Error codes</span></span>



| <span data-ttu-id="f2625-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="f2625-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f2625-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f2625-116">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="f2625-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f2625-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f2625-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f2625-118">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="f2625-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f2625-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f2625-120">Le paramètre *IsEnabled* n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="f2625-120">The *isEnabled* parameter is not specified.</span></span><br/> |
| <dl> <span data-ttu-id="f2625-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="f2625-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f2625-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="f2625-122">The configuration is unknown.</span></span><br/>               |
| <dl> <span data-ttu-id="f2625-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f2625-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f2625-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f2625-124">An unexpected error has occurred.</span></span><br/>           |



## <a name="remarks"></a><span data-ttu-id="f2625-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f2625-125">Remarks</span></span>

<span data-ttu-id="f2625-126">Vous ne pouvez pas modifier ce paramètre lorsque l’ordinateur virtuel est actif (autrement dit, en cours d’exécution ou dans un état enregistré).</span><span class="sxs-lookup"><span data-stu-id="f2625-126">You cannot change this setting while the virtual machine is active (that is, running or in saved state).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2625-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2625-127">Requirements</span></span>



| <span data-ttu-id="f2625-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2625-128">Requirement</span></span> | <span data-ttu-id="f2625-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2625-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2625-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2625-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f2625-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2625-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2625-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2625-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f2625-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2625-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f2625-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f2625-134">End of client support</span></span><br/>    | <span data-ttu-id="f2625-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f2625-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f2625-136">Produit</span><span class="sxs-lookup"><span data-stu-id="f2625-136">Product</span></span><br/>                  | <span data-ttu-id="f2625-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f2625-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f2625-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2625-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2625-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2625-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f2625-140">IID</span><span class="sxs-lookup"><span data-stu-id="f2625-140">IID</span></span><br/>                      | <span data-ttu-id="f2625-141">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="f2625-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f2625-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2625-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2625-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="f2625-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

