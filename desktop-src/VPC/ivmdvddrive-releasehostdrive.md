---
title: Méthode IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libère un lecteur hôte capturé à partir du lecteur de DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- Méthode ReleaseHostDrive Virtual PC
- Méthode ReleaseHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2ed2c551ba619855743266b9b506a0c579f92a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384439"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a><span data-ttu-id="31635-106">IVMDVDDrive :: ReleaseHostDrive, méthode</span><span class="sxs-lookup"><span data-stu-id="31635-106">IVMDVDDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="31635-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="31635-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="31635-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="31635-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="31635-109">Libère un lecteur hôte capturé à partir du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="31635-109">Releases a captured host drive from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="31635-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="31635-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="31635-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31635-111">Parameters</span></span>

<span data-ttu-id="31635-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="31635-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31635-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="31635-113">Return value</span></span>

<span data-ttu-id="31635-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="31635-114">This method can return one of these values.</span></span>



| <span data-ttu-id="31635-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="31635-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="31635-116">Description</span><span class="sxs-lookup"><span data-stu-id="31635-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31635-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="31635-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="31635-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="31635-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="31635-119"><dt>**E \_ ÉCHEC**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="31635-119"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="31635-120">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="31635-120">An unexpected error has occurred.</span></span><br/>                                  |
| <dl> <span data-ttu-id="31635-121"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="31635-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="31635-122">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="31635-122">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="31635-123"><dt>**Ordinateur virtuel \_ \_Type de média E \_ incorrect \_**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="31635-123"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="31635-124">Le support actuellement capturé n’est pas un lecteur de disque hôte.</span><span class="sxs-lookup"><span data-stu-id="31635-124">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="31635-125"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="31635-125"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="31635-126">Le lecteur n’a pas pu être initialisé en raison d’un emplacement de bus non valide.</span><span class="sxs-lookup"><span data-stu-id="31635-126">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="31635-127"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="31635-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="31635-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="31635-128">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="31635-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31635-129">Requirements</span></span>



| <span data-ttu-id="31635-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31635-130">Requirement</span></span> | <span data-ttu-id="31635-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="31635-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="31635-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31635-132">Minimum supported client</span></span><br/> | <span data-ttu-id="31635-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31635-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="31635-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31635-134">Minimum supported server</span></span><br/> | <span data-ttu-id="31635-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="31635-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="31635-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="31635-136">End of client support</span></span><br/>    | <span data-ttu-id="31635-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="31635-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="31635-138">Produit</span><span class="sxs-lookup"><span data-stu-id="31635-138">Product</span></span><br/>                  | <span data-ttu-id="31635-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="31635-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="31635-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="31635-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="31635-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="31635-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="31635-142">IID</span><span class="sxs-lookup"><span data-stu-id="31635-142">IID</span></span><br/>                      | <span data-ttu-id="31635-143">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="31635-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="31635-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31635-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31635-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="31635-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

