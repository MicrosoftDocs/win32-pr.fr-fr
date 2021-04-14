---
title: Méthode IVMGuestOS InstallIntegrationComponents (VPCCOMInterfaces. h)
description: Localise et installe les derniers composants d’intégration dans le système d’exploitation invité.
ms.assetid: 06f302b3-ec2b-471a-8e2e-095ed6ecbd3d
keywords:
- Méthode InstallIntegrationComponents Virtual PC
- Méthode InstallIntegrationComponents Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode InstallIntegrationComponents
topic_type:
- apiref
api_name:
- IVMGuestOS.InstallIntegrationComponents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879ded1464ebd310e1d1da4e3a952dc086600350
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383947"
---
# <a name="ivmguestosinstallintegrationcomponents-method"></a><span data-ttu-id="8165c-106">IVMGuestOS :: InstallIntegrationComponents, méthode</span><span class="sxs-lookup"><span data-stu-id="8165c-106">IVMGuestOS::InstallIntegrationComponents method</span></span>

<span data-ttu-id="8165c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8165c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8165c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8165c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8165c-109">Localise et installe les derniers composants d’intégration dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="8165c-109">Locates and installs the latest Integration Components into the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8165c-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8165c-110">Syntax</span></span>


```C++
HRESULT InstallIntegrationComponents();
```



## <a name="parameters"></a><span data-ttu-id="8165c-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8165c-111">Parameters</span></span>

<span data-ttu-id="8165c-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8165c-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8165c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8165c-113">Return value</span></span>

<span data-ttu-id="8165c-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8165c-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8165c-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8165c-115">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="8165c-116">Description</span><span class="sxs-lookup"><span data-stu-id="8165c-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8165c-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8165c-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="8165c-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8165c-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="8165c-119"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="8165c-119"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                       | <span data-ttu-id="8165c-120">L’ordinateur virtuel doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="8165c-120">The virtual machine must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="8165c-121"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="8165c-121"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="8165c-122">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="8165c-122">The virtual machine could not be found.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8165c-123"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8165c-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="8165c-124">L’ordinateur virtuel n’a pas de lecteur de DVD vide.</span><span class="sxs-lookup"><span data-stu-id="8165c-124">The virtual machine does not have an empty DVD drive.</span></span><br/>                       |
| <dl> <span data-ttu-id="8165c-125"><dt>**Ordinateur virtuel \_ \_Échec du \_ démontage \_ du média E**</dt> <dt>0xA0040508</dt></span><span class="sxs-lookup"><span data-stu-id="8165c-125"><dt>**VM\_E\_MEDIA\_UNMOUNT\_FAIL**</dt> <dt>0xA0040508</dt></span></span> </dl>                   | <span data-ttu-id="8165c-126">Échec de la tentative de démontage du média à partir du lecteur DVD de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8165c-126">The attempt to unmount the media from the virtual machine DVD drive failed.</span></span><br/> |
| <dl> <span data-ttu-id="8165c-127"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8165c-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="8165c-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8165c-128">An unexpected error has occurred.</span></span><br/>                                           |
| <dl> <span data-ttu-id="8165c-129">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="8165c-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="8165c-130">Le système ne peut pas trouver le fichier ISO pour les composants d’intégration.</span><span class="sxs-lookup"><span data-stu-id="8165c-130">The system cannot find the ISO file for the Integration Components.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="8165c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8165c-131">Requirements</span></span>



| <span data-ttu-id="8165c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8165c-132">Requirement</span></span> | <span data-ttu-id="8165c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="8165c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8165c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8165c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8165c-135">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8165c-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8165c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8165c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8165c-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8165c-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8165c-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8165c-138">End of client support</span></span><br/>    | <span data-ttu-id="8165c-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8165c-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8165c-140">Produit</span><span class="sxs-lookup"><span data-stu-id="8165c-140">Product</span></span><br/>                  | <span data-ttu-id="8165c-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8165c-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8165c-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="8165c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="8165c-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8165c-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8165c-144">IID</span><span class="sxs-lookup"><span data-stu-id="8165c-144">IID</span></span><br/>                      | <span data-ttu-id="8165c-145">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="8165c-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8165c-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8165c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8165c-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="8165c-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

