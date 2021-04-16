---
title: Méthode INapSoHConstructor AppendAttribute (NapProtocol. h)
description: Ajoute un TLV à la fin de la mémoire tampon SoH.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- Méthode AppendAttribute NAP
- Méthode AppendAttribute NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, méthode AppendAttribute
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508529"
---
# <a name="inapsohconstructorappendattribute-method"></a><span data-ttu-id="813d6-106">INapSoHConstructor :: AppendAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="813d6-106">INapSoHConstructor::AppendAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="813d6-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="813d6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="813d6-108">La méthode **INapSoHConstructor :: AppendAttribute** ajoute un TLV à la fin de la mémoire tampon SOH.</span><span class="sxs-lookup"><span data-stu-id="813d6-108">The **INapSoHConstructor::AppendAttribute** method adds a TLV to the end of the SoH buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="813d6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="813d6-109">Syntax</span></span>


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="813d6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="813d6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="813d6-111">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="813d6-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="813d6-112">Énumération [**SoHAttributeType**](sohattributetype-enum.md) qui indique le type d’attribut du nouvel TLV.</span><span class="sxs-lookup"><span data-stu-id="813d6-112">A [**SoHAttributeType**](sohattributetype-enum.md) enumeration that indicates the attribute type of the new TLV.</span></span>

</dd> <dt>

<span data-ttu-id="813d6-113">*valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="813d6-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="813d6-114">Pointeur vers une structure [**SoHAttributeValue**](sohattributevalue-union.md) qui contient la valeur de la nouvelle TLV.</span><span class="sxs-lookup"><span data-stu-id="813d6-114">A pointer to an [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the value for the new TLV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="813d6-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="813d6-115">Return value</span></span>

<span data-ttu-id="813d6-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="813d6-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="813d6-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="813d6-117">Return code</span></span>                                                                                     | <span data-ttu-id="813d6-118">Description</span><span class="sxs-lookup"><span data-stu-id="813d6-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="813d6-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="813d6-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="813d6-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="813d6-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="813d6-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="813d6-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="813d6-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="813d6-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="813d6-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="813d6-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="813d6-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="813d6-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="813d6-125">Notes</span><span class="sxs-lookup"><span data-stu-id="813d6-125">Remarks</span></span>

<span data-ttu-id="813d6-126">Le [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV ne doit pas être ajouté à l’aide de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="813d6-126">The [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV must not be added using this function.</span></span> <span data-ttu-id="813d6-127">Il est ajouté comme premier TLV par [**INapSoHConstructor :: Initialize**](inapsohconstructor-initialize-method.md) aux paquets SOH nouvellement construits.</span><span class="sxs-lookup"><span data-stu-id="813d6-127">It is added as the first TLV by [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) to newly constructed SOH packets.</span></span>

<span data-ttu-id="813d6-128">Lors de l’ajout d’un attribut qui sera consommé par le système NAP, il ne doit pas être chiffré ou modifié de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="813d6-128">When appending an attribute which will be consumed by the Nap System, it should not be encrypted or modified in any manner.</span></span> <span data-ttu-id="813d6-129">Si le HealthEntity requiert le chiffrement/la vérification de l’intégrité (Mac) des informations privées, il doit être inclus uniquement dans l’attribut [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="813d6-129">If the HealthEntity requires encryption/integrity checking (MACs) of private information, it should be included only in the [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="813d6-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="813d6-130">Requirements</span></span>



| <span data-ttu-id="813d6-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="813d6-131">Requirement</span></span> | <span data-ttu-id="813d6-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="813d6-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="813d6-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="813d6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="813d6-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="813d6-134">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="813d6-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="813d6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="813d6-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="813d6-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="813d6-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="813d6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="813d6-138"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="813d6-138"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="813d6-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="813d6-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="813d6-140"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="813d6-140"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="813d6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="813d6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="813d6-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="813d6-142"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="813d6-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="813d6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="813d6-144">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="813d6-144">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





