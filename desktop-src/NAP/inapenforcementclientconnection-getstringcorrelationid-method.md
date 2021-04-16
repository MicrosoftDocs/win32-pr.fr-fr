---
title: Méthode INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient. h)
description: Obtient la version de chaîne de l’ID utilisé pour corréler les demandes et les réponses.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Méthode GetStringCorrelationId NAP
- Méthode GetStringCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508442"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a><span data-ttu-id="51312-106">INapEnforcementClientConnection :: GetStringCorrelationId, méthode</span><span class="sxs-lookup"><span data-stu-id="51312-106">INapEnforcementClientConnection::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="51312-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="51312-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="51312-108">La méthode **INapEnforcementClientConnection :: GetStringCorrelationId** obtient la version de chaîne de l’ID utilisé pour corréler les demandes et les réponses.</span><span class="sxs-lookup"><span data-stu-id="51312-108">The **INapEnforcementClientConnection::GetStringCorrelationId** method gets the string version of the ID used to correlate requests and responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="51312-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51312-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="51312-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51312-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51312-111">*CorrelationId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="51312-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51312-112">Pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version sous forme de chaîne de l’ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid)de la connexion.</span><span class="sxs-lookup"><span data-stu-id="51312-112">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the string version of the connection's [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51312-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51312-113">Return value</span></span>

<span data-ttu-id="51312-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="51312-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="51312-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="51312-115">Return code</span></span>                                                                                     | <span data-ttu-id="51312-116">Description</span><span class="sxs-lookup"><span data-stu-id="51312-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="51312-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51312-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="51312-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="51312-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="51312-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="51312-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="51312-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="51312-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="51312-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="51312-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="51312-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="51312-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="51312-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51312-123">Requirements</span></span>



| <span data-ttu-id="51312-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51312-124">Requirement</span></span> | <span data-ttu-id="51312-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="51312-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51312-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51312-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51312-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51312-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="51312-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51312-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51312-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51312-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="51312-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="51312-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="51312-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="51312-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="51312-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="51312-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51312-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="51312-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="51312-134">DLL</span><span class="sxs-lookup"><span data-stu-id="51312-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51312-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51312-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="51312-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51312-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51312-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="51312-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





