---
title: Propriété de fichier IVMVirtualMachine (VPCCOMInterfaces. h)
description: Récupère le chemin d’accès complet du fichier. vmc pour la configuration de l’ordinateur virtuel.
ms.assetid: fc215068-e908-417c-bd68-214539a0a14e
keywords:
- Propriété de fichier Virtual PC
- Propriété de fichier Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, propriété de fichier
topic_type:
- apiref
api_name:
- IVMVirtualMachine.File
- IVMVirtualMachine.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ac3bc68d167a7057d76adc1ce84a29291b7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742052"
---
# <a name="ivmvirtualmachinefile-property"></a><span data-ttu-id="b768a-106">IVMVirtualMachine :: file, propriété</span><span class="sxs-lookup"><span data-stu-id="b768a-106">IVMVirtualMachine::File property</span></span>

<span data-ttu-id="b768a-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b768a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b768a-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b768a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b768a-109">Récupère le chemin d’accès complet du fichier. vmc pour la configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="b768a-109">Retrieves the fully qualified path of the .vmc file for the virtual machine configuration.</span></span>

<span data-ttu-id="b768a-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b768a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b768a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b768a-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *virtualMachineXMLFile
);
```



## <a name="property-value"></a><span data-ttu-id="b768a-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b768a-112">Property value</span></span>

<span data-ttu-id="b768a-113">Nom complet du \* fichier « . vmc » qui décrit cette configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="b768a-113">The fully qualified name of the "\*.vmc" file that describes this virtual machine configuration.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b768a-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b768a-114">Error codes</span></span>



| <span data-ttu-id="b768a-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="b768a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b768a-116">Signification</span><span class="sxs-lookup"><span data-stu-id="b768a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="b768a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b768a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b768a-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b768a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="b768a-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b768a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b768a-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b768a-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="b768a-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="b768a-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b768a-122">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="b768a-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="b768a-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b768a-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b768a-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b768a-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b768a-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b768a-125">Requirements</span></span>



| <span data-ttu-id="b768a-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b768a-126">Requirement</span></span> | <span data-ttu-id="b768a-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b768a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b768a-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b768a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b768a-129">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b768a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b768a-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b768a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b768a-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b768a-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b768a-132">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b768a-132">End of client support</span></span><br/>    | <span data-ttu-id="b768a-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b768a-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b768a-134">Produit</span><span class="sxs-lookup"><span data-stu-id="b768a-134">Product</span></span><br/>                  | <span data-ttu-id="b768a-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b768a-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b768a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="b768a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b768a-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b768a-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b768a-138">IID</span><span class="sxs-lookup"><span data-stu-id="b768a-138">IID</span></span><br/>                      | <span data-ttu-id="b768a-139">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="b768a-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="b768a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b768a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b768a-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b768a-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

