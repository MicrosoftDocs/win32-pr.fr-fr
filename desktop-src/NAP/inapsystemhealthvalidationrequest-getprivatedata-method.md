---
title: Méthode INapSystemHealthValidationRequest GetPrivateData (NapSystemHealthValidator. h)
description: Autorise le NapServer à récupérer des informations d’État.
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- Méthode GetPrivateData NAP
- Méthode GetPrivateData NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode GetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d78cceba42cd503ef8a875ece8f4ed196eaeff8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743348"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a><span data-ttu-id="c18c0-106">INapSystemHealthValidationRequest :: GetPrivateData, méthode</span><span class="sxs-lookup"><span data-stu-id="c18c0-106">INapSystemHealthValidationRequest::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="c18c0-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c18c0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c18c0-108">La méthode **INapSystemHealthValidationRequest :: GetPrivateData** permet au NapServer de récupérer des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="c18c0-108">The **INapSystemHealthValidationRequest::GetPrivateData** method allows the NapServer to retrieve state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c18c0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c18c0-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="c18c0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c18c0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c18c0-111">*privateData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c18c0-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c18c0-112">Pointeur vers un pointeur vers un objet blob de données opaques [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) qui contient des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="c18c0-112">A pointer to a pointer to [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that contains state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c18c0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c18c0-113">Return value</span></span>

<span data-ttu-id="c18c0-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="c18c0-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c18c0-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c18c0-115">Return code</span></span>                                                                                     | <span data-ttu-id="c18c0-116">Description</span><span class="sxs-lookup"><span data-stu-id="c18c0-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c18c0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c18c0-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c18c0-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="c18c0-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c18c0-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c18c0-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c18c0-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="c18c0-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c18c0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c18c0-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c18c0-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="c18c0-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c18c0-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c18c0-123">Remarks</span></span>

<span data-ttu-id="c18c0-124">Seul le NapServer peut interpréter l’objet blob de données.</span><span class="sxs-lookup"><span data-stu-id="c18c0-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="c18c0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c18c0-125">Requirements</span></span>



| <span data-ttu-id="c18c0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c18c0-126">Requirement</span></span> | <span data-ttu-id="c18c0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c18c0-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c18c0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c18c0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c18c0-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c18c0-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="c18c0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c18c0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c18c0-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c18c0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c18c0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c18c0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c18c0-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="c18c0-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="c18c0-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="c18c0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c18c0-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c18c0-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="c18c0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c18c0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c18c0-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c18c0-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="c18c0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c18c0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c18c0-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="c18c0-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





