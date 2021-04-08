---
title: Méthode INapEnforcementClientConnection GetSoHRequest (NapEnforcementClient. h)
description: Obtient la demande d’intégrité actuelle.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- Méthode GetSoHRequest NAP
- Méthode GetSoHRequest NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941916"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a><span data-ttu-id="bcd77-106">INapEnforcementClientConnection :: GetSoHRequest, méthode</span><span class="sxs-lookup"><span data-stu-id="bcd77-106">INapEnforcementClientConnection::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="bcd77-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bcd77-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bcd77-108">La méthode **INapEnforcementClientConnection :: GetSoHRequest** obtient la requête SOH actuelle.</span><span class="sxs-lookup"><span data-stu-id="bcd77-108">The **INapEnforcementClientConnection::GetSoHRequest** method gets the current SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd77-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcd77-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="bcd77-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcd77-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcd77-111">*sohRequest* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bcd77-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcd77-112">Pointeur vers un pointeur vers une structure [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , qui est un objet blob de données opaque pour l’application.</span><span class="sxs-lookup"><span data-stu-id="bcd77-112">A pointer to a pointer to a [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcd77-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcd77-113">Return value</span></span>

<span data-ttu-id="bcd77-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="bcd77-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bcd77-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bcd77-115">Return code</span></span>                                                                                     | <span data-ttu-id="bcd77-116">Description</span><span class="sxs-lookup"><span data-stu-id="bcd77-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bcd77-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd77-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bcd77-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="bcd77-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bcd77-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd77-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bcd77-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="bcd77-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bcd77-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd77-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bcd77-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bcd77-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bcd77-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bcd77-123">Remarks</span></span>

<span data-ttu-id="bcd77-124">Cette valeur est définie par le NapAgent et interrogée par les enforceurs à envoyer sur le câble.</span><span class="sxs-lookup"><span data-stu-id="bcd77-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="bcd77-125">Un paquet SoH de longueur zéro octet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bcd77-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd77-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcd77-126">Requirements</span></span>



| <span data-ttu-id="bcd77-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcd77-127">Requirement</span></span> | <span data-ttu-id="bcd77-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcd77-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd77-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcd77-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bcd77-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcd77-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bcd77-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcd77-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bcd77-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcd77-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bcd77-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="bcd77-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcd77-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcd77-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bcd77-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="bcd77-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bcd77-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bcd77-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="bcd77-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bcd77-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcd77-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcd77-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bcd77-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcd77-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcd77-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="bcd77-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





