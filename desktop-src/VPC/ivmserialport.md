---
title: Interface IVMSerialPort (VPCCOMInterfaces. h)
description: Définit un port série à l’intérieur d’une machine virtuelle.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Virtual PC de l’interface IVMSerialPort
- IVMSerialPort interface Virtual PC, Description
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508986"
---
# <a name="ivmserialport-interface"></a><span data-ttu-id="27957-105">Interface IVMSerialPort</span><span class="sxs-lookup"><span data-stu-id="27957-105">IVMSerialPort interface</span></span>

<span data-ttu-id="27957-106">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27957-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27957-107">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27957-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27957-108">Définit un port série à l’intérieur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="27957-108">Defines a serial port inside a virtual machine.</span></span> <span data-ttu-id="27957-109">Cette interface vous permet de configurer des ports série à l’intérieur d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="27957-109">This interface allows you to configure serial ports inside a virtual machine.</span></span> <span data-ttu-id="27957-110">Vous pouvez récupérer un objet **IVMSerialPort** à partir de l’objet [**IVMSerialPortCollection**](ivmserialportcollection.md) retourné à partir de la propriété [**IVMVirtualMachine :: SerialPorts**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="27957-110">You can retrieve an **IVMSerialPort** object from the [**IVMSerialPortCollection**](ivmserialportcollection.md) object returned from the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="27957-111">Membres</span><span class="sxs-lookup"><span data-stu-id="27957-111">Members</span></span>

<span data-ttu-id="27957-112">L’interface **IVMSerialPort** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="27957-112">The **IVMSerialPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="27957-113">**IVMSerialPort** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="27957-113">**IVMSerialPort** also has these types of members:</span></span>

-   [<span data-ttu-id="27957-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="27957-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="27957-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="27957-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="27957-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="27957-116">Methods</span></span>

<span data-ttu-id="27957-117">L’interface **IVMSerialPort** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="27957-117">The **IVMSerialPort** interface has these methods.</span></span>



| <span data-ttu-id="27957-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="27957-118">Method</span></span>                                       | <span data-ttu-id="27957-119">Description</span><span class="sxs-lookup"><span data-stu-id="27957-119">Description</span></span>                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="27957-120">**\_IDENTIFI**</span><span class="sxs-lookup"><span data-stu-id="27957-120">**\_ID**</span></span>](ivmserialport--id.md)            | <span data-ttu-id="27957-121">Récupère l’identificateur interne du port série.</span><span class="sxs-lookup"><span data-stu-id="27957-121">Retrieves the internal identifier of the serial port.</span></span><br/> |
| [<span data-ttu-id="27957-122">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="27957-122">**Configure**</span></span>](ivmserialport-configure.md) | <span data-ttu-id="27957-123">Configure le port série.</span><span class="sxs-lookup"><span data-stu-id="27957-123">Configures the serial port.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="27957-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="27957-124">Properties</span></span>

<span data-ttu-id="27957-125">L’interface **IVMSerialPort** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="27957-125">The **IVMSerialPort** interface has these properties.</span></span>



| <span data-ttu-id="27957-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="27957-126">Property</span></span>                                                                  | <span data-ttu-id="27957-127">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="27957-127">Access type</span></span>          | <span data-ttu-id="27957-128">Description</span><span class="sxs-lookup"><span data-stu-id="27957-128">Description</span></span>                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27957-129">**ConnectImmediately**</span><span class="sxs-lookup"><span data-stu-id="27957-129">**ConnectImmediately**</span></span>](ivmserialport-connectimmediately.md)<br/> | <span data-ttu-id="27957-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27957-130">Read-only</span></span><br/> | <span data-ttu-id="27957-131">Indique si le port série doit être ouvert sans attendre la réception d’une commande de modem.</span><span class="sxs-lookup"><span data-stu-id="27957-131">Indicates whether the serial port should be opened without waiting for a modem command to be received.</span></span><br/> |
| [<span data-ttu-id="27957-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="27957-132">**Name**</span></span>](ivmserialport-name.md)<br/>                             | <span data-ttu-id="27957-133">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27957-133">Read-only</span></span><br/> | <span data-ttu-id="27957-134">Nom du port série.</span><span class="sxs-lookup"><span data-stu-id="27957-134">The name of the serial port.</span></span><br/>                                                                           |
| [<span data-ttu-id="27957-135">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="27957-135">**Type**</span></span>](ivmserialport-type.md)<br/>                             | <span data-ttu-id="27957-136">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="27957-136">Read-only</span></span><br/> | <span data-ttu-id="27957-137">Type du port série.</span><span class="sxs-lookup"><span data-stu-id="27957-137">The type of the serial port.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="27957-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27957-138">Requirements</span></span>



| <span data-ttu-id="27957-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="27957-139">Requirement</span></span> | <span data-ttu-id="27957-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="27957-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27957-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27957-141">Minimum supported client</span></span><br/> | <span data-ttu-id="27957-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="27957-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27957-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="27957-143">Minimum supported server</span></span><br/> | <span data-ttu-id="27957-144">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="27957-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27957-145">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="27957-145">End of client support</span></span><br/>    | <span data-ttu-id="27957-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27957-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27957-147">Produit</span><span class="sxs-lookup"><span data-stu-id="27957-147">Product</span></span><br/>                  | <span data-ttu-id="27957-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27957-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27957-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="27957-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="27957-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="27957-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27957-151">IID</span><span class="sxs-lookup"><span data-stu-id="27957-151">IID</span></span><br/>                      | <span data-ttu-id="27957-152">IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815</span><span class="sxs-lookup"><span data-stu-id="27957-152">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



 

