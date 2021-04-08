---
title: Méthode IVMFloppyDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libère un lecteur physique sur l’ordinateur hôte à partir du lecteur de disquette.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Méthode ReleaseHostDrive Virtual PC
- Méthode ReleaseHostDrive Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, méthode ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739772"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a><span data-ttu-id="39a41-106">IVMFloppyDrive :: ReleaseHostDrive, méthode</span><span class="sxs-lookup"><span data-stu-id="39a41-106">IVMFloppyDrive::ReleaseHostDrive method</span></span>

<span data-ttu-id="39a41-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39a41-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39a41-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39a41-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39a41-109">Libère un lecteur physique sur l’ordinateur hôte à partir du lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="39a41-109">Releases a physical drive on the host from the floppy drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="39a41-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39a41-110">Syntax</span></span>


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a><span data-ttu-id="39a41-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39a41-111">Parameters</span></span>

<span data-ttu-id="39a41-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="39a41-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="39a41-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39a41-113">Return value</span></span>

<span data-ttu-id="39a41-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="39a41-114">This method can return one of these values.</span></span>



| <span data-ttu-id="39a41-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="39a41-115">Return code/value</span></span>                                                                                                                                                          | <span data-ttu-id="39a41-116">Description</span><span class="sxs-lookup"><span data-stu-id="39a41-116">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39a41-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39a41-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="39a41-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="39a41-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="39a41-119"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="39a41-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>          | <span data-ttu-id="39a41-120">La configuration de cette machine virtuelle n’est pas valide ou est introuvable.</span><span class="sxs-lookup"><span data-stu-id="39a41-120">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="39a41-121"><dt>**Ordinateur virtuel \_ \_Type de média E \_ incorrect \_**</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="39a41-121"><dt>**VM\_E\_MEDIA\_WRONG\_TYPE**</dt> <dt>0xA00400728</dt></span></span> </dl>  | <span data-ttu-id="39a41-122">Le support attaché à ce lecteur de disquette n’est pas un lecteur de disquette physique.</span><span class="sxs-lookup"><span data-stu-id="39a41-122">The media attached to this floppy drive is not a physical floppy drive.</span></span><br/>     |
| <dl> <span data-ttu-id="39a41-123"><dt>**Ordinateur virtuel \_ E \_ aucun \_ support \_ capturé**</dt> <dt>0xA00400652</dt></span><span class="sxs-lookup"><span data-stu-id="39a41-123"><dt>**VM\_E\_NO\_MEDIA\_CAPTURED**</dt> <dt>0xA00400652</dt></span></span> </dl> | <span data-ttu-id="39a41-124">Aucun support n’est attaché à ce lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="39a41-124">There is no media attached to this floppy drive.</span></span><br/>                            |
| <dl> <span data-ttu-id="39a41-125"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="39a41-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>          | <span data-ttu-id="39a41-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="39a41-126">An unexpected error has occurred.</span></span><br/>                                           |



 

## <a name="requirements"></a><span data-ttu-id="39a41-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39a41-127">Requirements</span></span>



| <span data-ttu-id="39a41-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39a41-128">Requirement</span></span> | <span data-ttu-id="39a41-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="39a41-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39a41-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39a41-130">Minimum supported client</span></span><br/> | <span data-ttu-id="39a41-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39a41-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39a41-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39a41-132">Minimum supported server</span></span><br/> | <span data-ttu-id="39a41-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="39a41-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39a41-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="39a41-134">End of client support</span></span><br/>    | <span data-ttu-id="39a41-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39a41-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39a41-136">Produit</span><span class="sxs-lookup"><span data-stu-id="39a41-136">Product</span></span><br/>                  | <span data-ttu-id="39a41-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39a41-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39a41-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="39a41-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="39a41-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39a41-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39a41-140">IID</span><span class="sxs-lookup"><span data-stu-id="39a41-140">IID</span></span><br/>                      | <span data-ttu-id="39a41-141">IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="39a41-141">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="39a41-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39a41-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39a41-143">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="39a41-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

