---
title: IVMVirtualMachine BIOSGUID, propriété (VPCCOMInterfaces. h)
description: GUID du BIOS.
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- BIOSGUID propriété Virtual PC
- BIOSGUID, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété BIOSGUID
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843510"
---
# <a name="ivmvirtualmachinebiosguid-property"></a><span data-ttu-id="adf6e-106">IVMVirtualMachine :: BIOSGUID, propriété</span><span class="sxs-lookup"><span data-stu-id="adf6e-106">IVMVirtualMachine::BIOSGUID property</span></span>

<span data-ttu-id="adf6e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="adf6e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="adf6e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="adf6e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="adf6e-109">Récupère et définit le GUID du BIOS.</span><span class="sxs-lookup"><span data-stu-id="adf6e-109">Retrieves and sets the BIOS GUID.</span></span>

<span data-ttu-id="adf6e-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="adf6e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf6e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="adf6e-111">Syntax</span></span>


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a><span data-ttu-id="adf6e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="adf6e-112">Property value</span></span>

<span data-ttu-id="adf6e-113">Spécifie le GUID du BIOS.</span><span class="sxs-lookup"><span data-stu-id="adf6e-113">Specifies the BIOS GUID.</span></span> <span data-ttu-id="adf6e-114">Incluez les accolades gauche et droite autour des chiffres hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="adf6e-114">Include left and right braces around the hex digits.</span></span>

## <a name="error-codes"></a><span data-ttu-id="adf6e-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="adf6e-115">Error codes</span></span>



| <span data-ttu-id="adf6e-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="adf6e-116">Name/value</span></span>                                                                                                                                                               | <span data-ttu-id="adf6e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="adf6e-117">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="adf6e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="adf6e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="adf6e-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="adf6e-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="adf6e-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="adf6e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="adf6e-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="adf6e-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="adf6e-122"><dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="adf6e-122"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="adf6e-123">Le paramètre n’est pas valide ou est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="adf6e-123">The parameter is not valid or is an empty string.</span></span><br/>   |
| <dl> <span data-ttu-id="adf6e-124"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="adf6e-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="adf6e-125">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="adf6e-125">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="adf6e-126"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_ </dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="adf6e-126"><dt>VM\_E\_VM\_RUNNING\_OR\_SAVED</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="adf6e-127">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="adf6e-127">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="adf6e-128"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="adf6e-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="adf6e-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="adf6e-129">An unexpected error has occurred.</span></span><br/>                   |



## <a name="remarks"></a><span data-ttu-id="adf6e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="adf6e-130">Remarks</span></span>

<span data-ttu-id="adf6e-131">Cette propriété ne contient pas d’informations valides tant que l’ordinateur virtuel n’a pas démarré pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="adf6e-131">This property will not contain valid information until after the virtual machine has started up for the first time.</span></span> <span data-ttu-id="adf6e-132">Une chaîne vide est retournée si elle est lue avant le démarrage initial.</span><span class="sxs-lookup"><span data-stu-id="adf6e-132">An empty string will be returned if it is read before the initial startup.</span></span>

## <a name="requirements"></a><span data-ttu-id="adf6e-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="adf6e-133">Requirements</span></span>



| <span data-ttu-id="adf6e-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="adf6e-134">Requirement</span></span> | <span data-ttu-id="adf6e-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="adf6e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf6e-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adf6e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="adf6e-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="adf6e-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="adf6e-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="adf6e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="adf6e-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="adf6e-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="adf6e-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="adf6e-140">End of client support</span></span><br/>    | <span data-ttu-id="adf6e-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="adf6e-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="adf6e-142">Produit</span><span class="sxs-lookup"><span data-stu-id="adf6e-142">Product</span></span><br/>                  | <span data-ttu-id="adf6e-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="adf6e-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="adf6e-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="adf6e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="adf6e-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="adf6e-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="adf6e-146">IID</span><span class="sxs-lookup"><span data-stu-id="adf6e-146">IID</span></span><br/>                      | <span data-ttu-id="adf6e-147">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="adf6e-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="adf6e-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="adf6e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf6e-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="adf6e-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

