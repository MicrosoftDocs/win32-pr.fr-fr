---
title: Méthode INapEnforcementClientConnection GetMaxSize (NapEnforcementClient. h)
description: Obtient la taille maximale du paquet SoH pour ce client.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- Méthode GetMaxSize NAP
- Méthode GetMaxSize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d86cc71cd5da906146ab1577d58311d167d484
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740933"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a><span data-ttu-id="626c7-106">INapEnforcementClientConnection :: GetMaxSize, méthode</span><span class="sxs-lookup"><span data-stu-id="626c7-106">INapEnforcementClientConnection::GetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="626c7-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="626c7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="626c7-108">La méthode **INapEnforcementClientConnection :: GetMaxSize** obtient la taille maximale du paquet SOH pour ce client.</span><span class="sxs-lookup"><span data-stu-id="626c7-108">The **INapEnforcementClientConnection::GetMaxSize** method gets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="626c7-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="626c7-109">Syntax</span></span>


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="626c7-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="626c7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="626c7-111">*MaxSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="626c7-111">*maxSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="626c7-112">Pointeur vers un [**ProtocolMaxSize**](nap-datatypes.md) qui indique la taille maximale, en octets, du paquet SOH.</span><span class="sxs-lookup"><span data-stu-id="626c7-112">A pointer to a [**ProtocolMaxSize**](nap-datatypes.md) that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="626c7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="626c7-113">Return value</span></span>

<span data-ttu-id="626c7-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="626c7-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="626c7-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="626c7-115">Return code</span></span>                                                                                     | <span data-ttu-id="626c7-116">Description</span><span class="sxs-lookup"><span data-stu-id="626c7-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="626c7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="626c7-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="626c7-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="626c7-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="626c7-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="626c7-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="626c7-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="626c7-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="626c7-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="626c7-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="626c7-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="626c7-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="626c7-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="626c7-123">Requirements</span></span>



| <span data-ttu-id="626c7-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="626c7-124">Requirement</span></span> | <span data-ttu-id="626c7-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="626c7-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="626c7-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="626c7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="626c7-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="626c7-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="626c7-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="626c7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="626c7-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="626c7-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="626c7-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="626c7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="626c7-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="626c7-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="626c7-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="626c7-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="626c7-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="626c7-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="626c7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="626c7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="626c7-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="626c7-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="626c7-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="626c7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="626c7-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="626c7-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





