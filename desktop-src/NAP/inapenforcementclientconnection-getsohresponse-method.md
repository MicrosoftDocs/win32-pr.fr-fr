---
title: Méthode INapEnforcementClientConnection GetSoHResponse (NapEnforcementClient. h)
description: Obtient le SoH-Response reçu par le client de mise en œuvre.
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- Méthode GetSoHResponse NAP
- Méthode GetSoHResponse NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843329"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a><span data-ttu-id="c71cc-106">INapEnforcementClientConnection :: GetSoHResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="c71cc-106">INapEnforcementClientConnection::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="c71cc-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c71cc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c71cc-108">La méthode **INapEnforcementClientConnection :: GetSoHResponse** obtient le SoH-Response reçu par le client de mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="c71cc-108">The **INapEnforcementClientConnection::GetSoHResponse** method gets the SoH-Response received by the enforcement client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c71cc-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c71cc-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="c71cc-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c71cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c71cc-111">*sohResponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c71cc-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c71cc-112">Pointeur vers un pointeur vers une structure [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) unique, qui est un objet blob de données opaque pour l’application.</span><span class="sxs-lookup"><span data-stu-id="c71cc-112">A pointer to a pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c71cc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c71cc-113">Return value</span></span>

<span data-ttu-id="c71cc-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="c71cc-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c71cc-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c71cc-115">Return code</span></span>                                                                                     | <span data-ttu-id="c71cc-116">Description</span><span class="sxs-lookup"><span data-stu-id="c71cc-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c71cc-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c71cc-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c71cc-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="c71cc-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c71cc-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c71cc-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c71cc-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="c71cc-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c71cc-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c71cc-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c71cc-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="c71cc-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c71cc-123">Notes</span><span class="sxs-lookup"><span data-stu-id="c71cc-123">Remarks</span></span>

<span data-ttu-id="c71cc-124">Un paquet de taille de zéro octet est valide.</span><span class="sxs-lookup"><span data-stu-id="c71cc-124">A zero-byte sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="c71cc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c71cc-125">Requirements</span></span>



| <span data-ttu-id="c71cc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c71cc-126">Requirement</span></span> | <span data-ttu-id="c71cc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c71cc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c71cc-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c71cc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c71cc-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c71cc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c71cc-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c71cc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c71cc-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c71cc-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c71cc-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="c71cc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c71cc-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c71cc-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c71cc-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="c71cc-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c71cc-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c71cc-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="c71cc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c71cc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c71cc-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c71cc-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c71cc-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c71cc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c71cc-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="c71cc-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





