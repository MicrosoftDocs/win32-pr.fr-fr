---
title: IVMHardDisk compact, méthode (VPCCOMInterfaces. h)
description: Compacte une image de disque dur virtuel de taille dynamique.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Méthode compact PC virtuelle
- Méthode compact PC Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, méthode compact
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743245"
---
# <a name="ivmharddiskcompact-method"></a><span data-ttu-id="a2687-106">IVMHardDisk :: compact, méthode</span><span class="sxs-lookup"><span data-stu-id="a2687-106">IVMHardDisk::Compact method</span></span>

<span data-ttu-id="a2687-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a2687-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a2687-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a2687-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a2687-109">Compacte une image de disque dur virtuel de taille dynamique.</span><span class="sxs-lookup"><span data-stu-id="a2687-109">Compacts a dynamically expanding virtual hard disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2687-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2687-110">Syntax</span></span>


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a><span data-ttu-id="a2687-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2687-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2687-112">*compactTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a2687-112">*compactTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a2687-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus de compactage.</span><span class="sxs-lookup"><span data-stu-id="a2687-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion the compaction process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2687-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2687-114">Return value</span></span>

<span data-ttu-id="a2687-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a2687-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a2687-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a2687-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="a2687-117">Description</span><span class="sxs-lookup"><span data-stu-id="a2687-117">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2687-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="a2687-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a2687-119">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="a2687-120"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="a2687-121">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a2687-121">An unexpected error has occurred.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="a2687-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="a2687-123">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a2687-123">The parameter is **NULL**.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="a2687-124">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="a2687-125">L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a2687-125">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use.</span></span><br/>                                  |
| <dl> <span data-ttu-id="a2687-126">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (disque d’erreur \_ \_ saturé)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="a2687-127">Le volume hôte ne dispose pas de suffisamment d’espace pour créer un fichier temporaire nécessaire pour la compression de cette image de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a2687-127">The host volume does not have enough space to create a temporary file needed for the compaction of this virtual hard disk image.</span></span><br/>     |
| <dl> <span data-ttu-id="a2687-128"><dt>**Ordinateur virtuel \_ \_ \_ Arrêt \_**</dt> de l’application <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-128"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="a2687-129">L’image de disque dur virtuel ne peut pas être compactée, car l’application est en cours d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a2687-129">The virtual hard disk image cannot be compacted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="a2687-130"><dt>**Ordinateur virtuel \_ \_Fichier E \_ lecture \_ seule**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-130"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="a2687-131">L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) est marquée en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a2687-131">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                     |
| <dl> <span data-ttu-id="a2687-132"><dt>**Ordinateur virtuel \_ E \_ mauvais \_ \_ \_ type d’image HD**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-132"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="a2687-133">L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) doit être un type d’image **vmDiskTypeDynamic** .</span><span class="sxs-lookup"><span data-stu-id="a2687-133">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a **vmDiskTypeDynamic** image type.</span></span><br/> |
| <dl> <span data-ttu-id="a2687-134"><dt>**Ordinateur virtuel \_ E \_ \_ \_ fichier HD 0xA0040682 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a2687-134"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="a2687-135">L’image de disque dur virtuel référencée par cet objet [**IVMHardDisk**](ivmharddisk.md) ne semble pas être une image valide.</span><span class="sxs-lookup"><span data-stu-id="a2687-135">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="a2687-136">Notes</span><span class="sxs-lookup"><span data-stu-id="a2687-136">Remarks</span></span>

<span data-ttu-id="a2687-137">Pour compacter une image de disque dur de taille dynamique, l’espace libre sur l’image de disque doit d’abord être mis à zéro.</span><span class="sxs-lookup"><span data-stu-id="a2687-137">To compact a dynamically expanding hard disk image, free space on the disk image should first be zeroed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2687-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2687-138">Requirements</span></span>



| <span data-ttu-id="a2687-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2687-139">Requirement</span></span> | <span data-ttu-id="a2687-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2687-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2687-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2687-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a2687-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2687-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a2687-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2687-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a2687-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2687-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a2687-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="a2687-145">End of client support</span></span><br/>    | <span data-ttu-id="a2687-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2687-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a2687-147">Produit</span><span class="sxs-lookup"><span data-stu-id="a2687-147">Product</span></span><br/>                  | <span data-ttu-id="a2687-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a2687-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a2687-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2687-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2687-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2687-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a2687-151">IID</span><span class="sxs-lookup"><span data-stu-id="a2687-151">IID</span></span><br/>                      | <span data-ttu-id="a2687-152">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="a2687-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a2687-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2687-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2687-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a2687-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

