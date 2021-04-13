---
title: Méthode INapSoHProcessor GetNumberOfAttributes (NapProtocol. h)
description: Récupère le nombre total d’attributs dans la SoH.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Méthode GetNumberOfAttributes NAP
- Méthode GetNumberOfAttributes NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, méthode GetNumberOfAttributes
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508570"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a><span data-ttu-id="40b88-106">INapSoHProcessor :: GetNumberOfAttributes, méthode</span><span class="sxs-lookup"><span data-stu-id="40b88-106">INapSoHProcessor::GetNumberOfAttributes method</span></span>

> [!Note]  
> <span data-ttu-id="40b88-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="40b88-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="40b88-108">La méthode **INapSoHProcessor :: GetNumberOfAttributes** récupère le nombre total d’attributs dans la SOH.</span><span class="sxs-lookup"><span data-stu-id="40b88-108">The **INapSoHProcessor::GetNumberOfAttributes** method retrieves the total number of attributes in the SoH.</span></span>

## <a name="syntax"></a><span data-ttu-id="40b88-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40b88-109">Syntax</span></span>


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a><span data-ttu-id="40b88-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40b88-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40b88-111">*attributeCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="40b88-111">*attributeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40b88-112">Pointeur vers le nombre d’attributs retourné.</span><span class="sxs-lookup"><span data-stu-id="40b88-112">A pointer to the returned attribute count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40b88-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40b88-113">Return value</span></span>

<span data-ttu-id="40b88-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="40b88-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="40b88-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="40b88-115">Return code</span></span>                                                                                     | <span data-ttu-id="40b88-116">Description</span><span class="sxs-lookup"><span data-stu-id="40b88-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="40b88-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="40b88-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="40b88-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="40b88-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="40b88-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="40b88-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="40b88-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="40b88-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="40b88-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="40b88-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="40b88-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="40b88-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="40b88-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40b88-123">Requirements</span></span>



| <span data-ttu-id="40b88-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40b88-124">Requirement</span></span> | <span data-ttu-id="40b88-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="40b88-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="40b88-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40b88-126">Minimum supported client</span></span><br/> | <span data-ttu-id="40b88-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40b88-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="40b88-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40b88-128">Minimum supported server</span></span><br/> | <span data-ttu-id="40b88-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40b88-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="40b88-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="40b88-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="40b88-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="40b88-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="40b88-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="40b88-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="40b88-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="40b88-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="40b88-134">DLL</span><span class="sxs-lookup"><span data-stu-id="40b88-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40b88-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40b88-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="40b88-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40b88-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40b88-137">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="40b88-137">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





