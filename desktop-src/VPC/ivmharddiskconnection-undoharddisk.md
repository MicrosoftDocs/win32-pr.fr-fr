---
title: IVMHardDiskConnection UndoHardDisk, propriété (VPCCOMInterfaces. h)
description: Récupère un objet disque dur correspondant à l’image de disque d’annulation de cette connexion.
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- UndoHardDisk propriété Virtual PC
- UndoHardDisk, propriété Virtual PC, IVMHardDiskConnection, interface
- IVMHardDiskConnection interface Virtual PC, propriété UndoHardDisk
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102820"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a><span data-ttu-id="e3155-106">IVMHardDiskConnection :: UndoHardDisk, propriété</span><span class="sxs-lookup"><span data-stu-id="e3155-106">IVMHardDiskConnection::UndoHardDisk property</span></span>

<span data-ttu-id="e3155-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e3155-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e3155-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e3155-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e3155-109">Récupère un objet disque dur correspondant à l’image de disque d’annulation de cette connexion.</span><span class="sxs-lookup"><span data-stu-id="e3155-109">Retrieves a hard disk object corresponding to this connection's undo disk image.</span></span>

<span data-ttu-id="e3155-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e3155-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3155-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3155-111">Syntax</span></span>


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a><span data-ttu-id="e3155-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e3155-112">Property value</span></span>

<span data-ttu-id="e3155-113">Objet [**IVMHardDisk**](ivmharddisk.md) qui décrit le disque dur d’annulation associé à cette connexion.</span><span class="sxs-lookup"><span data-stu-id="e3155-113">An [**IVMHardDisk**](ivmharddisk.md) object that describes the undo hard disk associated with this connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e3155-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e3155-114">Error codes</span></span>



| <span data-ttu-id="e3155-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="e3155-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="e3155-116">Signification</span><span class="sxs-lookup"><span data-stu-id="e3155-116">Meaning</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3155-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e3155-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="e3155-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e3155-118">The operation was successful.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="e3155-119"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e3155-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="e3155-120">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="e3155-120">An unexpected error has occurred.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e3155-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e3155-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="e3155-122">Le paramètre a la **valeur null** ou n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e3155-122">The parameter is **NULL** or not valid.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="e3155-123">Valeur <dt>HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="e3155-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="e3155-124">Le disque d’annulation pour cette connexion est introuvable.</span><span class="sxs-lookup"><span data-stu-id="e3155-124">The undo disk for this connection was not found.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e3155-125"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="e3155-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="e3155-126">La configuration actuelle de l’ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e3155-126">The current virtual machine configuration is not valid.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="e3155-127"><dt>Ordinateur virtuel \_ 0xA0040502 \_ lecteur E \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e3155-127"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="e3155-128">L’emplacement du bus pour cette connexion n’a pas été correctement initialisé, ou l’appareil à cet emplacement n’est pas un disque dur valide.</span><span class="sxs-lookup"><span data-stu-id="e3155-128">The bus location for this connection has not been properly initialized, or the device at this location is not a valid hard disk.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="e3155-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3155-129">Requirements</span></span>



| <span data-ttu-id="e3155-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3155-130">Requirement</span></span> | <span data-ttu-id="e3155-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3155-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3155-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3155-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e3155-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3155-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3155-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3155-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e3155-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3155-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e3155-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="e3155-136">End of client support</span></span><br/>    | <span data-ttu-id="e3155-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e3155-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e3155-138">Produit</span><span class="sxs-lookup"><span data-stu-id="e3155-138">Product</span></span><br/>                  | <span data-ttu-id="e3155-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e3155-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e3155-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3155-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3155-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3155-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e3155-142">IID</span><span class="sxs-lookup"><span data-stu-id="e3155-142">IID</span></span><br/>                      | <span data-ttu-id="e3155-143">IID \_ IVMHardDiskconnection est défini en tant que aefa36a5-463a-46AE-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="e3155-143">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="e3155-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3155-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3155-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="e3155-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

