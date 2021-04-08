---
title: IVMFloppyDrive DriveNumber, propriété (VPCCOMInterfaces. h)
description: Récupère l’index de base zéro du contrôleur auquel le lecteur de disquette est attaché.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- DriveNumber propriété Virtual PC
- DriveNumber, propriété Virtual PC, IVMFloppyDrive, interface
- IVMFloppyDrive interface Virtual PC, propriété DriveNumber
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843725"
---
# <a name="ivmfloppydrivedrivenumber-property"></a><span data-ttu-id="02d6c-106">IVMFloppyDrive ::D propriété riveNumber</span><span class="sxs-lookup"><span data-stu-id="02d6c-106">IVMFloppyDrive::DriveNumber property</span></span>

<span data-ttu-id="02d6c-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02d6c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02d6c-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02d6c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02d6c-109">Récupère l’index de base zéro du contrôleur auquel le lecteur de disquette est attaché.</span><span class="sxs-lookup"><span data-stu-id="02d6c-109">Retrieves the zero-based index of the controller to which the floppy drive is attached.</span></span>

<span data-ttu-id="02d6c-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="02d6c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d6c-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02d6c-111">Syntax</span></span>


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a><span data-ttu-id="02d6c-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="02d6c-112">Property value</span></span>

<span data-ttu-id="02d6c-113">Index de base zéro du contrôleur.</span><span class="sxs-lookup"><span data-stu-id="02d6c-113">The zero-based index of the controller.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02d6c-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="02d6c-114">Error codes</span></span>



| <span data-ttu-id="02d6c-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="02d6c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="02d6c-116">Signification</span><span class="sxs-lookup"><span data-stu-id="02d6c-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="02d6c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02d6c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="02d6c-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="02d6c-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="02d6c-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="02d6c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="02d6c-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="02d6c-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="02d6c-121"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="02d6c-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="02d6c-122">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="02d6c-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="02d6c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02d6c-123">Requirements</span></span>



| <span data-ttu-id="02d6c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02d6c-124">Requirement</span></span> | <span data-ttu-id="02d6c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="02d6c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02d6c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02d6c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="02d6c-127">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02d6c-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02d6c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02d6c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="02d6c-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="02d6c-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02d6c-130">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="02d6c-130">End of client support</span></span><br/>    | <span data-ttu-id="02d6c-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02d6c-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02d6c-132">Produit</span><span class="sxs-lookup"><span data-stu-id="02d6c-132">Product</span></span><br/>                  | <span data-ttu-id="02d6c-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02d6c-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02d6c-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="02d6c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="02d6c-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="02d6c-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="02d6c-136">IID</span><span class="sxs-lookup"><span data-stu-id="02d6c-136">IID</span></span><br/>                      | <span data-ttu-id="02d6c-137">IID \_ IVMFloppyDrive est défini en tant que 661abee6-112a-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="02d6c-137">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="02d6c-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02d6c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d6c-139">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="02d6c-139">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

