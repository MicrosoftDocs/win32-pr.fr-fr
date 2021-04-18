---
title: Méthode IVMVirtualMachine AddDVDROMDrive (VPCCOMInterfaces. h)
description: Ajoute un nouveau lecteur de CD ou de DVD à la machine virtuelle.
ms.assetid: d39f2728-6146-42ed-b67f-6586566a7209
keywords:
- Méthode AddDVDROMDrive Virtual PC
- Méthode AddDVDROMDrive Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode AddDVDROMDrive
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7acbe70f6b338b3490c12ab67bcdfdc997d90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512812"
---
# <a name="ivmvirtualmachineadddvdromdrive-method"></a><span data-ttu-id="8afdc-106">IVMVirtualMachine :: AddDVDROMDrive, méthode</span><span class="sxs-lookup"><span data-stu-id="8afdc-106">IVMVirtualMachine::AddDVDROMDrive method</span></span>

<span data-ttu-id="8afdc-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8afdc-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8afdc-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8afdc-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8afdc-109">Ajoute un nouveau lecteur de CD ou de DVD à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="8afdc-109">Adds a new CD or DVD drive to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afdc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8afdc-110">Syntax</span></span>


```C++
HRESULT AddDVDROMDrive(
  [in]          long        busNumber,
  [in]          long        deviceNumber,
  [out, retval] IVMDVDDrive **dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="8afdc-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8afdc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8afdc-112">*busNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8afdc-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8afdc-113">Bus auquel le lecteur sera attaché.</span><span class="sxs-lookup"><span data-stu-id="8afdc-113">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="8afdc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8afdc-114">Value</span></span>                                                                        | <span data-ttu-id="8afdc-115">Signification</span><span class="sxs-lookup"><span data-stu-id="8afdc-115">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="8afdc-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="8afdc-117">Le lecteur sera attaché au premier bus.</span><span class="sxs-lookup"><span data-stu-id="8afdc-117">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="8afdc-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="8afdc-119">Le lecteur sera attaché au second bus.</span><span class="sxs-lookup"><span data-stu-id="8afdc-119">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8afdc-120">*deviceNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8afdc-120">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8afdc-121">Appareil auquel le lecteur sera attaché.</span><span class="sxs-lookup"><span data-stu-id="8afdc-121">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="8afdc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8afdc-122">Value</span></span>                                                                        | <span data-ttu-id="8afdc-123">Signification</span><span class="sxs-lookup"><span data-stu-id="8afdc-123">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8afdc-124"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-124"><dt>0</dt></span></span> </dl> | <span data-ttu-id="8afdc-125">Le lecteur sera attaché au premier périphérique sur le bus.</span><span class="sxs-lookup"><span data-stu-id="8afdc-125">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="8afdc-126"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-126"><dt>1</dt></span></span> </dl> | <span data-ttu-id="8afdc-127">Le lecteur sera attaché au deuxième périphérique sur le bus.</span><span class="sxs-lookup"><span data-stu-id="8afdc-127">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8afdc-128">*dvdDrive* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8afdc-128">*dvdDrive* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8afdc-129">Objet [**IVMDVDDrive**](ivmdvddrive.md) .</span><span class="sxs-lookup"><span data-stu-id="8afdc-129">An [**IVMDVDDrive**](ivmdvddrive.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8afdc-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8afdc-130">Return value</span></span>

<span data-ttu-id="8afdc-131">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8afdc-131">This method can return one of these values.</span></span>



| <span data-ttu-id="8afdc-132">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8afdc-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="8afdc-133">Description</span><span class="sxs-lookup"><span data-stu-id="8afdc-133">Description</span></span>                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="8afdc-134"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-134"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="8afdc-135">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8afdc-135">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="8afdc-136"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-136"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                       | <span data-ttu-id="8afdc-137">Le paramètre *dvdDrive* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8afdc-137">The *dvdDrive* parameter is **NULL**.</span></span><br/>               |
| <dl> <span data-ttu-id="8afdc-138"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-138"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="8afdc-139">Un paramètre n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8afdc-139">A parameter is not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="8afdc-140"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="8afdc-140"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="8afdc-141">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="8afdc-141">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="8afdc-142"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-142"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="8afdc-143">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="8afdc-143">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="8afdc-144"><dt>**Ordinateur virtuel \_ 0xA00400503 \_ \_ de bus \_ de lecteur E \_ en cours d' \_ utilisation**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-144"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="8afdc-145">L’emplacement de bus spécifié est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8afdc-145">The specified bus location is in use.</span></span><br/>               |
| <dl> <span data-ttu-id="8afdc-146"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-146"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="8afdc-147">Le lecteur spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8afdc-147">The drive specified is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="8afdc-148"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-148"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="8afdc-149">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8afdc-149">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="8afdc-150">Notes</span><span class="sxs-lookup"><span data-stu-id="8afdc-150">Remarks</span></span>

<span data-ttu-id="8afdc-151">Vous pouvez uniquement ajouter un nouveau lecteur de CD ou de DVD à une machine virtuelle arrêtée.</span><span class="sxs-lookup"><span data-stu-id="8afdc-151">You can only add a new CD or DVD drive to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afdc-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8afdc-152">Requirements</span></span>



| <span data-ttu-id="8afdc-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8afdc-153">Requirement</span></span> | <span data-ttu-id="8afdc-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="8afdc-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afdc-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8afdc-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8afdc-156">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8afdc-156">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8afdc-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8afdc-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8afdc-158">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8afdc-158">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8afdc-159">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8afdc-159">End of client support</span></span><br/>    | <span data-ttu-id="8afdc-160">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8afdc-160">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8afdc-161">Produit</span><span class="sxs-lookup"><span data-stu-id="8afdc-161">Product</span></span><br/>                  | <span data-ttu-id="8afdc-162">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8afdc-162">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8afdc-163">En-tête</span><span class="sxs-lookup"><span data-stu-id="8afdc-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="8afdc-164"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8afdc-164"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8afdc-165">IID</span><span class="sxs-lookup"><span data-stu-id="8afdc-165">IID</span></span><br/>                      | <span data-ttu-id="8afdc-166">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8afdc-166">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8afdc-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8afdc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afdc-168">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8afdc-168">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

