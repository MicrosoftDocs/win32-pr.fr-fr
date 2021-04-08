---
title: Méthode INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Recherche l’emplacement (index) de l’attribut suivant du type indiqué par SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- Méthode FindNextAttribute NAP
- Méthode FindNextAttribute NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, méthode FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740221"
---
# <a name="inapsohprocessorfindnextattribute-method"></a><span data-ttu-id="36741-106">INapSoHProcessor :: FindNextAttribute, méthode</span><span class="sxs-lookup"><span data-stu-id="36741-106">INapSoHProcessor::FindNextAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="36741-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="36741-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="36741-108">La méthode **INapSoHProcessor :: FindNextAttribute** recherche l’emplacement (index) de l’attribut suivant du type indiqué par *SoHAttributeType*.</span><span class="sxs-lookup"><span data-stu-id="36741-108">The **INapSoHProcessor::FindNextAttribute** method finds the location (index) of the next attribute of the type indicated by *SoHAttributeType*.</span></span>

## <a name="syntax"></a><span data-ttu-id="36741-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36741-109">Syntax</span></span>


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a><span data-ttu-id="36741-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36741-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36741-111">*fromLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36741-111">*fromLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36741-112">Emplacement de départ (index) dans le paquet de déclaration d’intégrité (SoH) à partir duquel commencer la recherche d’attribut.</span><span class="sxs-lookup"><span data-stu-id="36741-112">The starting location (index) in the Statement of Health (SoH) packet to begin the attribute search.</span></span> <span data-ttu-id="36741-113">Cette valeur doit être comprise entre 0 et (**numAttrib** -1) où **numAttrib** est récupéré à l’aide de [**INapSoHProcessor :: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span><span class="sxs-lookup"><span data-stu-id="36741-113">This value must be in the range of 0 to (**numAttrib** - 1) where **numAttrib** is retrieved using [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="36741-114">Le paquet SoH utilise des index d’attributs basés sur 0.</span><span class="sxs-lookup"><span data-stu-id="36741-114">The SoH packet uses 0-based attribute indices.</span></span>

 

</dd> <dt>

<span data-ttu-id="36741-115">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36741-115">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36741-116">Structure [**SoHAttributeType**](sohattributetype-enum.md) qui contient le type d’attribut à rechercher.</span><span class="sxs-lookup"><span data-stu-id="36741-116">An [**SoHAttributeType**](sohattributetype-enum.md) structure that contains the attribute type to locate.</span></span>

</dd> <dt>

<span data-ttu-id="36741-117">*attributeLocation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="36741-117">*attributeLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36741-118">Pointeur qui contient l’emplacement (index) dans le paquet SoH du premier attribut de type *SoHAttributeType* à partir de l’index *fromLocation*.</span><span class="sxs-lookup"><span data-stu-id="36741-118">A pointer that contains the location (index) in the SoH packet of the first attribute of type *SoHAttributeType* from the index *fromLocation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36741-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36741-119">Return value</span></span>

<span data-ttu-id="36741-120">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="36741-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="36741-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="36741-121">Return code</span></span>                                                                                            | <span data-ttu-id="36741-122">Description</span><span class="sxs-lookup"><span data-stu-id="36741-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="36741-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36741-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="36741-124">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="36741-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="36741-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="36741-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="36741-126">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="36741-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="36741-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="36741-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="36741-128">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="36741-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="36741-129"><dt>**\_fichier d' \_ erreur \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="36741-129"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="36741-130">Attribut introuvable.</span><span class="sxs-lookup"><span data-stu-id="36741-130">Attribute not found.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="36741-131">Notes</span><span class="sxs-lookup"><span data-stu-id="36741-131">Remarks</span></span>

<span data-ttu-id="36741-132">La méthode **FindNextAttribute** recherche les attributs de type *SoHAttributeType* à partir de l’index spécifié par *fromLocation* et une valeur supérieure jusqu’à ce qu’une correspondance soit trouvée.</span><span class="sxs-lookup"><span data-stu-id="36741-132">The **FindNextAttribute** method searches for attributes of type *SoHAttributeType* from the index specified by *fromLocation* and higher until a match is found.</span></span> <span data-ttu-id="36741-133">Si aucune correspondance n’est trouvée, le **fichier d’erreur \_ \_ \_ introuvable** est retourné.</span><span class="sxs-lookup"><span data-stu-id="36741-133">If no match is found, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="36741-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36741-134">Requirements</span></span>



| <span data-ttu-id="36741-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36741-135">Requirement</span></span> | <span data-ttu-id="36741-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="36741-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="36741-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36741-137">Minimum supported client</span></span><br/> | <span data-ttu-id="36741-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36741-138">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="36741-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36741-139">Minimum supported server</span></span><br/> | <span data-ttu-id="36741-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36741-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="36741-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="36741-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="36741-142"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="36741-142"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="36741-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="36741-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36741-144"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36741-144"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="36741-145">DLL</span><span class="sxs-lookup"><span data-stu-id="36741-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36741-146"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36741-146"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="36741-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36741-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36741-148">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="36741-148">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





