---
title: Propriété de type IVMSerialPort (VPCCOMInterfaces. h)
description: Récupère le type du port série.
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- Propriété de type Virtual PC
- Propriété de type Virtual PC, IVMSerialPort, interface
- IVMSerialPort interface Virtual PC, type, propriété
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465538"
---
# <a name="ivmserialporttype-property"></a><span data-ttu-id="50d93-106">IVMSerialPort :: type, propriété</span><span class="sxs-lookup"><span data-stu-id="50d93-106">IVMSerialPort::Type property</span></span>

<span data-ttu-id="50d93-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50d93-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="50d93-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="50d93-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="50d93-109">Récupère le type du port série.</span><span class="sxs-lookup"><span data-stu-id="50d93-109">Retrieves the type of the serial port.</span></span>

<span data-ttu-id="50d93-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="50d93-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d93-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50d93-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a><span data-ttu-id="50d93-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="50d93-112">Property value</span></span>

<span data-ttu-id="50d93-113">Type de port série.</span><span class="sxs-lookup"><span data-stu-id="50d93-113">The type of serial port.</span></span> <span data-ttu-id="50d93-114">Pour obtenir la liste des valeurs, consultez [**VMSerialPortType**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="50d93-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="50d93-115">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="50d93-115">Error codes</span></span>



| <span data-ttu-id="50d93-116">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="50d93-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="50d93-117">Signification</span><span class="sxs-lookup"><span data-stu-id="50d93-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="50d93-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="50d93-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="50d93-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="50d93-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="50d93-120"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="50d93-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="50d93-121">Le paramètre a la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="50d93-121">The parameter is NULL.</span></span><br/>                                   |
| <dl> <span data-ttu-id="50d93-122"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="50d93-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="50d93-123">La configuration de cet ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="50d93-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="50d93-124"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="50d93-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="50d93-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="50d93-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="50d93-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50d93-126">Requirements</span></span>



| <span data-ttu-id="50d93-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50d93-127">Requirement</span></span> | <span data-ttu-id="50d93-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="50d93-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d93-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d93-129">Minimum supported client</span></span><br/> | <span data-ttu-id="50d93-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50d93-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50d93-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d93-131">Minimum supported server</span></span><br/> | <span data-ttu-id="50d93-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d93-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="50d93-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="50d93-133">End of client support</span></span><br/>    | <span data-ttu-id="50d93-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50d93-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="50d93-135">Produit</span><span class="sxs-lookup"><span data-stu-id="50d93-135">Product</span></span><br/>                  | <span data-ttu-id="50d93-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="50d93-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="50d93-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="50d93-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="50d93-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="50d93-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="50d93-139">IID</span><span class="sxs-lookup"><span data-stu-id="50d93-139">IID</span></span><br/>                      | <span data-ttu-id="50d93-140">IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815</span><span class="sxs-lookup"><span data-stu-id="50d93-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="50d93-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50d93-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d93-142">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="50d93-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

