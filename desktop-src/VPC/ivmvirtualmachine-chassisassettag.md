---
title: IVMVirtualMachine ChassisAssetTag, propriété (VPCCOMInterfaces. h)
description: Étiquette de la ressource du châssis.
ms.assetid: 469816a8-3078-4960-a5e1-79d65b5fc8fc
keywords:
- ChassisAssetTag propriété Virtual PC
- ChassisAssetTag, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété ChassisAssetTag
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisAssetTag
- IVMVirtualMachine.get_ChassisAssetTag
- IVMVirtualMachine.put_ChassisAssetTag
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72d02f71907121354c4d937436366548d41f9944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843833"
---
# <a name="ivmvirtualmachinechassisassettag-property"></a><span data-ttu-id="e434e-106">IVMVirtualMachine :: ChassisAssetTag, propriété</span><span class="sxs-lookup"><span data-stu-id="e434e-106">IVMVirtualMachine::ChassisAssetTag property</span></span>

<span data-ttu-id="e434e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e434e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e434e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e434e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e434e-109">Récupère et définit la balise de la ressource du châssis.</span><span class="sxs-lookup"><span data-stu-id="e434e-109">Retrieves and sets the chassis asset tag.</span></span>

<span data-ttu-id="e434e-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e434e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e434e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e434e-111">Syntax</span></span>


```C++
HRESULT put_ChassisAssetTag(
  [in]          BSTR chassisAssetTag
);

HRESULT get_ChassisAssetTag(
  [out, retval] BSTR *chassisAssetTag
);
```



## <a name="property-value"></a><span data-ttu-id="e434e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e434e-112">Property value</span></span>

<span data-ttu-id="e434e-113">Spécifie la balise de la ressource du châssis.</span><span class="sxs-lookup"><span data-stu-id="e434e-113">Specifies the chassis asset tag.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e434e-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e434e-114">Error codes</span></span>



| <span data-ttu-id="e434e-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="e434e-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="e434e-116">Signification</span><span class="sxs-lookup"><span data-stu-id="e434e-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e434e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e434e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="e434e-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e434e-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e434e-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e434e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="e434e-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e434e-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="e434e-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e434e-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="e434e-122">Le paramètre est supérieur à 32 caractères, une chaîne vide ou non valide.</span><span class="sxs-lookup"><span data-stu-id="e434e-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="e434e-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="e434e-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="e434e-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="e434e-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e434e-125"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_ </dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="e434e-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="e434e-126">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="e434e-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="e434e-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e434e-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="e434e-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e434e-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="e434e-129">Notes</span><span class="sxs-lookup"><span data-stu-id="e434e-129">Remarks</span></span>

<span data-ttu-id="e434e-130">Cette propriété ne contient pas d’informations valides tant que l’ordinateur virtuel n’a pas démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="e434e-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="e434e-131">Une chaîne vide est retournée si elle est lue avant le démarrage initial.</span><span class="sxs-lookup"><span data-stu-id="e434e-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="e434e-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e434e-132">Requirements</span></span>



| <span data-ttu-id="e434e-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e434e-133">Requirement</span></span> | <span data-ttu-id="e434e-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e434e-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e434e-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e434e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e434e-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e434e-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e434e-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e434e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e434e-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e434e-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e434e-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e434e-139">End of client support</span></span><br/>    | <span data-ttu-id="e434e-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e434e-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e434e-141">Produit</span><span class="sxs-lookup"><span data-stu-id="e434e-141">Product</span></span><br/>                  | <span data-ttu-id="e434e-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e434e-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e434e-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="e434e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e434e-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e434e-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e434e-145">IID</span><span class="sxs-lookup"><span data-stu-id="e434e-145">IID</span></span><br/>                      | <span data-ttu-id="e434e-146">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="e434e-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="e434e-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e434e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e434e-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e434e-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

