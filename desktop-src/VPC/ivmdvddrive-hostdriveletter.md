---
title: IVMDVDDrive HostDriveLetter, propriété (VPCCOMInterfaces. h)
description: Lettre du lecteur hôte défini pour cet appareil.
ms.assetid: e17f707f-e1cf-4302-a69e-caa5829df1af
keywords:
- HostDriveLetter propriété Virtual PC
- HostDriveLetter, propriété Virtual PC, IVMDVDDrive, interface
- IVMDVDDrive interface Virtual PC, propriété HostDriveLetter
topic_type:
- apiref
api_name:
- IVMDVDDrive.HostDriveLetter
- IVMDVDDrive.get_HostDriveLetter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60d2599b8fb73e727100111dc37d29a9d13c5d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741093"
---
# <a name="ivmdvddrivehostdriveletter-property"></a><span data-ttu-id="f4415-106">IVMDVDDrive :: HostDriveLetter, propriété</span><span class="sxs-lookup"><span data-stu-id="f4415-106">IVMDVDDrive::HostDriveLetter property</span></span>

<span data-ttu-id="f4415-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f4415-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f4415-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f4415-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f4415-109">Récupère la lettre du jeu de lecteurs hôtes pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="f4415-109">Retrieves the letter of the host drive set for this device.</span></span>

<span data-ttu-id="f4415-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f4415-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4415-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4415-111">Syntax</span></span>


```C++
HRESULT get_HostDriveLetter(
  [out, retval] BSTR *driveLetter
);
```



## <a name="property-value"></a><span data-ttu-id="f4415-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f4415-112">Property value</span></span>

<span data-ttu-id="f4415-113">Lettre de lecteur.</span><span class="sxs-lookup"><span data-stu-id="f4415-113">The drive letter.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f4415-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f4415-114">Error codes</span></span>



| <span data-ttu-id="f4415-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="f4415-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="f4415-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f4415-116">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4415-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4415-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="f4415-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f4415-118">The operation was successful.</span></span><br/>                             |
| <dl> <span data-ttu-id="f4415-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f4415-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="f4415-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f4415-120">The parameter is **NULL**.</span></span><br/>                                |
| <dl> <span data-ttu-id="f4415-121"><dt>E \_ ÉCHEC</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="f4415-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="f4415-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f4415-122">An unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="f4415-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="f4415-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="f4415-124">L’ordinateur virtuel est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f4415-124">The virtual machine could not be found.</span></span><br/>                   |
| <dl> <span data-ttu-id="f4415-125"><dt>Ordinateur virtuel \_ \_Type de média E \_ incorrect \_ </dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="f4415-125"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="f4415-126">Le support capturé par ce lecteur de DVD n’est pas un lecteur hôte.</span><span class="sxs-lookup"><span data-stu-id="f4415-126">The media captured by this DVD drive is not a host drive.</span></span><br/> |
| <dl> <span data-ttu-id="f4415-127"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f4415-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="f4415-128">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="f4415-128">An unexpected error has occurred.</span></span><br/>                         |



## <a name="requirements"></a><span data-ttu-id="f4415-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4415-129">Requirements</span></span>



| <span data-ttu-id="f4415-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4415-130">Requirement</span></span> | <span data-ttu-id="f4415-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4415-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4415-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4415-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f4415-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4415-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f4415-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4415-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f4415-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4415-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f4415-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f4415-136">End of client support</span></span><br/>    | <span data-ttu-id="f4415-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f4415-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f4415-138">Produit</span><span class="sxs-lookup"><span data-stu-id="f4415-138">Product</span></span><br/>                  | <span data-ttu-id="f4415-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f4415-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f4415-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4415-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4415-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4415-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f4415-142">IID</span><span class="sxs-lookup"><span data-stu-id="f4415-142">IID</span></span><br/>                      | <span data-ttu-id="f4415-143">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="f4415-143">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f4415-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4415-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4415-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f4415-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

