---
title: Propriété IVMSerialPort Name (VPCCOMInterfaces. h)
description: Nom du port série.
ms.assetid: 4d3fe008-f089-4a1b-9c90-2e0b3ded58fa
keywords:
- Propriété de nom Virtual PC
- Propriété de nom Virtual PC, interface IVMSerialPort
- IVMSerialPort interface Virtual PC, propriété Name
topic_type:
- apiref
api_name:
- IVMSerialPort.Name
- IVMSerialPort.get_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 540540e2af91647b9c77735a1c601ed62aecdbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844146"
---
# <a name="ivmserialportname-property"></a><span data-ttu-id="595d2-106">IVMSerialPort :: Name, propriété</span><span class="sxs-lookup"><span data-stu-id="595d2-106">IVMSerialPort::Name property</span></span>

<span data-ttu-id="595d2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="595d2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="595d2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="595d2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="595d2-109">Récupère le nom du port série.</span><span class="sxs-lookup"><span data-stu-id="595d2-109">Retrieves the name of the serial port.</span></span>

<span data-ttu-id="595d2-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="595d2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="595d2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="595d2-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *portName
);
```



## <a name="property-value"></a><span data-ttu-id="595d2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="595d2-112">Property value</span></span>

<span data-ttu-id="595d2-113">Nom du port série.</span><span class="sxs-lookup"><span data-stu-id="595d2-113">The name of the serial port.</span></span> <span data-ttu-id="595d2-114">Par exemple, « COM1 » pour **vmSerialPort \_ appelait hostport**, « C : \\SerialPort.txt » pour **vmSerialPort \_ TextFile**, ou « \\ \\ *ServerName* \\ pipe \\ *pipeName*» pour **vmSerialPort \_ NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="595d2-114">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="595d2-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="595d2-115">Error codes</span></span>



| <span data-ttu-id="595d2-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="595d2-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="595d2-117">Signification</span><span class="sxs-lookup"><span data-stu-id="595d2-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="595d2-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="595d2-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="595d2-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="595d2-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="595d2-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="595d2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="595d2-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="595d2-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="595d2-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="595d2-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="595d2-123">La configuration de cet ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="595d2-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="595d2-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="595d2-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="595d2-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="595d2-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="595d2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="595d2-126">Requirements</span></span>



| <span data-ttu-id="595d2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="595d2-127">Requirement</span></span> | <span data-ttu-id="595d2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="595d2-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="595d2-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="595d2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="595d2-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="595d2-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="595d2-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="595d2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="595d2-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="595d2-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="595d2-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="595d2-133">End of client support</span></span><br/>    | <span data-ttu-id="595d2-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="595d2-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="595d2-135">Produit</span><span class="sxs-lookup"><span data-stu-id="595d2-135">Product</span></span><br/>                  | <span data-ttu-id="595d2-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="595d2-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="595d2-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="595d2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="595d2-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="595d2-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="595d2-139">IID</span><span class="sxs-lookup"><span data-stu-id="595d2-139">IID</span></span><br/>                      | <span data-ttu-id="595d2-140">IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815</span><span class="sxs-lookup"><span data-stu-id="595d2-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="595d2-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="595d2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="595d2-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="595d2-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

