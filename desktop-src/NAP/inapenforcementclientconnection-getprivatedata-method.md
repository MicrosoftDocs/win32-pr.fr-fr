---
title: Méthode INapEnforcementClientConnection GetPrivateData (NapEnforcementClient. h)
description: Est utilisé par le NapAgent pour recevoir des données privées.
ms.assetid: d38ef523-b645-401f-b3a9-1315ef39931a
keywords:
- Méthode GetPrivateData NAP
- Méthode GetPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6618ff7b25ad57cbb943107e80f299d9b6a68bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843330"
---
# <a name="inapenforcementclientconnectiongetprivatedata-method"></a><span data-ttu-id="bff7a-106">INapEnforcementClientConnection :: GetPrivateData, méthode</span><span class="sxs-lookup"><span data-stu-id="bff7a-106">INapEnforcementClientConnection::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="bff7a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bff7a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bff7a-108">La méthode **INapEnforcementClientConnection :: GetPrivateData** est utilisée par NapAgent pour recevoir des données privées.</span><span class="sxs-lookup"><span data-stu-id="bff7a-108">The **INapEnforcementClientConnection::GetPrivateData** method is used by the NapAgent to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff7a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bff7a-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="bff7a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bff7a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff7a-111">*privateData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bff7a-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bff7a-112">Pointeur vers un pointeur vers un objet blob de données opaques [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que seul le NapAgent peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="bff7a-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff7a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bff7a-113">Return value</span></span>

<span data-ttu-id="bff7a-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="bff7a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bff7a-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bff7a-115">Return code</span></span>                                                                                     | <span data-ttu-id="bff7a-116">Description</span><span class="sxs-lookup"><span data-stu-id="bff7a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bff7a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bff7a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bff7a-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="bff7a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bff7a-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bff7a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bff7a-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="bff7a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bff7a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bff7a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bff7a-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bff7a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bff7a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bff7a-123">Requirements</span></span>



| <span data-ttu-id="bff7a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bff7a-124">Requirement</span></span> | <span data-ttu-id="bff7a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="bff7a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff7a-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bff7a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bff7a-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bff7a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bff7a-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bff7a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bff7a-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bff7a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bff7a-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="bff7a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bff7a-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff7a-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bff7a-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="bff7a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bff7a-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bff7a-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="bff7a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bff7a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bff7a-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bff7a-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bff7a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bff7a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff7a-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="bff7a-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





