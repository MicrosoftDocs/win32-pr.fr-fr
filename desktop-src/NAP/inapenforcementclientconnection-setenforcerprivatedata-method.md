---
title: Méthode INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient. h)
description: Est utilisé par l’application pour définir des données privées.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Méthode SetEnforcerPrivateData NAP
- Méthode SetEnforcerPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetEnforcerPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032654"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a><span data-ttu-id="52d9c-106">INapEnforcementClientConnection :: SetEnforcerPrivateData, méthode</span><span class="sxs-lookup"><span data-stu-id="52d9c-106">INapEnforcementClientConnection::SetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="52d9c-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="52d9c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="52d9c-108">La méthode **INapEnforcementClientConnection :: SetEnforcerPrivateData** est utilisée par l’application pour définir des données privées.</span><span class="sxs-lookup"><span data-stu-id="52d9c-108">The **INapEnforcementClientConnection::SetEnforcerPrivateData** method is used by the enforcer to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d9c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52d9c-109">Syntax</span></span>


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="52d9c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52d9c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52d9c-111">*privateData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52d9c-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52d9c-112">Pointeur vers un objet blob de données opaques [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que seul l’application peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="52d9c-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52d9c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52d9c-113">Return value</span></span>

<span data-ttu-id="52d9c-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="52d9c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="52d9c-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="52d9c-115">Return code</span></span>                                                                                     | <span data-ttu-id="52d9c-116">Description</span><span class="sxs-lookup"><span data-stu-id="52d9c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="52d9c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="52d9c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="52d9c-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="52d9c-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="52d9c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="52d9c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="52d9c-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="52d9c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="52d9c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="52d9c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="52d9c-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="52d9c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="52d9c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52d9c-123">Requirements</span></span>



| <span data-ttu-id="52d9c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52d9c-124">Requirement</span></span> | <span data-ttu-id="52d9c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d9c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52d9c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d9c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52d9c-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d9c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="52d9c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d9c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52d9c-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52d9c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="52d9c-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="52d9c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="52d9c-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="52d9c-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="52d9c-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="52d9c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="52d9c-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="52d9c-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="52d9c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="52d9c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52d9c-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52d9c-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="52d9c-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52d9c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d9c-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="52d9c-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





