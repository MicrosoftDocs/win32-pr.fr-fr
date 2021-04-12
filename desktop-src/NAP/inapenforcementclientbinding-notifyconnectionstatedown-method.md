---
title: Méthode INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: Est utilisé pour informer le NapAgent qu’une connexion à un client de contrainte s’est déroulée.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Méthode NotifyConnectionStateDown NAP
- Méthode NotifyConnectionStateDown NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode NotifyConnectionStateDown
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519281"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a><span data-ttu-id="f5d6e-106">INapEnforcementClientBinding :: NotifyConnectionStateDown, méthode</span><span class="sxs-lookup"><span data-stu-id="f5d6e-106">INapEnforcementClientBinding::NotifyConnectionStateDown method</span></span>

> [!Note]  
> <span data-ttu-id="f5d6e-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f5d6e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f5d6e-108">La méthode **INapEnforcementClientBinding :: NotifyConnectionStateDown** est utilisée pour informer le NapAgent qu’une connexion à un client de contrainte s’est déroulée.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-108">The **INapEnforcementClientBinding::NotifyConnectionStateDown** method is used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5d6e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5d6e-109">Syntax</span></span>


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a><span data-ttu-id="f5d6e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5d6e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5d6e-111">*downCxn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f5d6e-111">*downCxn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5d6e-112">Pointeur COM vers l’interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la connexion en aval.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the down connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5d6e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5d6e-113">Return value</span></span>

<span data-ttu-id="f5d6e-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f5d6e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f5d6e-115">Return code</span></span>                                                                                             | <span data-ttu-id="f5d6e-116">Description</span><span class="sxs-lookup"><span data-stu-id="f5d6e-116">Description</span></span>                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5d6e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-117"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="f5d6e-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f5d6e-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="f5d6e-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f5d6e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="f5d6e-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f5d6e-123"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-123"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="f5d6e-124">L’application n’a pas été précédemment initialisée.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-124">The enforcer has not been previously initialized.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="f5d6e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="f5d6e-125">Remarks</span></span>

<span data-ttu-id="f5d6e-126">Lorsque l’une des connexions établies par un client de mise en œuvre est arrêtée, le client de contrainte doit supprimer la connexion de sa liste active et informer le NapAgent à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-126">When any of the connections established by an enforcement client go down, the enforcement client should remove the connection from its active list and inform the NapAgent using this method.</span></span> <span data-ttu-id="f5d6e-127">Dès que cet appel est retourné, l’objet de connexion peut être libéré et libéré.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-127">As soon as this call returns, the connection object can be released and freed.</span></span> <span data-ttu-id="f5d6e-128">NapAgent ne contient pas de références à l’objet de connexion.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-128">The NapAgent will not hold references to the connection object.</span></span>

<span data-ttu-id="f5d6e-129">À la suite de cette notification, NapAgent met à jour son état NAP du système en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="f5d6e-129">As a result of this notification, the NapAgent updates its system NAP state as appropriate.</span></span>

<span data-ttu-id="f5d6e-130">Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="f5d6e-130">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5d6e-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5d6e-131">Requirements</span></span>



| <span data-ttu-id="f5d6e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5d6e-132">Requirement</span></span> | <span data-ttu-id="f5d6e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5d6e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d6e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5d6e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f5d6e-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5d6e-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f5d6e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5d6e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f5d6e-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5d6e-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f5d6e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5d6e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5d6e-139"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-139"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5d6e-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="f5d6e-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5d6e-141"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-141"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="f5d6e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f5d6e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5d6e-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="f5d6e-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5d6e-144">See also</span></span>

<dl> <span data-ttu-id="f5d6e-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f5d6e-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f5d6e-146">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="f5d6e-146">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> </dl>

 

 





