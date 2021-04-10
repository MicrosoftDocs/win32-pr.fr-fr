---
title: Méthode INapEnforcementClientConnection GetConnectionID, (NapEnforcementClient. h)
description: Est utilisé pour récupérer l’ID de connexion unique du client.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- Méthode GetConnectionID, NAP
- Méthode GetConnectionID, NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetConnectionID,
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106426"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a><span data-ttu-id="707b1-106">INapEnforcementClientConnection :: GetConnectionID,, méthode</span><span class="sxs-lookup"><span data-stu-id="707b1-106">INapEnforcementClientConnection::GetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="707b1-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="707b1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="707b1-108">La méthode **INapEnforcementClientConnection :: GetConnectionID,** permet d’accéder à l’ID de connexion unique du client.</span><span class="sxs-lookup"><span data-stu-id="707b1-108">The **INapEnforcementClientConnection::GetConnectionId** method is used to get the unique connection ID of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="707b1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="707b1-109">Syntax</span></span>


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="707b1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="707b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="707b1-111">*ID* \[ de la à\]</span><span class="sxs-lookup"><span data-stu-id="707b1-111">*connectionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="707b1-112">Pointeur vers un pointeur vers un [**ID**](nap-datatypes.md) de connexion qui identifie de façon unique cette connexion.</span><span class="sxs-lookup"><span data-stu-id="707b1-112">A pointer to a pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies this connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="707b1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="707b1-113">Return value</span></span>

<span data-ttu-id="707b1-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="707b1-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="707b1-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="707b1-115">Return code</span></span>                                                                                     | <span data-ttu-id="707b1-116">Description</span><span class="sxs-lookup"><span data-stu-id="707b1-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="707b1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="707b1-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="707b1-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="707b1-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="707b1-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="707b1-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="707b1-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="707b1-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="707b1-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="707b1-123">Notes</span><span class="sxs-lookup"><span data-stu-id="707b1-123">Remarks</span></span>

<span data-ttu-id="707b1-124">L’ID de connexion est principalement utilisé à des fins de journalisation.</span><span class="sxs-lookup"><span data-stu-id="707b1-124">The connection ID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="707b1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="707b1-125">Requirements</span></span>



| <span data-ttu-id="707b1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="707b1-126">Requirement</span></span> | <span data-ttu-id="707b1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="707b1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="707b1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707b1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="707b1-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707b1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="707b1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707b1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="707b1-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707b1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="707b1-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="707b1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="707b1-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="707b1-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="707b1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="707b1-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="707b1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="707b1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="707b1-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="707b1-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="707b1-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="707b1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707b1-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="707b1-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





