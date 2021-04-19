---
title: IVMFloppyDrive, propriété de la pièce jointe (VPCCOMInterfaces. h)
description: Récupère le type de support attaché au lecteur de disquette dans l’ordinateur virtuel.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Propriété de pièce jointe Virtual PC
- Propriété des pièces jointes Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface Virtual PC, propriété Attachment
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510541"
---
# <a name="ivmfloppydriveattachment-property"></a><span data-ttu-id="71d75-106">IVMFloppyDrive :: Attachment, propriété</span><span class="sxs-lookup"><span data-stu-id="71d75-106">IVMFloppyDrive::Attachment property</span></span>

<span data-ttu-id="71d75-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71d75-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="71d75-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="71d75-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="71d75-109">Récupère le type de média attaché au lecteur de disquette dans l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="71d75-109">Retrieves the type of media attached to the floppy drive in the virtual machine (VM).</span></span>

<span data-ttu-id="71d75-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="71d75-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d75-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71d75-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="71d75-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="71d75-112">Property value</span></span>

<span data-ttu-id="71d75-113">Type de média.</span><span class="sxs-lookup"><span data-stu-id="71d75-113">The type of media.</span></span> <span data-ttu-id="71d75-114">Pour obtenir la liste des valeurs, consultez [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="71d75-114">For a list of values, see [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="71d75-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="71d75-115">Error codes</span></span>



| <span data-ttu-id="71d75-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="71d75-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="71d75-117">Signification</span><span class="sxs-lookup"><span data-stu-id="71d75-117">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71d75-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="71d75-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="71d75-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="71d75-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="71d75-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="71d75-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="71d75-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="71d75-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="71d75-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="71d75-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="71d75-123">La configuration de cette machine virtuelle n’est pas valide ou est introuvable.</span><span class="sxs-lookup"><span data-stu-id="71d75-123">The configuration for this VM is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="71d75-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="71d75-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="71d75-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="71d75-125">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="71d75-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71d75-126">Requirements</span></span>



| <span data-ttu-id="71d75-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71d75-127">Requirement</span></span> | <span data-ttu-id="71d75-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="71d75-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d75-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d75-129">Minimum supported client</span></span><br/> | <span data-ttu-id="71d75-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71d75-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71d75-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d75-131">Minimum supported server</span></span><br/> | <span data-ttu-id="71d75-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="71d75-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="71d75-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="71d75-133">End of client support</span></span><br/>    | <span data-ttu-id="71d75-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71d75-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="71d75-135">Produit</span><span class="sxs-lookup"><span data-stu-id="71d75-135">Product</span></span><br/>                  | <span data-ttu-id="71d75-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="71d75-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="71d75-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="71d75-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="71d75-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d75-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="71d75-139">IID</span><span class="sxs-lookup"><span data-stu-id="71d75-139">IID</span></span><br/>                      | <span data-ttu-id="71d75-140">IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="71d75-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="71d75-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71d75-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d75-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="71d75-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

