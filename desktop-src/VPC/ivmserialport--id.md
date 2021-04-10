---
title: IVMSerialPort _ID, méthode (VPCCOMInterfaces. h)
description: Identificateur interne du port série.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- Méthode _ID Virtual PC
- _ID méthode Virtual PC, interface IVMSerialPort
- IVMSerialPort interface Virtual PC, méthode _ID
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103592"
---
# <a name="ivmserialport_id-method"></a><span data-ttu-id="b20c0-106">IVMSerialPort :: \_ ID, méthode</span><span class="sxs-lookup"><span data-stu-id="b20c0-106">IVMSerialPort::\_ID method</span></span>

<span data-ttu-id="b20c0-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b20c0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b20c0-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b20c0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b20c0-109">Récupère l’identificateur interne du port série.</span><span class="sxs-lookup"><span data-stu-id="b20c0-109">Retrieves the internal identifier of the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="b20c0-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b20c0-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="b20c0-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b20c0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20c0-112">*port* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b20c0-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b20c0-113">Identificateur du port série.</span><span class="sxs-lookup"><span data-stu-id="b20c0-113">The serial port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20c0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b20c0-114">Return value</span></span>

<span data-ttu-id="b20c0-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b20c0-115">This method can return one of these values.</span></span>



| <span data-ttu-id="b20c0-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b20c0-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="b20c0-117">Description</span><span class="sxs-lookup"><span data-stu-id="b20c0-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="b20c0-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b20c0-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b20c0-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="b20c0-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="b20c0-120"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b20c0-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b20c0-121">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b20c0-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="b20c0-122"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b20c0-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b20c0-123">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b20c0-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="b20c0-124"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="b20c0-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b20c0-125">La configuration de cet ordinateur virtuel n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b20c0-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b20c0-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b20c0-126">Remarks</span></span>

<span data-ttu-id="b20c0-127">Cette propriété n’est pas utilisable par les langages de script.</span><span class="sxs-lookup"><span data-stu-id="b20c0-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20c0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b20c0-128">Requirements</span></span>



| <span data-ttu-id="b20c0-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b20c0-129">Requirement</span></span> | <span data-ttu-id="b20c0-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b20c0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b20c0-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b20c0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b20c0-132">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b20c0-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b20c0-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b20c0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b20c0-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b20c0-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b20c0-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b20c0-135">End of client support</span></span><br/>    | <span data-ttu-id="b20c0-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b20c0-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b20c0-137">Produit</span><span class="sxs-lookup"><span data-stu-id="b20c0-137">Product</span></span><br/>                  | <span data-ttu-id="b20c0-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b20c0-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b20c0-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b20c0-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b20c0-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b20c0-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b20c0-141">IID</span><span class="sxs-lookup"><span data-stu-id="b20c0-141">IID</span></span><br/>                      | <span data-ttu-id="b20c0-142">IID \_ IVMSerialPort est défini en tant que 2ce4460d-1d3f-4458-BF8B-44084b816815</span><span class="sxs-lookup"><span data-stu-id="b20c0-142">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="b20c0-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b20c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20c0-144">**IVMSerialPort**</span><span class="sxs-lookup"><span data-stu-id="b20c0-144">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

