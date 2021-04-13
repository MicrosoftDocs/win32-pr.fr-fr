---
title: Méthode IVMVirtualMachine RemoveHardDiskConnection (VPCCOMInterfaces. h)
description: Supprime la connexion de disque dur spécifiée de l’ordinateur virtuel.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Méthode RemoveHardDiskConnection Virtual PC
- Méthode RemoveHardDiskConnection Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode RemoveHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384743"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a><span data-ttu-id="8c926-106">IVMVirtualMachine :: RemoveHardDiskConnection, méthode</span><span class="sxs-lookup"><span data-stu-id="8c926-106">IVMVirtualMachine::RemoveHardDiskConnection method</span></span>

<span data-ttu-id="8c926-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8c926-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8c926-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8c926-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8c926-109">Supprime la connexion de disque dur spécifiée de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8c926-109">Removes the specified hard disk connection from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c926-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c926-110">Syntax</span></span>


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="8c926-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c926-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c926-112">*hardDiskConnection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c926-112">*hardDiskConnection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c926-113">Objet [**IVMHardDiskConnection**](ivmharddiskconnection.md) qui représente la connexion au disque dur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8c926-113">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object that represents the hard disk connection to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c926-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c926-114">Return value</span></span>

<span data-ttu-id="8c926-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8c926-115">This method can return one of these values.</span></span>



| <span data-ttu-id="8c926-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8c926-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="8c926-117">Description</span><span class="sxs-lookup"><span data-stu-id="8c926-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="8c926-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8c926-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="8c926-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8c926-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="8c926-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8c926-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="8c926-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8c926-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="8c926-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="8c926-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="8c926-123">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="8c926-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="8c926-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="8c926-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="8c926-125">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="8c926-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="8c926-126"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8c926-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="8c926-127">Le lecteur spécifié n’est pas connecté à cet emplacement de bus.</span><span class="sxs-lookup"><span data-stu-id="8c926-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="8c926-128"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8c926-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="8c926-129">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8c926-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8c926-130">Notes</span><span class="sxs-lookup"><span data-stu-id="8c926-130">Remarks</span></span>

<span data-ttu-id="8c926-131">Vous pouvez uniquement supprimer une connexion de disque dur existante d’une machine virtuelle arrêtée.</span><span class="sxs-lookup"><span data-stu-id="8c926-131">You can only remove an existing hard disk connection from a stopped virtual machine.</span></span> <span data-ttu-id="8c926-132">Une liste des connexions actuellement attachées à la machine virtuelle est obtenue en énumérant la propriété [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="8c926-132">A list of connections currently attached to the virtual machine is obtained by enumerating the [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c926-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c926-133">Requirements</span></span>



| <span data-ttu-id="8c926-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c926-134">Requirement</span></span> | <span data-ttu-id="8c926-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c926-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c926-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c926-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8c926-137">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c926-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c926-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c926-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8c926-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c926-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8c926-140">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8c926-140">End of client support</span></span><br/>    | <span data-ttu-id="8c926-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8c926-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8c926-142">Produit</span><span class="sxs-lookup"><span data-stu-id="8c926-142">Product</span></span><br/>                  | <span data-ttu-id="8c926-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8c926-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8c926-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c926-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c926-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c926-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8c926-146">IID</span><span class="sxs-lookup"><span data-stu-id="8c926-146">IID</span></span><br/>                      | <span data-ttu-id="8c926-147">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8c926-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8c926-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c926-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c926-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="8c926-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

