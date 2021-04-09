---
title: IVMHardDisk SizeOnHost, propriété (VPCCOMInterfaces. h)
description: Taille du fichier de disque dur virtuel sur l’ordinateur hôte.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- SizeOnHost propriété Virtual PC
- SizeOnHost, propriété Virtual PC, IVMHardDisk, interface
- IVMHardDisk interface Virtual PC, propriété SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033071"
---
# <a name="ivmharddisksizeonhost-property"></a><span data-ttu-id="270b2-106">IVMHardDisk :: SizeOnHost, propriété</span><span class="sxs-lookup"><span data-stu-id="270b2-106">IVMHardDisk::SizeOnHost property</span></span>

<span data-ttu-id="270b2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="270b2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="270b2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="270b2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="270b2-109">Récupère la taille du fichier de disque dur virtuel sur l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="270b2-109">Retrieves the size of the virtual hard disk file on the host computer.</span></span>

<span data-ttu-id="270b2-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="270b2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="270b2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="270b2-111">Syntax</span></span>


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="270b2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="270b2-112">Property value</span></span>

<span data-ttu-id="270b2-113">Taille, en octets, du fichier image de disque dur.</span><span class="sxs-lookup"><span data-stu-id="270b2-113">The size, in bytes, of the hard disk image file.</span></span> <span data-ttu-id="270b2-114">Cette valeur est une **variante** de type **VT \_ Decimal**.</span><span class="sxs-lookup"><span data-stu-id="270b2-114">This value is a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="270b2-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="270b2-115">Error codes</span></span>



| <span data-ttu-id="270b2-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="270b2-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="270b2-117">Signification</span><span class="sxs-lookup"><span data-stu-id="270b2-117">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="270b2-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="270b2-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="270b2-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="270b2-119">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="270b2-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="270b2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="270b2-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="270b2-121">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="270b2-122"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="270b2-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="270b2-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="270b2-123">An unexpected error has occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="270b2-124">Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="270b2-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="270b2-125">Le fichier image de disque dur est introuvable.</span><span class="sxs-lookup"><span data-stu-id="270b2-125">The hard disk image file was not found.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="270b2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="270b2-126">Requirements</span></span>



| <span data-ttu-id="270b2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="270b2-127">Requirement</span></span> | <span data-ttu-id="270b2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="270b2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="270b2-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="270b2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="270b2-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="270b2-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="270b2-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="270b2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="270b2-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="270b2-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="270b2-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="270b2-133">End of client support</span></span><br/>    | <span data-ttu-id="270b2-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="270b2-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="270b2-135">Produit</span><span class="sxs-lookup"><span data-stu-id="270b2-135">Product</span></span><br/>                  | <span data-ttu-id="270b2-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="270b2-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="270b2-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="270b2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="270b2-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="270b2-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="270b2-139">IID</span><span class="sxs-lookup"><span data-stu-id="270b2-139">IID</span></span><br/>                      | <span data-ttu-id="270b2-140">IID \_ IVMHardDisk est défini en tant que ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="270b2-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="270b2-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="270b2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="270b2-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="270b2-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

