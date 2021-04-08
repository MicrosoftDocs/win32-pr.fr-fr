---
title: Interface INapEnforcementClientBinding (NapEnforcementClient. h)
description: Les clients de contrainte utilisent pour communiquer avec le NapAgent.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- NAP de l’interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844357"
---
# <a name="inapenforcementclientbinding-interface"></a><span data-ttu-id="53611-105">Interface INapEnforcementClientBinding</span><span class="sxs-lookup"><span data-stu-id="53611-105">INapEnforcementClientBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="53611-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="53611-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="53611-107">**INapEnforcementClientBinding** fournit des méthodes que les clients de mise en œuvre utilisent pour communiquer avec NapAgent.</span><span class="sxs-lookup"><span data-stu-id="53611-107">The **INapEnforcementClientBinding** provides methods that enforcement clients use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="53611-108">Membres</span><span class="sxs-lookup"><span data-stu-id="53611-108">Members</span></span>

<span data-ttu-id="53611-109">L’interface **INapEnforcementClientBinding** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="53611-109">The **INapEnforcementClientBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="53611-110">**INapEnforcementClientBinding** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="53611-110">**INapEnforcementClientBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="53611-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53611-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="53611-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="53611-112">Methods</span></span>

<span data-ttu-id="53611-113">L’interface **INapEnforcementClientBinding** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="53611-113">The **INapEnforcementClientBinding** interface has these methods.</span></span>



| <span data-ttu-id="53611-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="53611-114">Method</span></span>                                                                                                                           | <span data-ttu-id="53611-115">Description</span><span class="sxs-lookup"><span data-stu-id="53611-115">Description</span></span>                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53611-116">**INapEnforcementClientBinding :: CreateConnection**</span><span class="sxs-lookup"><span data-stu-id="53611-116">**INapEnforcementClientBinding::CreateConnection**</span></span>](inapenforcementclientbinding-createconnection-method.md)                   | <span data-ttu-id="53611-117">Utilisé par les enforceurs pour créer des objets de connexion.</span><span class="sxs-lookup"><span data-stu-id="53611-117">Used by enforcers to create connection objects.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="53611-118">**INapEnforcementClientBinding::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="53611-118">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)                         | <span data-ttu-id="53611-119">Utilisé par le client de mise en œuvre lorsqu’il a besoin d’une requête SoH pour une connexion particulière.</span><span class="sxs-lookup"><span data-stu-id="53611-119">Used by the enforcement client when it needs an SoH-request for a particular connection.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="53611-120">**INapEnforcementClientBinding :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="53611-120">**INapEnforcementClientBinding::Initialize**</span></span>](inapenforcementclientbinding-initialize-method.md)                               | <span data-ttu-id="53611-121">Démarre le service NapAgent.</span><span class="sxs-lookup"><span data-stu-id="53611-121">Starts up the NapAgent service.</span></span> <span data-ttu-id="53611-122">Le client de contrainte doit appeler cette méthode avant d’appeler toute autre méthode de cette interface.</span><span class="sxs-lookup"><span data-stu-id="53611-122">The enforcement client must call this method before calling any other method of this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="53611-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="53611-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | <span data-ttu-id="53611-124">Utilisé pour informer le NapAgent qu’une connexion à un client de contrainte s’est déroulée.</span><span class="sxs-lookup"><span data-stu-id="53611-124">Used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="53611-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span><span class="sxs-lookup"><span data-stu-id="53611-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span></span>](inapenforcementclientbinding-notifysohchangefailure-method.md)       | <span data-ttu-id="53611-126">Utilisé par le client de mise en œuvre pour informer NapAgent qu’il n’a pas pu traiter un précédent [**INapEnforcementClientCallback :: NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="53611-126">Used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span><br/> |
| [<span data-ttu-id="53611-127">**INapEnforcementClientBinding ::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="53611-127">**INapEnforcementClientBinding::ProcessSoHResponse**</span></span>](inapenforcementclientbinding-processsohresponse-method.md)               | <span data-ttu-id="53611-128">Utilisé par les clients de mise en œuvre chaque fois qu’ils obtiennent une SoH-Response objet blob de données à partir du serveur de mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="53611-128">Used by enforcement clients whenever they get an SoH-Response data blob from the enforcement server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="53611-129">**INapEnforcementClientBinding :: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="53611-129">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)                           | <span data-ttu-id="53611-130">Conclut le service NapAgent pour cette connexion client.</span><span class="sxs-lookup"><span data-stu-id="53611-130">Concludes the NapAgent service for this client connection.</span></span><br/>                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="53611-131">Notes</span><span class="sxs-lookup"><span data-stu-id="53611-131">Remarks</span></span>

<span data-ttu-id="53611-132">Toutes les API de cette interface renverront RPC \_ E \_ Disconnected si le NapAgent est arrêté.</span><span class="sxs-lookup"><span data-stu-id="53611-132">All the APIs in this interface will return RPC\_E\_DISCONNECTED if the NapAgent is stopped.</span></span> <span data-ttu-id="53611-133">Cet objet est automatiquement récupéré et est de nouveau lié au NapAgent, une fois qu’il a redémarré.</span><span class="sxs-lookup"><span data-stu-id="53611-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="53611-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53611-134">Requirements</span></span>



| <span data-ttu-id="53611-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53611-135">Requirement</span></span> | <span data-ttu-id="53611-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="53611-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53611-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53611-137">Minimum supported client</span></span><br/> | <span data-ttu-id="53611-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53611-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53611-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53611-139">Minimum supported server</span></span><br/> | <span data-ttu-id="53611-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53611-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53611-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="53611-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="53611-142"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="53611-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="53611-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="53611-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="53611-144"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="53611-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="53611-145">DLL</span><span class="sxs-lookup"><span data-stu-id="53611-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53611-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53611-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="53611-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53611-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53611-148">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="53611-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="53611-149">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="53611-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

