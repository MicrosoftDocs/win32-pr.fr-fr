---
title: Méthode IVMFloppyDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Attache un lecteur physique sur l’ordinateur hôte au lecteur de disquette dans l’ordinateur virtuel.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- Méthode AttachHostDrive Virtual PC
- Méthode AttachHostDrive Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, méthode AttachHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a21785e3e1e4ec77146f048ab4cce018de9d8c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032995"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a><span data-ttu-id="09ef6-106">IVMFloppyDrive :: AttachHostDrive, méthode</span><span class="sxs-lookup"><span data-stu-id="09ef6-106">IVMFloppyDrive::AttachHostDrive method</span></span>

<span data-ttu-id="09ef6-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="09ef6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="09ef6-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="09ef6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="09ef6-109">Attache un lecteur physique sur l’ordinateur hôte au lecteur de disquette dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="09ef6-109">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="09ef6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09ef6-110">Syntax</span></span>


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a><span data-ttu-id="09ef6-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09ef6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09ef6-112">lettre de *lecteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09ef6-112">*driveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09ef6-113">La lettre de lecteur du lecteur de disquette physique sur l’ordinateur hôte doit être attachée.</span><span class="sxs-lookup"><span data-stu-id="09ef6-113">The drive letter of the physical floppy drive on the host machine to is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09ef6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09ef6-114">Return value</span></span>

<span data-ttu-id="09ef6-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="09ef6-115">This method can return one of these values.</span></span>



| <span data-ttu-id="09ef6-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="09ef6-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="09ef6-117">Description</span><span class="sxs-lookup"><span data-stu-id="09ef6-117">Description</span></span>                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09ef6-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="09ef6-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="09ef6-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="09ef6-120"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="09ef6-121">Le paramètre *driveLetter* a la **valeur null**, n’est pas un lecteur de disquette valide ou le chemin d’accès spécifié est vide.</span><span class="sxs-lookup"><span data-stu-id="09ef6-121">The *driveLetter* parameter is **NULL**, is not a valid floppy drive, or the given path is empty.</span></span><br/> |
| <dl> <span data-ttu-id="09ef6-122"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="09ef6-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="09ef6-123">La configuration de cette machine virtuelle n’est pas valide ou est introuvable.</span><span class="sxs-lookup"><span data-stu-id="09ef6-123">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                       |
| <dl> <span data-ttu-id="09ef6-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="09ef6-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="09ef6-125">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="09ef6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09ef6-126">Requirements</span></span>



| <span data-ttu-id="09ef6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09ef6-127">Requirement</span></span> | <span data-ttu-id="09ef6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="09ef6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="09ef6-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ef6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="09ef6-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09ef6-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09ef6-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ef6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="09ef6-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ef6-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="09ef6-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="09ef6-133">End of client support</span></span><br/>    | <span data-ttu-id="09ef6-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09ef6-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="09ef6-135">Produit</span><span class="sxs-lookup"><span data-stu-id="09ef6-135">Product</span></span><br/>                  | <span data-ttu-id="09ef6-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="09ef6-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="09ef6-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="09ef6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="09ef6-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="09ef6-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="09ef6-139">IID</span><span class="sxs-lookup"><span data-stu-id="09ef6-139">IID</span></span><br/>                      | <span data-ttu-id="09ef6-140">IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="09ef6-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="09ef6-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09ef6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ef6-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="09ef6-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

