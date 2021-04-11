---
title: Méthode INapEnforcementClientConnection SetPrivateData (NapEnforcementClient. h)
description: Est utilisé par NapAgent pour définir des données privées.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- Méthode SetPrivateData NAP
- Méthode SetPrivateData NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032652"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a><span data-ttu-id="be034-106">INapEnforcementClientConnection :: SetPrivateData, méthode</span><span class="sxs-lookup"><span data-stu-id="be034-106">INapEnforcementClientConnection::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="be034-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="be034-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="be034-108">La méthode **INapEnforcementClientConnection :: SetPrivateData** est utilisée par le NapAgent pour définir des données privées.</span><span class="sxs-lookup"><span data-stu-id="be034-108">The **INapEnforcementClientConnection::SetPrivateData** method is used by the NapAgent to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="be034-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be034-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="be034-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be034-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be034-111">*privateData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be034-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be034-112">Pointeur vers un objet blob de données [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) que seul le NapAgent peut interpréter.</span><span class="sxs-lookup"><span data-stu-id="be034-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be034-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="be034-113">Return value</span></span>

<span data-ttu-id="be034-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="be034-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="be034-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="be034-115">Return code</span></span>                                                                                     | <span data-ttu-id="be034-116">Description</span><span class="sxs-lookup"><span data-stu-id="be034-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="be034-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="be034-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="be034-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="be034-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="be034-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="be034-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="be034-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="be034-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="be034-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="be034-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="be034-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="be034-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be034-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be034-123">Requirements</span></span>



| <span data-ttu-id="be034-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be034-124">Requirement</span></span> | <span data-ttu-id="be034-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="be034-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be034-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be034-126">Minimum supported client</span></span><br/> | <span data-ttu-id="be034-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be034-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="be034-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be034-128">Minimum supported server</span></span><br/> | <span data-ttu-id="be034-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be034-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="be034-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="be034-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="be034-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="be034-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="be034-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="be034-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be034-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be034-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="be034-134">DLL</span><span class="sxs-lookup"><span data-stu-id="be034-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be034-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be034-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="be034-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be034-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be034-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="be034-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





