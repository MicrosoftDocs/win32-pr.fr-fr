---
title: IVMSerialPort ConnectImmediately, propriété (VPCCOMInterfaces. h)
description: Détermine si le port série doit être ouvert sans attendre la réception d’une commande de modem.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- ConnectImmediately propriété Virtual PC
- ConnectImmediately, propriété Virtual PC, IVMSerialPort, interface
- IVMSerialPort interface Virtual PC, propriété ConnectImmediately
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741741"
---
# <a name="ivmserialportconnectimmediately-property"></a><span data-ttu-id="07ea7-106">IVMSerialPort :: ConnectImmediately, propriété</span><span class="sxs-lookup"><span data-stu-id="07ea7-106">IVMSerialPort::ConnectImmediately property</span></span>

<span data-ttu-id="07ea7-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="07ea7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="07ea7-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="07ea7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="07ea7-109">Détermine si le port série doit être ouvert sans attendre la réception d’une commande de modem.</span><span class="sxs-lookup"><span data-stu-id="07ea7-109">Determines whether the serial port should be opened without waiting for a modem command to be received.</span></span>

<span data-ttu-id="07ea7-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="07ea7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ea7-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07ea7-111">Syntax</span></span>


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a><span data-ttu-id="07ea7-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="07ea7-112">Property value</span></span>

<span data-ttu-id="07ea7-113">**Variante \_ TRUE** si le port série doit être ouvert sans attendre la réception d’une commande de modem ; **Variante \_ FALSe** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="07ea7-113">**VARIANT\_TRUE** if the serial port should be opened without waiting for a modem command to be received; **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07ea7-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="07ea7-114">Error codes</span></span>



| <span data-ttu-id="07ea7-115">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="07ea7-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="07ea7-116">Signification</span><span class="sxs-lookup"><span data-stu-id="07ea7-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="07ea7-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="07ea7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="07ea7-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="07ea7-118">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="07ea7-119"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="07ea7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="07ea7-120">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="07ea7-120">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="07ea7-121"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ </dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="07ea7-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="07ea7-122">La configuration de cet ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="07ea7-122">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="07ea7-123"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="07ea7-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="07ea7-124">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="07ea7-124">An unexpected error has occurred.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="07ea7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="07ea7-125">Remarks</span></span>

<span data-ttu-id="07ea7-126">Cette propriété est valide uniquement si la propriété de [**type**](ivmserialport-type.md) de port est **vmSerialPort \_ appelait hostport**.</span><span class="sxs-lookup"><span data-stu-id="07ea7-126">This property is valid only if the port [**Type**](ivmserialport-type.md) property is **vmSerialPort\_HostPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07ea7-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07ea7-127">Requirements</span></span>



| <span data-ttu-id="07ea7-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07ea7-128">Requirement</span></span> | <span data-ttu-id="07ea7-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="07ea7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="07ea7-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07ea7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="07ea7-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07ea7-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07ea7-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07ea7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="07ea7-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="07ea7-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="07ea7-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="07ea7-134">End of client support</span></span><br/>    | <span data-ttu-id="07ea7-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07ea7-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="07ea7-136">Produit</span><span class="sxs-lookup"><span data-stu-id="07ea7-136">Product</span></span><br/>                  | <span data-ttu-id="07ea7-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="07ea7-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="07ea7-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="07ea7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="07ea7-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="07ea7-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="07ea7-140">IID</span><span class="sxs-lookup"><span data-stu-id="07ea7-140">IID</span></span><br/>                      | <span data-ttu-id="07ea7-141">IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815</span><span class="sxs-lookup"><span data-stu-id="07ea7-141">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="07ea7-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07ea7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ea7-143">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="07ea7-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

