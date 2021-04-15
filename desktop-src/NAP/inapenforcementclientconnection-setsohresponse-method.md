---
title: Méthode INapEnforcementClientConnection SetSoHResponse (NapEnforcementClient. h)
description: Définit le SoH-Response et est utilisé par le client de mise en œuvre lors de la réception d’un paquet.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Méthode SetSoHResponse NAP
- Méthode SetSoHResponse NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdc403a1ff68e28f7d262e64ebe558226741b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466186"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a><span data-ttu-id="4a057-106">INapEnforcementClientConnection :: SetSoHResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="4a057-106">INapEnforcementClientConnection::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="4a057-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="4a057-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4a057-108">La méthode **INapEnforcementClientConnection :: SetSoHResponse** définit la SoH-Response et est utilisée par le client de mise en œuvre lors de la réception d’un paquet.</span><span class="sxs-lookup"><span data-stu-id="4a057-108">The **INapEnforcementClientConnection::SetSoHResponse** method sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a057-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a057-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="4a057-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a057-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a057-111">*sohResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a057-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a057-112">Pointeur vers une structure [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) unique, qui est un objet blob de données opaque pour l’application.</span><span class="sxs-lookup"><span data-stu-id="4a057-112">A pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a057-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a057-113">Return value</span></span>

<span data-ttu-id="4a057-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="4a057-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4a057-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4a057-115">Return code</span></span>                                                                                     | <span data-ttu-id="4a057-116">Description</span><span class="sxs-lookup"><span data-stu-id="4a057-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a057-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4a057-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4a057-118">Le paquet SoH est valide.</span><span class="sxs-lookup"><span data-stu-id="4a057-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="4a057-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4a057-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4a057-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="4a057-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4a057-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4a057-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4a057-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="4a057-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4a057-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4a057-123">Remarks</span></span>

<span data-ttu-id="4a057-124">Un paquet de taille zéro est valide.</span><span class="sxs-lookup"><span data-stu-id="4a057-124">A zero-sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a057-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a057-125">Requirements</span></span>



| <span data-ttu-id="4a057-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a057-126">Requirement</span></span> | <span data-ttu-id="4a057-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a057-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a057-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a057-128">Minimum supported client</span></span><br/> | <span data-ttu-id="4a057-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a057-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4a057-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a057-130">Minimum supported server</span></span><br/> | <span data-ttu-id="4a057-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a057-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4a057-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a057-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a057-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a057-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4a057-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="4a057-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4a057-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4a057-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="4a057-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4a057-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a057-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a057-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4a057-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a057-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a057-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="4a057-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





