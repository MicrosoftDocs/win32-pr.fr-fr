---
title: IVMVirtualMachine BIOSSerialNumber, propriété (VPCCOMInterfaces. h)
description: Numéro de série du BIOS.
ms.assetid: a105009d-1c44-4079-a7d4-103cb02bad71
keywords:
- BIOSSerialNumber propriété Virtual PC
- BIOSSerialNumber, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété BIOSSerialNumber
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSSerialNumber
- IVMVirtualMachine.get_BIOSSerialNumber
- IVMVirtualMachine.put_BIOSSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8bd3f240d863a6f43dabbdb0a26429c4a77219
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033162"
---
# <a name="ivmvirtualmachinebiosserialnumber-property"></a><span data-ttu-id="b3d37-106">IVMVirtualMachine :: BIOSSerialNumber, propriété</span><span class="sxs-lookup"><span data-stu-id="b3d37-106">IVMVirtualMachine::BIOSSerialNumber property</span></span>

<span data-ttu-id="b3d37-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b3d37-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b3d37-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b3d37-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b3d37-109">Récupère et définit le numéro de série du BIOS.</span><span class="sxs-lookup"><span data-stu-id="b3d37-109">Retrieves and sets the BIOS serial number.</span></span>

<span data-ttu-id="b3d37-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b3d37-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3d37-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3d37-111">Syntax</span></span>


```C++
HRESULT put_BIOSSerialNumber(
  [in]          BSTR biosSerialNumber
);

HRESULT get_BIOSSerialNumber(
  [out, retval] BSTR *biosSerialNumber
);
```



## <a name="property-value"></a><span data-ttu-id="b3d37-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b3d37-112">Property value</span></span>

<span data-ttu-id="b3d37-113">Spécifie le numéro de série du BIOS.</span><span class="sxs-lookup"><span data-stu-id="b3d37-113">Specifies the BIOS serial number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b3d37-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b3d37-114">Error codes</span></span>



| <span data-ttu-id="b3d37-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="b3d37-115">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="b3d37-116">Signification</span><span class="sxs-lookup"><span data-stu-id="b3d37-116">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3d37-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b3d37-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="b3d37-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b3d37-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b3d37-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b3d37-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="b3d37-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b3d37-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="b3d37-121"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b3d37-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="b3d37-122">Le paramètre est supérieur à 32 caractères, une chaîne vide ou non valide.</span><span class="sxs-lookup"><span data-stu-id="b3d37-122">The parameter is greater than 32 characters, an empty string, or not valid.</span></span><br/> |
| <dl> <span data-ttu-id="b3d37-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="b3d37-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="b3d37-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="b3d37-124">The configuration is unknown.</span></span><br/>                                               |
| <dl> <span data-ttu-id="b3d37-125"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_ </dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="b3d37-125"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="b3d37-126">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="b3d37-126">The virtual machine is in a running or saved state.</span></span><br/>                         |
| <dl> <span data-ttu-id="b3d37-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b3d37-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="b3d37-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b3d37-128">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="remarks"></a><span data-ttu-id="b3d37-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b3d37-129">Remarks</span></span>

<span data-ttu-id="b3d37-130">Cette propriété ne contient pas d’informations valides tant que l’ordinateur virtuel n’a pas démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="b3d37-130">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="b3d37-131">Une chaîne vide est retournée si elle est lue avant le démarrage initial.</span><span class="sxs-lookup"><span data-stu-id="b3d37-131">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3d37-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3d37-132">Requirements</span></span>



| <span data-ttu-id="b3d37-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3d37-133">Requirement</span></span> | <span data-ttu-id="b3d37-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3d37-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d37-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3d37-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d37-136">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b3d37-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3d37-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3d37-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d37-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3d37-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b3d37-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b3d37-139">End of client support</span></span><br/>    | <span data-ttu-id="b3d37-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3d37-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b3d37-141">Produit</span><span class="sxs-lookup"><span data-stu-id="b3d37-141">Product</span></span><br/>                  | <span data-ttu-id="b3d37-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b3d37-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b3d37-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3d37-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3d37-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3d37-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b3d37-145">IID</span><span class="sxs-lookup"><span data-stu-id="b3d37-145">IID</span></span><br/>                      | <span data-ttu-id="b3d37-146">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b3d37-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b3d37-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3d37-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3d37-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b3d37-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

