---
title: Interface IVMSerialPortCollection (VPCCOMInterfaces. h)
description: Définit la collection de ports série au sein de la machine virtuelle. Pour obtenir un objet IVMSerialPortCollection, utilisez la propriété SerialPorts IVMVirtualMachine.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Virtual PC de l’interface IVMSerialPortCollection
- IVMSerialPortCollection interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741740"
---
# <a name="ivmserialportcollection-interface"></a><span data-ttu-id="7a025-106">Interface IVMSerialPortCollection</span><span class="sxs-lookup"><span data-stu-id="7a025-106">IVMSerialPortCollection interface</span></span>

<span data-ttu-id="7a025-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a025-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7a025-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7a025-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7a025-109">Définit la collection de ports série au sein de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="7a025-109">Defines the collection of serial ports within the virtual machine.</span></span> <span data-ttu-id="7a025-110">Pour obtenir un objet **IVMSerialPortCollection** , utilisez la propriété [**IVMVirtualMachine :: SerialPorts**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="7a025-110">To obtain an **IVMSerialPortCollection** object, use the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="7a025-111">Membres</span><span class="sxs-lookup"><span data-stu-id="7a025-111">Members</span></span>

<span data-ttu-id="7a025-112">L’interface **IVMSerialPortCollection** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7a025-112">The **IVMSerialPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="7a025-113">**IVMSerialPortCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7a025-113">**IVMSerialPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="7a025-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7a025-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a025-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7a025-115">Properties</span></span>

<span data-ttu-id="7a025-116">L’interface **IVMSerialPortCollection** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7a025-116">The **IVMSerialPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="7a025-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="7a025-117">Property</span></span>                                                         | <span data-ttu-id="7a025-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="7a025-118">Access type</span></span>          | <span data-ttu-id="7a025-119">Description</span><span class="sxs-lookup"><span data-stu-id="7a025-119">Description</span></span>                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="7a025-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="7a025-120">**\_NewEnum**</span></span>](ivmserialportcollection--newenum.md)<br/> | <span data-ttu-id="7a025-121">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a025-121">Read-only</span></span><br/> | <span data-ttu-id="7a025-122">Énumérateur de la collection.</span><span class="sxs-lookup"><span data-stu-id="7a025-122">An enumerator for the collection.</span></span><br/>                               |
| [<span data-ttu-id="7a025-123">**Saut**</span><span class="sxs-lookup"><span data-stu-id="7a025-123">**Count**</span></span>](ivmserialportcollection-count.md)<br/>        | <span data-ttu-id="7a025-124">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a025-124">Read-only</span></span><br/> | <span data-ttu-id="7a025-125">Nombre de ports série dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="7a025-125">The number of serial ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="7a025-126">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7a025-126">**Item**</span></span>](ivmserialportcollection-item.md)<br/>          | <span data-ttu-id="7a025-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7a025-127">Read-only</span></span><br/> | <span data-ttu-id="7a025-128">Objet de port série qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="7a025-128">The serial port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7a025-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a025-129">Requirements</span></span>



| <span data-ttu-id="7a025-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a025-130">Requirement</span></span> | <span data-ttu-id="7a025-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a025-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a025-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a025-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7a025-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7a025-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a025-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a025-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7a025-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a025-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7a025-136">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7a025-136">End of client support</span></span><br/>    | <span data-ttu-id="7a025-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a025-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a025-138">Produit</span><span class="sxs-lookup"><span data-stu-id="7a025-138">Product</span></span><br/>                  | <span data-ttu-id="7a025-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7a025-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7a025-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a025-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a025-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a025-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7a025-142">IID</span><span class="sxs-lookup"><span data-stu-id="7a025-142">IID</span></span><br/>                      | <span data-ttu-id="7a025-143">IID \_ IVMSerialPortCollection est défini en tant que dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="7a025-143">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="7a025-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a025-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a025-145">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="7a025-145">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="7a025-146">**IVMVirtualMachine::SerialPorts**</span><span class="sxs-lookup"><span data-stu-id="7a025-146">**IVMVirtualMachine::SerialPorts**</span></span>](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

