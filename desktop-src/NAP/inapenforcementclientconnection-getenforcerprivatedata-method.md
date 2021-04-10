---
title: Méthode INapEnforcementClientConnection GetEnforcerPrivateData (NapEnforcementClient. h)
description: Est utilisé par l’application pour recevoir des données privées.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- Méthode GetEnforcerPrivateData NAP
- Méthode GetEnforcerPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106420"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a><span data-ttu-id="589f3-106">INapEnforcementClientConnection :: GetEnforcerPrivateData, méthode</span><span class="sxs-lookup"><span data-stu-id="589f3-106">INapEnforcementClientConnection::GetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="589f3-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="589f3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="589f3-108">La méthode **INapEnforcementClientConnection :: GetEnforcerPrivateData** est utilisée par l’application pour récupérer des données privées.</span><span class="sxs-lookup"><span data-stu-id="589f3-108">The **INapEnforcementClientConnection::GetEnforcerPrivateData** method is used by the enforcer to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="589f3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="589f3-109">Syntax</span></span>


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="589f3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="589f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="589f3-111">*privateData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="589f3-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="589f3-112">Pointeur vers un pointeur vers un objet blob de données opaques [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que seul l’application peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="589f3-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="589f3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="589f3-113">Return value</span></span>

<span data-ttu-id="589f3-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="589f3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="589f3-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="589f3-115">Return code</span></span>                                                                                     | <span data-ttu-id="589f3-116">Description</span><span class="sxs-lookup"><span data-stu-id="589f3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="589f3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="589f3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="589f3-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="589f3-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="589f3-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="589f3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="589f3-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="589f3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="589f3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="589f3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="589f3-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="589f3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="589f3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="589f3-123">Requirements</span></span>



| <span data-ttu-id="589f3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="589f3-124">Requirement</span></span> | <span data-ttu-id="589f3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="589f3-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="589f3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="589f3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="589f3-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="589f3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="589f3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="589f3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="589f3-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="589f3-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="589f3-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="589f3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="589f3-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="589f3-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="589f3-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="589f3-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="589f3-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="589f3-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="589f3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="589f3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="589f3-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="589f3-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="589f3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="589f3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="589f3-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="589f3-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





