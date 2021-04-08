---
title: Méthode INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient. h)
description: Définit la requête SoH.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- Méthode SetSoHRequest NAP
- Méthode SetSoHRequest NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740909"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a><span data-ttu-id="386dd-106">INapEnforcementClientConnection :: SetSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="386dd-106">INapEnforcementClientConnection::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="386dd-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="386dd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="386dd-108">La méthode **INapEnforcementClientConnection :: SetSoHRequest** définit la requête SOH.</span><span class="sxs-lookup"><span data-stu-id="386dd-108">The **INapEnforcementClientConnection::SetSoHRequest** method sets the SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="386dd-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="386dd-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="386dd-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="386dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="386dd-111">*sohRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="386dd-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="386dd-112">Pointeur vers une structure [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) unique, qui est un objet blob de données opaque pour l’application.</span><span class="sxs-lookup"><span data-stu-id="386dd-112">A pointer to a unique [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="386dd-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="386dd-113">Return value</span></span>

<span data-ttu-id="386dd-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="386dd-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="386dd-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="386dd-115">Return code</span></span>                                                                                     | <span data-ttu-id="386dd-116">Description</span><span class="sxs-lookup"><span data-stu-id="386dd-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="386dd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="386dd-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="386dd-118">Le paquet SoH est valide.</span><span class="sxs-lookup"><span data-stu-id="386dd-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="386dd-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="386dd-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="386dd-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="386dd-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="386dd-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="386dd-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="386dd-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="386dd-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="386dd-123">Notes</span><span class="sxs-lookup"><span data-stu-id="386dd-123">Remarks</span></span>

<span data-ttu-id="386dd-124">Cette valeur est définie par le NapAgent et interrogée par les enforceurs à envoyer sur le câble.</span><span class="sxs-lookup"><span data-stu-id="386dd-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="386dd-125">Un paquet SoH de longueur zéro octet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="386dd-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="386dd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="386dd-126">Requirements</span></span>



| <span data-ttu-id="386dd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="386dd-127">Requirement</span></span> | <span data-ttu-id="386dd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="386dd-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="386dd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="386dd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="386dd-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="386dd-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="386dd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="386dd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="386dd-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="386dd-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="386dd-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="386dd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="386dd-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="386dd-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="386dd-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="386dd-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="386dd-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="386dd-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="386dd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="386dd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="386dd-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="386dd-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="386dd-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="386dd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="386dd-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="386dd-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





