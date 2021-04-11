---
title: IVMHardDiskConnection DeviceNumber, propriété (VPCCOMInterfaces. h)
description: Récupère le numéro d’appareil auquel l’image de lecteur est attachée.
ms.assetid: fea8bac6-fb25-495a-bc56-1d517b831f33
keywords:
- DeviceNumber propriété Virtual PC
- DeviceNumber, propriété Virtual PC, IVMHardDiskConnection, interface
- IVMHardDiskConnection interface Virtual PC, propriété DeviceNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.DeviceNumber
- IVMHardDiskConnection.get_DeviceNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b69f7d9d3f9a373c9b8086857af56c7e5da9f5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105808"
---
# <a name="ivmharddiskconnectiondevicenumber-property"></a><span data-ttu-id="2758b-106">IVMHardDiskConnection ::D propriété eviceNumber</span><span class="sxs-lookup"><span data-stu-id="2758b-106">IVMHardDiskConnection::DeviceNumber property</span></span>

<span data-ttu-id="2758b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2758b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2758b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2758b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2758b-109">Récupère le numéro d’appareil auquel l’image de lecteur est attachée.</span><span class="sxs-lookup"><span data-stu-id="2758b-109">Retrieves the device number to which the drive image is attached.</span></span>

<span data-ttu-id="2758b-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2758b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2758b-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2758b-111">Syntax</span></span>


```C++
HRESULT get_DeviceNumber(
  [out, retval] long *vmDeviceNumber
);
```



## <a name="property-value"></a><span data-ttu-id="2758b-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2758b-112">Property value</span></span>

<span data-ttu-id="2758b-113">Numéro de périphérique qui correspond à cette connexion.</span><span class="sxs-lookup"><span data-stu-id="2758b-113">The device number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2758b-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="2758b-114">Error codes</span></span>



| <span data-ttu-id="2758b-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="2758b-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="2758b-116">Signification</span><span class="sxs-lookup"><span data-stu-id="2758b-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2758b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2758b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="2758b-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2758b-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="2758b-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2758b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="2758b-120">Le paramètre a la **valeur null** ou n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2758b-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="2758b-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="2758b-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="2758b-122">La configuration actuelle de l’ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2758b-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="2758b-123"><dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2758b-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="2758b-124">L’emplacement du bus pour cette connexion n’a pas été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="2758b-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="2758b-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2758b-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="2758b-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2758b-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="2758b-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2758b-127">Requirements</span></span>



| <span data-ttu-id="2758b-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2758b-128">Requirement</span></span> | <span data-ttu-id="2758b-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="2758b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2758b-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2758b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2758b-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2758b-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2758b-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2758b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2758b-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2758b-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2758b-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2758b-134">End of client support</span></span><br/>    | <span data-ttu-id="2758b-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2758b-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2758b-136">Produit</span><span class="sxs-lookup"><span data-stu-id="2758b-136">Product</span></span><br/>                  | <span data-ttu-id="2758b-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2758b-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2758b-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="2758b-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2758b-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2758b-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2758b-140">IID</span><span class="sxs-lookup"><span data-stu-id="2758b-140">IID</span></span><br/>                      | <span data-ttu-id="2758b-141">IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="2758b-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="2758b-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2758b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2758b-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="2758b-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

