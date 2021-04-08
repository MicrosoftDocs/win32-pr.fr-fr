---
title: IVMDVDDrive DeviceNumber, propriété (VPCCOMInterfaces. h)
description: Récupère le numéro de périphérique auquel ce lecteur est attaché.
ms.assetid: 57b09400-e0c8-4ca2-bcd4-e6dd047daf95
keywords:
- DeviceNumber propriété Virtual PC
- DeviceNumber, propriété Virtual PC, IVMDVDDrive, interface
- IVMDVDDrive interface Virtual PC, propriété DeviceNumber
topic_type:
- apiref
api_name:
- IVMDVDDrive.DeviceNumber
- IVMDVDDrive.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de189b162ed2c880819f4c8729e996236ace250a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032997"
---
# <a name="ivmdvddrivedevicenumber-property"></a><span data-ttu-id="40c47-106">IVMDVDDrive ::D propriété eviceNumber</span><span class="sxs-lookup"><span data-stu-id="40c47-106">IVMDVDDrive::DeviceNumber property</span></span>

<span data-ttu-id="40c47-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="40c47-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40c47-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="40c47-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40c47-109">Récupère le numéro de périphérique auquel ce lecteur est attaché.</span><span class="sxs-lookup"><span data-stu-id="40c47-109">Retrieves the device number to which this drive is attached.</span></span>

<span data-ttu-id="40c47-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="40c47-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c47-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40c47-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="40c47-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="40c47-112">Property value</span></span>

<span data-ttu-id="40c47-113">Numéro de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="40c47-113">The device number.</span></span> <span data-ttu-id="40c47-114">Par exemple, sur un bus IDE, cette valeur représente l’emplacement principal ou secondaire.</span><span class="sxs-lookup"><span data-stu-id="40c47-114">For example, on an IDE bus, this value would represent either the primary or secondary location.</span></span>

## <a name="error-codes"></a><span data-ttu-id="40c47-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="40c47-115">Error codes</span></span>



| <span data-ttu-id="40c47-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="40c47-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="40c47-117">Signification</span><span class="sxs-lookup"><span data-stu-id="40c47-117">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40c47-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40c47-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="40c47-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="40c47-119">The operation was successful.</span></span><br/>                                          |
| <dl> <span data-ttu-id="40c47-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="40c47-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="40c47-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="40c47-121">The parameter is **NULL**.</span></span><br/>                                             |
| <dl> <span data-ttu-id="40c47-122"><dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="40c47-122"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="40c47-123">L’emplacement du bus pour ce lecteur de DVD n’a pas été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="40c47-123">The bus location for this DVD drive has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="40c47-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="40c47-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="40c47-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="40c47-125">An unexpected error has occurred.</span></span><br/>                                      |



## <a name="requirements"></a><span data-ttu-id="40c47-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40c47-126">Requirements</span></span>



| <span data-ttu-id="40c47-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40c47-127">Requirement</span></span> | <span data-ttu-id="40c47-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="40c47-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c47-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40c47-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40c47-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40c47-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40c47-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40c47-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40c47-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40c47-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40c47-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="40c47-133">End of client support</span></span><br/>    | <span data-ttu-id="40c47-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40c47-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40c47-135">Produit</span><span class="sxs-lookup"><span data-stu-id="40c47-135">Product</span></span><br/>                  | <span data-ttu-id="40c47-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40c47-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40c47-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="40c47-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="40c47-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="40c47-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40c47-139">IID</span><span class="sxs-lookup"><span data-stu-id="40c47-139">IID</span></span><br/>                      | <span data-ttu-id="40c47-140">IID \_ IVMDVDDrive est défini en tant que b96328f6-6732-437D-A00D-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="40c47-140">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="40c47-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40c47-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c47-142">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="40c47-142">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

