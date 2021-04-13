---
title: Méthode INapEnforcementClientBinding ProcessSoHResponse (NapEnforcementClient. h)
description: Est utilisé par les clients de mise en œuvre pour traiter un SoHResponse chaque fois qu’ils reçoivent un objet blob de données SoHResponse à partir du serveur de mise en œuvre.
ms.assetid: 6ff6d2c5-9ebe-4d8c-aa27-03147e2e1122
keywords:
- Méthode ProcessSoHResponse NAP
- Méthode ProcessSoHResponse NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, méthode ProcessSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.ProcessSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac8c87314ca1e28163428bf53e4a1fc6e31106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519177"
---
# <a name="inapenforcementclientbindingprocesssohresponse-method"></a><span data-ttu-id="e46f3-106">INapEnforcementClientBinding ::P méthode rocessSoHResponse</span><span class="sxs-lookup"><span data-stu-id="e46f3-106">INapEnforcementClientBinding::ProcessSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="e46f3-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e46f3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e46f3-108">La méthode **INapEnforcementClientBinding ::P rocesssohresponse** est utilisée par les clients de mise en œuvre pour traiter un SoHResponse chaque fois qu’ils reçoivent un objet blob de données SoHResponse du serveur d’application.</span><span class="sxs-lookup"><span data-stu-id="e46f3-108">The **INapEnforcementClientBinding::ProcessSoHResponse** method is used by enforcement clients to process an SoHResponse whenever they receive an SoHResponse data blob from the enforcement server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e46f3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e46f3-109">Syntax</span></span>


```C++
HRESULT ProcessSoHResponse(
  [in] INapEnforcementClientConnection *connection
);
```



## <a name="parameters"></a><span data-ttu-id="e46f3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e46f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e46f3-111">*connexion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e46f3-111">*connection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e46f3-112">Pointeur COM vers l’interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) de la connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="e46f3-112">A COM pointer to the [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface of the client connection.</span></span> <span data-ttu-id="e46f3-113">NapAgent ne contient pas de références à l’objet associé à cette interface après la fin de l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="e46f3-113">The NapAgent does not hold references to the object associated with this interface after this method call completes.</span></span>

<span data-ttu-id="e46f3-114">Vous devez utiliser une connexion précédemment établie pour le traitement des objets BLOB de données SOHResponse.</span><span class="sxs-lookup"><span data-stu-id="e46f3-114">You must use a previously established connection for processing SOHResponse data blobs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e46f3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e46f3-115">Return value</span></span>

<span data-ttu-id="e46f3-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="e46f3-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e46f3-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e46f3-117">Return code</span></span>                                                                                             | <span data-ttu-id="e46f3-118">Description</span><span class="sxs-lookup"><span data-stu-id="e46f3-118">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e46f3-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-119"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="e46f3-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e46f3-120">The operation is successful.</span></span><br/>                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="e46f3-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="e46f3-122">Aucune connexion n’a été créée précédemment sur le client de contrainte.</span><span class="sxs-lookup"><span data-stu-id="e46f3-122">No connections have previously been created on the enforcement client.</span></span> <br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="e46f3-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="e46f3-124">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e46f3-124">Permissions error, access denied.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="e46f3-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="e46f3-126">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e46f3-126">System resource limit, could not perform the operation.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="e46f3-127"><dt>**\_paquet NAP E \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-127"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl>  | <span data-ttu-id="e46f3-128">Si cette valeur est renvoyée, le client de contrainte doit supprimer le paquet si le NapAgent retourne le \_ paquet NAP E \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="e46f3-128">If this value is returned the enforcement client must drop the packet if the NapAgent returns NAP\_E\_INVALID\_PACKET.</span></span> <span data-ttu-id="e46f3-129">Dans ce cas, l’application doit supposer que le serveur auquel elle est confrontée n’est pas compatible avec la protection d’accès réseau (NAP) et supprime la connexion de la liste active (par exemple, notifier le NapAgent d’un état de connexion).</span><span class="sxs-lookup"><span data-stu-id="e46f3-129">In this case, the enforcer must assume that the server it is talking to is not NAP-enabled and remove the connection from the active list (i.e. notify the NapAgent of a connection state down).</span></span><br/> |
| <dl> <span data-ttu-id="e46f3-130"><dt>**\_ID non \_ compatible NAP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-130"><dt>**NAP\_E\_MISMATCHED\_ID**</dt></span></span> </dl>   | <span data-ttu-id="e46f3-131">Si cette valeur est retournée, elle indique que l’ID de corrélation dans le paquet SoH-Response ne correspond pas à la réponse SoH en suspens.</span><span class="sxs-lookup"><span data-stu-id="e46f3-131">If this value is returned it indicates that the correlation id in the SoH-Response packet did not match the outstanding SoH-Response.</span></span> <span data-ttu-id="e46f3-132">Dans ce cas, l’application doit supprimer le paquet et attendre un autre paquet plus récent SoH-Response.</span><span class="sxs-lookup"><span data-stu-id="e46f3-132">In this case, the enforcer should drop the packet and wait for another newer SoH-Response packet.</span></span><br/> <span data-ttu-id="e46f3-133">Cela peut être dû à une réponse à un message de demande plus ancien.</span><span class="sxs-lookup"><span data-stu-id="e46f3-133">This may be caused by a response to an older request message.</span></span><br/>        |
| <dl> <span data-ttu-id="e46f3-134"><dt>**NAP \_ E \_ non \_ initialisé**</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-134"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="e46f3-135">L’application n’a pas été précédemment initialisée.</span><span class="sxs-lookup"><span data-stu-id="e46f3-135">The enforcer has not been previously initialized.</span></span><br/>                                                                                                                                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="e46f3-136">Notes</span><span class="sxs-lookup"><span data-stu-id="e46f3-136">Remarks</span></span>

<span data-ttu-id="e46f3-137">Le NapAgent interroge l’objet blob de données SoH-Response à partir de l’objet de connexion, le traite et définit la décision résultante (par exemple,</span><span class="sxs-lookup"><span data-stu-id="e46f3-137">The NapAgent queries the SoH-Response data blob from the connection object, processes it, and sets the resulting decision (eg.</span></span> <span data-ttu-id="e46f3-138">accès complet/restreint, etc.) sur l’objet de connexion.</span><span class="sxs-lookup"><span data-stu-id="e46f3-138">full/restricted access/etc) on the connection object.</span></span>

<span data-ttu-id="e46f3-139">Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="e46f3-139">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e46f3-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e46f3-140">Requirements</span></span>



| <span data-ttu-id="e46f3-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e46f3-141">Requirement</span></span> | <span data-ttu-id="e46f3-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="e46f3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e46f3-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e46f3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e46f3-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e46f3-144">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e46f3-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e46f3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e46f3-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e46f3-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e46f3-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="e46f3-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e46f3-148"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-148"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="e46f3-149">MIDL</span><span class="sxs-lookup"><span data-stu-id="e46f3-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e46f3-150"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-150"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="e46f3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e46f3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e46f3-152"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-152"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e46f3-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e46f3-153">See also</span></span>

<dl> <span data-ttu-id="e46f3-154"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="e46f3-154"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="e46f3-155">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="e46f3-155">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="e46f3-156">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e46f3-156">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





