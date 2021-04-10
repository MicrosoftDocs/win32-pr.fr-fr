---
title: Propriété parente IVMHardDisk (VPCCOMInterfaces. h)
description: Parent du disque dur virtuel de différenciation.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Propriété Parent Virtual PC
- Propriété Parent Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, propriété parent
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941635"
---
# <a name="ivmharddiskparent-property"></a><span data-ttu-id="0ef40-106">IVMHardDisk ::P propriété rente</span><span class="sxs-lookup"><span data-stu-id="0ef40-106">IVMHardDisk::Parent property</span></span>

<span data-ttu-id="0ef40-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ef40-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0ef40-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0ef40-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0ef40-109">Récupère et définit le parent du disque dur virtuel de différenciation.</span><span class="sxs-lookup"><span data-stu-id="0ef40-109">Retrieves and sets the parent of the differencing virtual hard disk.</span></span>

<span data-ttu-id="0ef40-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0ef40-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef40-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ef40-111">Syntax</span></span>


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a><span data-ttu-id="0ef40-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0ef40-112">Property value</span></span>

<span data-ttu-id="0ef40-113">Définit l’objet [**IVMHardDisk**](ivmharddisk.md) associé à l’image de disque dur parent.</span><span class="sxs-lookup"><span data-stu-id="0ef40-113">Sets the [**IVMHardDisk**](ivmharddisk.md) object associated with the parent hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0ef40-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0ef40-114">Error codes</span></span>



| <span data-ttu-id="0ef40-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="0ef40-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="0ef40-116">Signification</span><span class="sxs-lookup"><span data-stu-id="0ef40-116">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ef40-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="0ef40-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0ef40-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="0ef40-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="0ef40-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0ef40-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="0ef40-121"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="0ef40-122">Ce n’est pas un disque dur de différenciation, donc il n’a pas de parent.</span><span class="sxs-lookup"><span data-stu-id="0ef40-122">This is not a differencing hard disk, so it has no parent.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="0ef40-123">Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="0ef40-124">Le système n’a pas pu trouver le fichier de disque dur virtuel parent.</span><span class="sxs-lookup"><span data-stu-id="0ef40-124">The system could not find the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="0ef40-125">Valeur <dt>HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="0ef40-126">Le système n’a pas pu trouver le chemin d’accès au fichier de disque dur virtuel parent.</span><span class="sxs-lookup"><span data-stu-id="0ef40-126">The system could not find the path to the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="0ef40-127"><dt>Ordinateur virtuel \_ \_Échec d' \_ \_ ouverture \_ d’une image HD E</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-127"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="0ef40-128">Une erreur s’est produite lors de la tentative d’ouverture du fichier image de disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="0ef40-128">An error occurred while attempting to open the current hard disk image file.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="0ef40-129"><dt>Ordinateur virtuel \_ 0xA0040681 \_ d' \_ \_ accès à l’image HD</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-129"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="0ef40-130">Une erreur s’est produite lors de la tentative d’accès au fichier image du disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="0ef40-130">An error occurred while attempting to access the current hard disk image file.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="0ef40-131"><dt>Ordinateur virtuel \_ \_Incompatibilité \_ d' \_ ID \_ enfant parent E</dt> <dt>0xA0040685</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-131"><dt>VM\_E\_PARENT\_CHILD\_ID\_MISMATCH</dt> <dt>0xA0040685</dt></span></span> </dl>            | <span data-ttu-id="0ef40-132">L’image de disque dur virtuel située dans le paramètre *parent* n’a pas le même ID que l’image de disque enfant.</span><span class="sxs-lookup"><span data-stu-id="0ef40-132">The virtual hard disk image located by the *parent* parameter does not have the same ID as the child disk image.</span></span> <span data-ttu-id="0ef40-133">Assurez-vous que l’image de disque dur virtuel parent située dans le paramètre *parent* est la même que celle utilisée pour créer l’image de disque dur virtuel de différenciation.</span><span class="sxs-lookup"><span data-stu-id="0ef40-133">Make sure the parent virtual hard disk image located by the *parent* parameter is the same image used to create the differencing virtual hard disk image.</span></span><br/> |
| <dl> <span data-ttu-id="0ef40-134"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="0ef40-135">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0ef40-135">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="0ef40-136">Notes</span><span class="sxs-lookup"><span data-stu-id="0ef40-136">Remarks</span></span>

<span data-ttu-id="0ef40-137">Cette propriété est valide uniquement avec les images de disque dur de différenciation.</span><span class="sxs-lookup"><span data-stu-id="0ef40-137">This property is only valid with differencing hard disk images.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef40-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ef40-138">Requirements</span></span>



| <span data-ttu-id="0ef40-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ef40-139">Requirement</span></span> | <span data-ttu-id="0ef40-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ef40-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef40-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ef40-141">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef40-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ef40-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ef40-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ef40-143">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef40-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ef40-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0ef40-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0ef40-145">End of client support</span></span><br/>    | <span data-ttu-id="0ef40-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0ef40-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0ef40-147">Produit</span><span class="sxs-lookup"><span data-stu-id="0ef40-147">Product</span></span><br/>                  | <span data-ttu-id="0ef40-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0ef40-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0ef40-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ef40-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef40-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef40-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0ef40-151">IID</span><span class="sxs-lookup"><span data-stu-id="0ef40-151">IID</span></span><br/>                      | <span data-ttu-id="0ef40-152">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="0ef40-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="0ef40-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ef40-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef40-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="0ef40-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

