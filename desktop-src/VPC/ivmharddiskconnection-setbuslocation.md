---
title: Méthode IVMHardDiskConnection SetBusLocation (VPCCOMInterfaces. h)
description: Définit l’emplacement du bus auquel ce disque dur est attaché.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Méthode SetBusLocation Virtual PC
- Méthode SetBusLocation Virtual PC, interface IVMHardDiskConnection
- IVMHardDiskConnection interface Virtual PC, méthode SetBusLocation
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317110"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a><span data-ttu-id="c991d-106">IVMHardDiskConnection :: SetBusLocation, méthode</span><span class="sxs-lookup"><span data-stu-id="c991d-106">IVMHardDiskConnection::SetBusLocation method</span></span>

<span data-ttu-id="c991d-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c991d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c991d-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c991d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c991d-109">Définit l’emplacement du bus auquel ce disque dur est attaché.</span><span class="sxs-lookup"><span data-stu-id="c991d-109">Sets the bus location to which this hard disk is attached.</span></span>

## <a name="syntax"></a><span data-ttu-id="c991d-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c991d-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="c991d-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c991d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c991d-112">*vmBusNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c991d-112">*vmBusNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c991d-113">Numéro de bus à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c991d-113">The bus number to be used.</span></span>

</dd> <dt>

<span data-ttu-id="c991d-114">*vmDeviceNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c991d-114">*vmDeviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c991d-115">Numéro d’appareil à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c991d-115">The device number to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c991d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c991d-116">Return value</span></span>

<span data-ttu-id="c991d-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c991d-117">This method can return one of these values.</span></span>



| <span data-ttu-id="c991d-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c991d-118">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="c991d-119">Description</span><span class="sxs-lookup"><span data-stu-id="c991d-119">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c991d-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c991d-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="c991d-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="c991d-121">The operation was successful.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="c991d-122"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="c991d-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="c991d-123">L’emplacement de bus spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c991d-123">The bus location specified is not valid.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="c991d-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="c991d-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="c991d-125">Impossible de définir l’emplacement du bus, car l’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="c991d-125">The bus location could not be set because the virtual machine is in a running or saved state.</span></span><br/>    |
| <dl> <span data-ttu-id="c991d-126"><dt>**Ordinateur virtuel \_ 0xA00400503 \_ \_ de bus \_ de lecteur E \_ en cours d' \_ utilisation**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c991d-126"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="c991d-127">Impossible de définir l’emplacement du bus, car un autre appareil est actuellement attaché à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="c991d-127">The bus location could not be set because another device is currently attached to this location.</span></span><br/> |
| <dl> <span data-ttu-id="c991d-128"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c991d-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="c991d-129">Le lecteur actuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c991d-129">The current drive is not valid.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="c991d-130"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="c991d-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="c991d-131">L’ordinateur virtuel actuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c991d-131">The current virtual machine is not valid.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c991d-132"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c991d-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="c991d-133">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c991d-133">An unexpected error has occurred.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="c991d-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c991d-134">Requirements</span></span>



| <span data-ttu-id="c991d-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c991d-135">Requirement</span></span> | <span data-ttu-id="c991d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c991d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c991d-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c991d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c991d-138">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c991d-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c991d-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c991d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c991d-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c991d-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c991d-141">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="c991d-141">End of client support</span></span><br/>    | <span data-ttu-id="c991d-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c991d-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c991d-143">Produit</span><span class="sxs-lookup"><span data-stu-id="c991d-143">Product</span></span><br/>                  | <span data-ttu-id="c991d-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c991d-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c991d-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="c991d-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c991d-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c991d-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c991d-147">IID</span><span class="sxs-lookup"><span data-stu-id="c991d-147">IID</span></span><br/>                      | <span data-ttu-id="c991d-148">IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="c991d-148">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="c991d-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c991d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c991d-150">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="c991d-150">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

