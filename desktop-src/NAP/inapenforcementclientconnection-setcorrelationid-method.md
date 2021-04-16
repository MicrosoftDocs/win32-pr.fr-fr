---
title: Méthode INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient. h)
description: Définit l’ID utilisé pour corréler les demandes SoH et les réponses SoH.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Méthode SetCorrelationId NAP
- Méthode SetCorrelationId NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508441"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a><span data-ttu-id="20190-106">INapEnforcementClientConnection :: SetCorrelationId, méthode</span><span class="sxs-lookup"><span data-stu-id="20190-106">INapEnforcementClientConnection::SetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="20190-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="20190-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="20190-108">La méthode **INapEnforcementClientConnection :: SetCorrelationId** définit l’ID utilisé pour corréler les demandes SOH et les réponses SOH.</span><span class="sxs-lookup"><span data-stu-id="20190-108">The **INapEnforcementClientConnection::SetCorrelationId** method sets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="20190-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20190-109">Syntax</span></span>


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="20190-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20190-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20190-111">*CorrelationId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="20190-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20190-112">Structure d’ID de [**corrélation**](/windows/win32/api/naptypes/ns-naptypes-correlationid) unique qui identifie un échange SOH spécifique.</span><span class="sxs-lookup"><span data-stu-id="20190-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies a specific SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20190-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20190-113">Return value</span></span>

<span data-ttu-id="20190-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="20190-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="20190-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="20190-115">Return code</span></span>                                                                                     | <span data-ttu-id="20190-116">Description</span><span class="sxs-lookup"><span data-stu-id="20190-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="20190-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20190-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="20190-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="20190-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="20190-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="20190-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="20190-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="20190-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="20190-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="20190-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="20190-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="20190-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20190-123">Notes</span><span class="sxs-lookup"><span data-stu-id="20190-123">Remarks</span></span>

<span data-ttu-id="20190-124">L’ID de corrélation est défini par NapAgent et basé sur l’ID de connexion.</span><span class="sxs-lookup"><span data-stu-id="20190-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="20190-125">Cet ID est utilisé pour corréler les demandes et les réponses, c.-à-d. il décrit de façon unique un échange SoH et contient toujours l’ID du dernier ensemble de déclaration d’intégrité de l’objet de connexion.</span><span class="sxs-lookup"><span data-stu-id="20190-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="20190-126">Lors de la réception d’un SoH-Response, NapAgent vérifie d’abord que les ID correspondent. Si ce n’est pas le cas, une erreur est retournée et l’application doit supprimer le paquet.</span><span class="sxs-lookup"><span data-stu-id="20190-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="20190-127">Pour plus d’informations, consultez [**INapEnforcementClientBinding ::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .</span><span class="sxs-lookup"><span data-stu-id="20190-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="20190-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20190-128">Requirements</span></span>



| <span data-ttu-id="20190-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20190-129">Requirement</span></span> | <span data-ttu-id="20190-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="20190-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20190-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20190-131">Minimum supported client</span></span><br/> | <span data-ttu-id="20190-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20190-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="20190-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20190-133">Minimum supported server</span></span><br/> | <span data-ttu-id="20190-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20190-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="20190-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="20190-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="20190-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="20190-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="20190-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="20190-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20190-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="20190-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="20190-139">DLL</span><span class="sxs-lookup"><span data-stu-id="20190-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20190-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20190-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="20190-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20190-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20190-142">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="20190-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





