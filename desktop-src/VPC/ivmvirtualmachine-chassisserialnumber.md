---
title: IVMVirtualMachine ChassisSerialNumber, propriété (VPCCOMInterfaces. h)
description: Numéro de série du châssis.
ms.assetid: 03e02e6e-6819-4052-a0e0-9167eb5fdf4b
keywords:
- ChassisSerialNumber propriété Virtual PC
- ChassisSerialNumber, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété ChassisSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisSerialNumber
- IVMVirtualMachine.get_ChassisSerialNumber
- IVMVirtualMachine.put_ChassisSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00edbac12248f624ac06d1f7b88c3782c3f5a3df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032955"
---
# <a name="ivmvirtualmachinechassisserialnumber-property"></a><span data-ttu-id="ef152-106">IVMVirtualMachine :: ChassisSerialNumber, propriété</span><span class="sxs-lookup"><span data-stu-id="ef152-106">IVMVirtualMachine::ChassisSerialNumber property</span></span>

<span data-ttu-id="ef152-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ef152-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ef152-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ef152-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ef152-109">Récupère et définit le numéro de série du châssis.</span><span class="sxs-lookup"><span data-stu-id="ef152-109">Retrieves and sets the chassis serial number.</span></span>

<span data-ttu-id="ef152-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ef152-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef152-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef152-111">Syntax</span></span>


```C++
HRESULT put_ChassisSerialNumber(
  [in]          BSTR chasisSerialNumber
);

HRESULT get_ChassisSerialNumber(
  [out, retval] BSTR *chassisSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="ef152-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ef152-112">Property value</span></span>

<span data-ttu-id="ef152-113">Spécifie le numéro de série du châssis.</span><span class="sxs-lookup"><span data-stu-id="ef152-113">Specifies the chassis serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef152-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ef152-114">Error codes</span></span>



| <span data-ttu-id="ef152-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="ef152-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="ef152-116">Signification</span><span class="sxs-lookup"><span data-stu-id="ef152-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef152-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ef152-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="ef152-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ef152-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ef152-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ef152-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="ef152-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ef152-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="ef152-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ef152-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="ef152-122">Le paramètre est supérieur à 32 caractères, une chaîne vide ou non valide.</span><span class="sxs-lookup"><span data-stu-id="ef152-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="ef152-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="ef152-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="ef152-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="ef152-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ef152-125"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_ </dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="ef152-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="ef152-126">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="ef152-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="ef152-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ef152-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="ef152-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="ef152-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="ef152-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ef152-129">Remarks</span></span>

<span data-ttu-id="ef152-130">Cette propriété ne contient pas d’informations valides tant que l’ordinateur virtuel n’a pas démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="ef152-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="ef152-131">Une chaîne vide est retournée si elle est lue avant le démarrage initial.</span><span class="sxs-lookup"><span data-stu-id="ef152-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef152-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef152-132">Requirements</span></span>



| <span data-ttu-id="ef152-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef152-133">Requirement</span></span> | <span data-ttu-id="ef152-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef152-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef152-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef152-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ef152-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef152-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef152-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef152-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ef152-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef152-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ef152-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="ef152-139">End of client support</span></span><br/>    | <span data-ttu-id="ef152-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ef152-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ef152-141">Produit</span><span class="sxs-lookup"><span data-stu-id="ef152-141">Product</span></span><br/>                  | <span data-ttu-id="ef152-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ef152-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ef152-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef152-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef152-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef152-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ef152-145">IID</span><span class="sxs-lookup"><span data-stu-id="ef152-145">IID</span></span><br/>                      | <span data-ttu-id="ef152-146">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ef152-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ef152-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef152-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef152-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ef152-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

