---
title: IVMHardDiskConnection BusNumber, propriété (VPCCOMInterfaces. h)
description: Récupère le numéro de bus auquel l’image de lecteur est attachée.
ms.assetid: 2a792930-d8c9-419d-88eb-ddec7c43c5bc
keywords:
- BusNumber propriété Virtual PC
- BusNumber, propriété Virtual PC, IVMHardDiskConnection, interface
- IVMHardDiskConnection interface Virtual PC, propriété BusNumber
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.BusNumber
- IVMHardDiskConnection.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdc49a0d4cb284ecd1e2a1340d3b0bf8d9ed43ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466158"
---
# <a name="ivmharddiskconnectionbusnumber-property"></a><span data-ttu-id="6d501-106">IVMHardDiskConnection :: BusNumber, propriété</span><span class="sxs-lookup"><span data-stu-id="6d501-106">IVMHardDiskConnection::BusNumber property</span></span>

<span data-ttu-id="6d501-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6d501-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6d501-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6d501-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6d501-109">Récupère le numéro de bus auquel l’image de lecteur est attachée.</span><span class="sxs-lookup"><span data-stu-id="6d501-109">Retrieves the bus number to which the drive image is attached.</span></span>

<span data-ttu-id="6d501-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6d501-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d501-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d501-111">Syntax</span></span>


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a><span data-ttu-id="6d501-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6d501-112">Property value</span></span>

<span data-ttu-id="6d501-113">Numéro de bus qui correspond à cette connexion.</span><span class="sxs-lookup"><span data-stu-id="6d501-113">The bus number that corresponds with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d501-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6d501-114">Error codes</span></span>



| <span data-ttu-id="6d501-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="6d501-115">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="6d501-116">Signification</span><span class="sxs-lookup"><span data-stu-id="6d501-116">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d501-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6d501-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="6d501-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="6d501-118">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="6d501-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6d501-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="6d501-120">Le paramètre a la **valeur null** ou n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d501-120">The parameter is **NULL** or not valid.</span></span><br/>                                 |
| <dl> <span data-ttu-id="6d501-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="6d501-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="6d501-122">La configuration actuelle de l’ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d501-122">The current virtual machine configuration is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="6d501-123"><dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6d501-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="6d501-124">L’emplacement du bus pour cette connexion n’a pas été correctement initialisé.</span><span class="sxs-lookup"><span data-stu-id="6d501-124">The bus location for this connection has not been properly initialized.</span></span><br/> |
| <dl> <span data-ttu-id="6d501-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="6d501-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="6d501-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6d501-126">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="6d501-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d501-127">Requirements</span></span>



| <span data-ttu-id="6d501-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d501-128">Requirement</span></span> | <span data-ttu-id="6d501-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d501-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d501-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d501-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6d501-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d501-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d501-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d501-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6d501-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d501-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6d501-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="6d501-134">End of client support</span></span><br/>    | <span data-ttu-id="6d501-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6d501-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6d501-136">Produit</span><span class="sxs-lookup"><span data-stu-id="6d501-136">Product</span></span><br/>                  | <span data-ttu-id="6d501-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6d501-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6d501-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d501-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d501-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d501-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6d501-140">IID</span><span class="sxs-lookup"><span data-stu-id="6d501-140">IID</span></span><br/>                      | <span data-ttu-id="6d501-141">IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="6d501-141">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="6d501-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d501-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d501-143">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="6d501-143">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

