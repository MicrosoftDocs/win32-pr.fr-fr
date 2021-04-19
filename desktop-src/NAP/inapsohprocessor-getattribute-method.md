---
title: INapSoHProcessor GetAttribute, méthode (NapProtocol. h)
description: Récupère le type et la valeur d’attribut, en fonction de l’emplacement de l’attribut.
ms.assetid: 0d7bc655-428b-4a31-b03f-445e80a6d194
keywords:
- Méthode GetAttribute NAP
- GetAttribute, méthode NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, GetAttribute, méthode
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2d7d9cbafa5a44e0f6c24f4c42959c456722a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513580"
---
# <a name="inapsohprocessorgetattribute-method"></a><span data-ttu-id="f7517-106">INapSoHProcessor :: GetAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="f7517-106">INapSoHProcessor::GetAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="f7517-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f7517-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f7517-108">La méthode **INapSoHProcessor :: GetAttribute** récupère le type et la valeur de l’attribut, en fonction de l’emplacement de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="f7517-108">The **INapSoHProcessor::GetAttribute** method retrieves the attribute type and value, given the attribute location.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7517-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7517-109">Syntax</span></span>


```C++
HRESULT GetAttribute(
  [in]  UINT16            attributeLocation,
  [out] SoHAttributeType  *type,
  [out] SoHAttributeValue **value
);
```



## <a name="parameters"></a><span data-ttu-id="f7517-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7517-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7517-111">*attributeLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7517-111">*attributeLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7517-112">Emplacement (index) de l’attribut dont le type et la valeur doivent être récupérés.</span><span class="sxs-lookup"><span data-stu-id="f7517-112">The location (index) of the attribute whose type and value are to be retrieved.</span></span> <span data-ttu-id="f7517-113">La valeur de *attributeLocation* est retournée à partir d’un appel antérieur à [**INapSoHProcessor :: FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span><span class="sxs-lookup"><span data-stu-id="f7517-113">The value of *attributeLocation* is returned from a prior call to [**INapSoHProcessor::FindNextAttribute**](inapsohprocessor-findnextattribute-method.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7517-114">*type* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f7517-114">*type* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7517-115">Pointeur vers une structure [**SoHAttributeType**](sohattributetype-enum.md) qui spécifie le type de l’attribut dans *valeur*.</span><span class="sxs-lookup"><span data-stu-id="f7517-115">A pointer to an [**SoHAttributeType**](sohattributetype-enum.md) structure that specifies the attribute's type in *value*.</span></span>

</dd> <dt>

<span data-ttu-id="f7517-116">*valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f7517-116">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7517-117">Pointeur vers un pointeur vers une structure [**SoHAttributeValue**](sohattributevalue-union.md) qui contient la valeur de l’attribut, telle que définie par le *type*.</span><span class="sxs-lookup"><span data-stu-id="f7517-117">A pointer to a pointer to a [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the attribute's value as defined by *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7517-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7517-118">Return value</span></span>

<span data-ttu-id="f7517-119">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="f7517-119">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f7517-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f7517-120">Return code</span></span>                                                                                     | <span data-ttu-id="f7517-121">Description</span><span class="sxs-lookup"><span data-stu-id="f7517-121">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7517-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f7517-122"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f7517-123">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="f7517-123">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f7517-124"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f7517-124"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f7517-125">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="f7517-125">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f7517-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f7517-126"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f7517-127">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f7517-127">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f7517-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7517-128">Requirements</span></span>



| <span data-ttu-id="f7517-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7517-129">Requirement</span></span> | <span data-ttu-id="f7517-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7517-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7517-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7517-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f7517-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7517-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f7517-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7517-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f7517-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7517-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f7517-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7517-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7517-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7517-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7517-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="f7517-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7517-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7517-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7517-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f7517-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7517-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7517-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="f7517-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7517-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7517-142">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="f7517-142">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





