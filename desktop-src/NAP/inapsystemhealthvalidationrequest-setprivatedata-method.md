---
title: Méthode INapSystemHealthValidationRequest SetPrivateData (NapSystemHealthValidator. h)
description: Permet au NapServer de stocker des informations d’État.
ms.assetid: 128f9beb-e5da-4b20-bf5e-fcf064209da3
keywords:
- Méthode SetPrivateData NAP
- Méthode SetPrivateData NAP, interface INapSystemHealthValidationRequest
- INapSystemHealthValidationRequest interface NAP, méthode SetPrivateData
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da50ca236c08388632e17916decee162b3b71743
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742221"
---
# <a name="inapsystemhealthvalidationrequestsetprivatedata-method"></a><span data-ttu-id="47a52-106">INapSystemHealthValidationRequest :: SetPrivateData, méthode</span><span class="sxs-lookup"><span data-stu-id="47a52-106">INapSystemHealthValidationRequest::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="47a52-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="47a52-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="47a52-108">La méthode **INapSystemHealthValidationRequest :: SetPrivateData** permet au NapServer de stocker des informations d’État.</span><span class="sxs-lookup"><span data-stu-id="47a52-108">The **INapSystemHealthValidationRequest::SetPrivateData** method allows the NapServer to store state information.</span></span>

## <a name="syntax"></a><span data-ttu-id="47a52-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47a52-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="47a52-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47a52-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a52-111">*privateData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47a52-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47a52-112">Pointeur vers un objet blob de données [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) qui contient les informations d’État opaques.</span><span class="sxs-lookup"><span data-stu-id="47a52-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that contains the opaque state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47a52-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47a52-113">Return value</span></span>

<span data-ttu-id="47a52-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="47a52-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="47a52-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="47a52-115">Return code</span></span>                                                                                     | <span data-ttu-id="47a52-116">Description</span><span class="sxs-lookup"><span data-stu-id="47a52-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="47a52-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47a52-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="47a52-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="47a52-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="47a52-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="47a52-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="47a52-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="47a52-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="47a52-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="47a52-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="47a52-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="47a52-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47a52-123">Notes</span><span class="sxs-lookup"><span data-stu-id="47a52-123">Remarks</span></span>

<span data-ttu-id="47a52-124">Seul le NapServer peut interpréter l’objet blob de données.</span><span class="sxs-lookup"><span data-stu-id="47a52-124">Only the NapServer can interpret the data blob.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a52-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47a52-125">Requirements</span></span>



| <span data-ttu-id="47a52-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47a52-126">Requirement</span></span> | <span data-ttu-id="47a52-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="47a52-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a52-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47a52-128">Minimum supported client</span></span><br/> | <span data-ttu-id="47a52-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="47a52-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="47a52-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47a52-130">Minimum supported server</span></span><br/> | <span data-ttu-id="47a52-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47a52-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47a52-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="47a52-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="47a52-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="47a52-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="47a52-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="47a52-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47a52-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47a52-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="47a52-136">DLL</span><span class="sxs-lookup"><span data-stu-id="47a52-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47a52-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47a52-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="47a52-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47a52-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a52-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="47a52-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





