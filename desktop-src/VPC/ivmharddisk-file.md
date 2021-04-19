---
title: Propriété de fichier IVMHardDisk (VPCCOMInterfaces. h)
description: Récupère le nom du chemin d’accès complet du fichier de disque dur virtuel.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Propriété de fichier Virtual PC
- Propriété de fichier Virtual PC, interface IVMHardDisk
- IVMHardDisk interface Virtual PC, propriété de fichier
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511177"
---
# <a name="ivmharddiskfile-property"></a><span data-ttu-id="8b5d3-106">IVMHardDisk :: file, propriété</span><span class="sxs-lookup"><span data-stu-id="8b5d3-106">IVMHardDisk::File property</span></span>

<span data-ttu-id="8b5d3-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8b5d3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8b5d3-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8b5d3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8b5d3-109">Récupère le nom du chemin d’accès complet du fichier de disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="8b5d3-109">Retrieves the full path name of the virtual hard disk file.</span></span>

<span data-ttu-id="8b5d3-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8b5d3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b5d3-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b5d3-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a><span data-ttu-id="8b5d3-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8b5d3-112">Property value</span></span>

<span data-ttu-id="8b5d3-113">Nom de chemin d’accès complet du fichier image de disque dur actuel.</span><span class="sxs-lookup"><span data-stu-id="8b5d3-113">The full path name of the current hard disk image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b5d3-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8b5d3-114">Error codes</span></span>



| <span data-ttu-id="8b5d3-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="8b5d3-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="8b5d3-116">Signification</span><span class="sxs-lookup"><span data-stu-id="8b5d3-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8b5d3-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8b5d3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="8b5d3-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8b5d3-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="8b5d3-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8b5d3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="8b5d3-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8b5d3-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="8b5d3-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8b5d3-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="8b5d3-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8b5d3-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="8b5d3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b5d3-123">Requirements</span></span>



| <span data-ttu-id="8b5d3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b5d3-124">Requirement</span></span> | <span data-ttu-id="8b5d3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b5d3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b5d3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b5d3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8b5d3-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b5d3-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8b5d3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b5d3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8b5d3-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b5d3-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8b5d3-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8b5d3-130">End of client support</span></span><br/>    | <span data-ttu-id="8b5d3-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8b5d3-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8b5d3-132">Produit</span><span class="sxs-lookup"><span data-stu-id="8b5d3-132">Product</span></span><br/>                  | <span data-ttu-id="8b5d3-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8b5d3-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8b5d3-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8b5d3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b5d3-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b5d3-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8b5d3-136">IID</span><span class="sxs-lookup"><span data-stu-id="8b5d3-136">IID</span></span><br/>                      | <span data-ttu-id="8b5d3-137">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="8b5d3-137">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="8b5d3-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b5d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b5d3-139">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="8b5d3-139">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

