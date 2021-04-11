---
title: IVMVirtualMachine AttachedDriveTypes, propriété (VPCCOMInterfaces. h)
description: Tableau qui indique le type de lecteur attaché à chaque emplacement de la machine virtuelle.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- AttachedDriveTypes propriété Virtual PC
- AttachedDriveTypes, propriété Virtual PC, IVMVirtualMachine, interface
- IVMVirtualMachine interface Virtual PC, propriété AttachedDriveTypes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105655"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a><span data-ttu-id="103fd-106">IVMVirtualMachine :: AttachedDriveTypes, propriété</span><span class="sxs-lookup"><span data-stu-id="103fd-106">IVMVirtualMachine::AttachedDriveTypes property</span></span>

<span data-ttu-id="103fd-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="103fd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="103fd-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="103fd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="103fd-109">Récupère un tableau indiquant le type de lecteur attaché à chaque emplacement de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="103fd-109">Retrieves an array indicating the type of drive attached to each location in the virtual machine (VM).</span></span>

<span data-ttu-id="103fd-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="103fd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="103fd-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="103fd-111">Syntax</span></span>


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a><span data-ttu-id="103fd-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="103fd-112">Property value</span></span>

<span data-ttu-id="103fd-113">Variante de type VT **de \_ tableau** VT \| contenant des entrées de type **VT \_ UI1**. **\_**</span><span class="sxs-lookup"><span data-stu-id="103fd-113">A variant of type **VT\_ARRAY** \| **VT\_VARIANT** containing entries of type **VT\_UI1**.</span></span> <span data-ttu-id="103fd-114">Le tableau contient la valeur [**VMDriveType**](vmdrivetype.md) de chaque appareil connecté à chaque emplacement de bus.</span><span class="sxs-lookup"><span data-stu-id="103fd-114">The array contains the [**VMDriveType**](vmdrivetype.md) value of each device connected to every bus location.</span></span> <span data-ttu-id="103fd-115">Le tableau est trié par \[ *busNumber* \] \[ *deviceID* \] .</span><span class="sxs-lookup"><span data-stu-id="103fd-115">The array is ordered by \[*busNumber*\]\[*deviceID*\].</span></span>

## <a name="error-codes"></a><span data-ttu-id="103fd-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="103fd-116">Error codes</span></span>



| <span data-ttu-id="103fd-117">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="103fd-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="103fd-118">Signification</span><span class="sxs-lookup"><span data-stu-id="103fd-118">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="103fd-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="103fd-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="103fd-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="103fd-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="103fd-121"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="103fd-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="103fd-122">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="103fd-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="103fd-123"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="103fd-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="103fd-124">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="103fd-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="103fd-125"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="103fd-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="103fd-126">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="103fd-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="103fd-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="103fd-127">Requirements</span></span>



| <span data-ttu-id="103fd-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="103fd-128">Requirement</span></span> | <span data-ttu-id="103fd-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="103fd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="103fd-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="103fd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="103fd-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="103fd-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="103fd-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="103fd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="103fd-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="103fd-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="103fd-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="103fd-134">End of client support</span></span><br/>    | <span data-ttu-id="103fd-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="103fd-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="103fd-136">Produit</span><span class="sxs-lookup"><span data-stu-id="103fd-136">Product</span></span><br/>                  | <span data-ttu-id="103fd-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="103fd-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="103fd-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="103fd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="103fd-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="103fd-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="103fd-140">IID</span><span class="sxs-lookup"><span data-stu-id="103fd-140">IID</span></span><br/>                      | <span data-ttu-id="103fd-141">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="103fd-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="103fd-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="103fd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103fd-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="103fd-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

