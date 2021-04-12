---
title: Méthode IVMDVDDrive ReleaseImage (VPCCOMInterfaces. h)
description: Libère une image ISO capturée à partir du lecteur de DVD.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- Méthode ReleaseImage Virtual PC
- Méthode ReleaseImage Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface Virtual PC, méthode ReleaseImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a36a13b258d155760269399d9f25f5eda6f296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464462"
---
# <a name="ivmdvddrivereleaseimage-method"></a><span data-ttu-id="8cd09-106">IVMDVDDrive :: ReleaseImage, méthode</span><span class="sxs-lookup"><span data-stu-id="8cd09-106">IVMDVDDrive::ReleaseImage method</span></span>

<span data-ttu-id="8cd09-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8cd09-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8cd09-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8cd09-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8cd09-109">Libère une image ISO capturée à partir du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="8cd09-109">Releases a captured ISO image from the DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cd09-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cd09-110">Syntax</span></span>


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a><span data-ttu-id="8cd09-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cd09-111">Parameters</span></span>

<span data-ttu-id="8cd09-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8cd09-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8cd09-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cd09-113">Return value</span></span>

<span data-ttu-id="8cd09-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8cd09-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8cd09-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8cd09-115">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="8cd09-116">Description</span><span class="sxs-lookup"><span data-stu-id="8cd09-116">Description</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8cd09-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8cd09-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="8cd09-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8cd09-118">The operation was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="8cd09-119"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="8cd09-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="8cd09-120">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="8cd09-120">The virtual machine could not be found.</span></span><br/>                            |
| <dl> <span data-ttu-id="8cd09-121"><dt>**Ordinateur virtuel \_ \_Type de média E \_ incorrect \_**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="8cd09-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="8cd09-122">Le support actuellement capturé n’est pas un lecteur de disque hôte.</span><span class="sxs-lookup"><span data-stu-id="8cd09-122">The currently captured media is not a host disk drive.</span></span><br/>             |
| <dl> <span data-ttu-id="8cd09-123"><dt>**Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8cd09-123"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="8cd09-124">Le lecteur n’a pas pu être initialisé en raison d’un emplacement de bus non valide.</span><span class="sxs-lookup"><span data-stu-id="8cd09-124">The drive could not be initialized due to an invalid bus location.</span></span><br/> |
| <dl> <span data-ttu-id="8cd09-125"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8cd09-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="8cd09-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8cd09-126">An unexpected error has occurred.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="8cd09-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cd09-127">Requirements</span></span>



| <span data-ttu-id="8cd09-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cd09-128">Requirement</span></span> | <span data-ttu-id="8cd09-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cd09-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cd09-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cd09-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8cd09-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8cd09-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8cd09-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cd09-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8cd09-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cd09-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8cd09-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8cd09-134">End of client support</span></span><br/>    | <span data-ttu-id="8cd09-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8cd09-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8cd09-136">Produit</span><span class="sxs-lookup"><span data-stu-id="8cd09-136">Product</span></span><br/>                  | <span data-ttu-id="8cd09-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8cd09-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8cd09-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="8cd09-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cd09-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cd09-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8cd09-140">IID</span><span class="sxs-lookup"><span data-stu-id="8cd09-140">IID</span></span><br/>                      | <span data-ttu-id="8cd09-141">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="8cd09-141">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="8cd09-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cd09-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd09-143">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="8cd09-143">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

