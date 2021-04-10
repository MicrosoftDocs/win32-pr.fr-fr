---
title: IVMHardDisk, méthode de fusion (VPCCOMInterfaces. h)
description: Fusionne un disque dur virtuel de différenciation avec son image de disque parent.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Méthode de fusion Virtual PC
- Méthode de fusion Virtual PC, interface IVMHardDisk
- IVMHardDisk interface virtuelle, méthode de fusion
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942322"
---
# <a name="ivmharddiskmerge-method"></a><span data-ttu-id="09fb6-106">IVMHardDisk :: Merge, méthode</span><span class="sxs-lookup"><span data-stu-id="09fb6-106">IVMHardDisk::Merge method</span></span>

<span data-ttu-id="09fb6-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="09fb6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="09fb6-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="09fb6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="09fb6-109">Fusionne un disque dur virtuel de différenciation avec son image de disque parent.</span><span class="sxs-lookup"><span data-stu-id="09fb6-109">Merges a differencing virtual hard disk with its parent disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fb6-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09fb6-110">Syntax</span></span>


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="09fb6-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09fb6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fb6-112">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="09fb6-112">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="09fb6-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de fusion.</span><span class="sxs-lookup"><span data-stu-id="09fb6-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fb6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09fb6-114">Return value</span></span>

<span data-ttu-id="09fb6-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="09fb6-115">This method can return one of these values.</span></span>



| <span data-ttu-id="09fb6-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="09fb6-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="09fb6-117">Description</span><span class="sxs-lookup"><span data-stu-id="09fb6-117">Description</span></span>                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09fb6-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="09fb6-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="09fb6-119">The operation was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="09fb6-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="09fb6-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="09fb6-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="09fb6-122">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="09fb6-123">L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) est en cours d’utilisation ou le parent de cette image de disque dur virtuel est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="09fb6-123">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use or the parent of this virtual hard disk image is in use.</span></span> <span data-ttu-id="09fb6-124">Ou bien, ces images de disque dur peuvent faire partie d’un état enregistré.</span><span class="sxs-lookup"><span data-stu-id="09fb6-124">Or, these hard disk images could be part of a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="09fb6-125"><dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-125"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="09fb6-126">L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) doit être une image de disque de différenciation.</span><span class="sxs-lookup"><span data-stu-id="09fb6-126">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a differencing disk image.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="09fb6-127"><dt>**Ordinateur virtuel \_ \_Fichier E \_ lecture \_ seule**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-127"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="09fb6-128">Le parent de l’image de disque dur virtuel référencé par cet objet [**IVMHardDisk**](ivmharddisk.md) est marqué en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09fb6-128">The parent of virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="09fb6-129"><dt>**Ordinateur virtuel \_ \_Chemin parent \_ E \_ \_ introuvable**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-129"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="09fb6-130">Le parent du disque dur virtuel référencé par cet objet [**IVMHardDisk**](ivmharddisk.md) n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="09fb6-130">The parent of the virtual hard disk referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not exist.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="09fb6-131"><dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-131"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="09fb6-132">Impossible de fusionner l’image de disque dur virtuel, car l’application est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="09fb6-132">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="09fb6-133"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="09fb6-134">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="09fb6-134">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="09fb6-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09fb6-135">Requirements</span></span>



| <span data-ttu-id="09fb6-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09fb6-136">Requirement</span></span> | <span data-ttu-id="09fb6-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="09fb6-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="09fb6-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09fb6-138">Minimum supported client</span></span><br/> | <span data-ttu-id="09fb6-139">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="09fb6-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="09fb6-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09fb6-140">Minimum supported server</span></span><br/> | <span data-ttu-id="09fb6-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="09fb6-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="09fb6-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="09fb6-142">End of client support</span></span><br/>    | <span data-ttu-id="09fb6-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09fb6-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="09fb6-144">Produit</span><span class="sxs-lookup"><span data-stu-id="09fb6-144">Product</span></span><br/>                  | <span data-ttu-id="09fb6-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="09fb6-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="09fb6-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="09fb6-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="09fb6-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="09fb6-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="09fb6-148">IID</span><span class="sxs-lookup"><span data-stu-id="09fb6-148">IID</span></span><br/>                      | <span data-ttu-id="09fb6-149">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="09fb6-149">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="09fb6-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09fb6-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fb6-151">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="09fb6-151">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

