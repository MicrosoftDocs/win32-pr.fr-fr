---
title: Méthode IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Demande des informations sur l’ordinateur cible sur lequel la connexion doit être redirigée.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetTargetInfo
- Méthode GetTargetInfo Services Bureau à distance, interface IConnectionBrokerClient
- Services Bureau à distance de l’interface IConnectionBrokerClient, méthode GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508302"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a><span data-ttu-id="fba20-106">IConnectionBrokerClient :: GetTargetInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="fba20-106">IConnectionBrokerClient::GetTargetInfo method</span></span>

<span data-ttu-id="fba20-107">Demande des informations sur l’ordinateur cible sur lequel la connexion doit être redirigée.</span><span class="sxs-lookup"><span data-stu-id="fba20-107">Requests information about the target computer where the connection should be redirected.</span></span> <span data-ttu-id="fba20-108">Cette méthode est utilisée par le redirecteur pour obtenir des informations de redirection pour la demande de connexion entrante.</span><span class="sxs-lookup"><span data-stu-id="fba20-108">This method is used by the redirector to get redirection information for the incoming connection request.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba20-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fba20-109">Syntax</span></span>


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a><span data-ttu-id="fba20-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fba20-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba20-111">*pConnectionInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fba20-111">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba20-112">Adresse d’une structure [**d' \_ \_ informations de connexion CB**](cb-connection-info.md) qui contient des informations sur la demande de connexion entrante.</span><span class="sxs-lookup"><span data-stu-id="fba20-112">The address of a [**CB\_CONNECTION\_INFO**](cb-connection-info.md) structure that contains information about the incoming connection request.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-113">*Réservé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fba20-113">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba20-114">Ce paramètre est réservé pour une utilisation ultérieure et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="fba20-114">This parameter is reserved for future use and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-115">*hStatusEvent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fba20-115">*hStatusEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fba20-116">Handle d’un événement qui est défini à chaque mise à jour de la progression de la requête.</span><span class="sxs-lookup"><span data-stu-id="fba20-116">The handle of an event that will get set whenever there is an update to the progress of the request.</span></span> <span data-ttu-id="fba20-117">Vous êtes responsable de la création et de la fermeture de cet événement.</span><span class="sxs-lookup"><span data-stu-id="fba20-117">You are responsible for creating and closing this event.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-118">*pTargetInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fba20-118">*pTargetInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba20-119">Adresse d’une structure [**d' \_ \_ informations de la cible CB**](cb-target-info.md) qui reçoit des informations sur l’ordinateur cible sur lequel la connexion entrante doit être redirigée.</span><span class="sxs-lookup"><span data-stu-id="fba20-119">The address of a [**CB\_TARGET\_INFO**](cb-target-info.md) structure that receives information about the target computer where the incoming connection should be redirected.</span></span> <span data-ttu-id="fba20-120">Étant donné qu’il s’agit d’une méthode asynchrone, cette mémoire doit rester disponible jusqu’à ce que la demande soit terminée.</span><span class="sxs-lookup"><span data-stu-id="fba20-120">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="fba20-121">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fba20-121">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-122">*pResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fba20-122">*pResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba20-123">Adresse d’une variable **DWORD** qui reçoit un code de résultat.</span><span class="sxs-lookup"><span data-stu-id="fba20-123">The address of a **DWORD** variable that receives a result code.</span></span> <span data-ttu-id="fba20-124">Étant donné qu’il s’agit d’une méthode asynchrone, cette mémoire doit rester disponible jusqu’à ce que la demande soit terminée.</span><span class="sxs-lookup"><span data-stu-id="fba20-124">Because this is an asynchronous method, this memory must remain available until the request is complete.</span></span> <span data-ttu-id="fba20-125">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fba20-125">For more information, see Remarks.</span></span>

<span data-ttu-id="fba20-126">Ce code de résultat sera l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="fba20-126">This result code will be one of the following values.</span></span>

<dt>

<span data-ttu-id="fba20-127">0</span><span class="sxs-lookup"><span data-stu-id="fba20-127">0</span></span>
</dt> <dd>

<span data-ttu-id="fba20-128">Réussite.</span><span class="sxs-lookup"><span data-stu-id="fba20-128">Success.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-129">0x0000400</span><span class="sxs-lookup"><span data-stu-id="fba20-129">0x0000400</span></span>
</dt> <dd>

<span data-ttu-id="fba20-130">L’ordinateur de destination est introuvable.</span><span class="sxs-lookup"><span data-stu-id="fba20-130">The destination computer could not be found.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-131">0x0000401</span><span class="sxs-lookup"><span data-stu-id="fba20-131">0x0000401</span></span>
</dt> <dd>

<span data-ttu-id="fba20-132">L’ordinateur de destination n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="fba20-132">The destination computer is not available.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-133">0x0000402</span><span class="sxs-lookup"><span data-stu-id="fba20-133">0x0000402</span></span>
</dt> <dd>

<span data-ttu-id="fba20-134">Erreur lors du chargement de l’ordinateur de destination.</span><span class="sxs-lookup"><span data-stu-id="fba20-134">Error loading destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-135">0x0000403</span><span class="sxs-lookup"><span data-stu-id="fba20-135">0x0000403</span></span>
</dt> <dd>

<span data-ttu-id="fba20-136">Erreur lors de l’importation de l’ordinateur de destination en ligne.</span><span class="sxs-lookup"><span data-stu-id="fba20-136">Error bringing destination computer online.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-137">0x0000404</span><span class="sxs-lookup"><span data-stu-id="fba20-137">0x0000404</span></span>
</dt> <dd>

<span data-ttu-id="fba20-138">Erreur lors de la redirection vers l’ordinateur de destination.</span><span class="sxs-lookup"><span data-stu-id="fba20-138">Error redirecting to destination computer.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-139">0x0000405</span><span class="sxs-lookup"><span data-stu-id="fba20-139">0x0000405</span></span>
</dt> <dd>

<span data-ttu-id="fba20-140">Erreur lors de la réactivation de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fba20-140">Error waking virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-141">0x0000406</span><span class="sxs-lookup"><span data-stu-id="fba20-141">0x0000406</span></span>
</dt> <dd>

<span data-ttu-id="fba20-142">Erreur lors du démarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fba20-142">Error booting virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-143">0x0000407</span><span class="sxs-lookup"><span data-stu-id="fba20-143">0x0000407</span></span>
</dt> <dd>

<span data-ttu-id="fba20-144">Erreur lors de la recherche de l’adresse IP de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="fba20-144">Error finding the IP address of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-145">0x0000408</span><span class="sxs-lookup"><span data-stu-id="fba20-145">0x0000408</span></span>
</dt> <dd>

<span data-ttu-id="fba20-146">Le service session Broker n’a trouvé aucun ordinateur disponible dans le pool.</span><span class="sxs-lookup"><span data-stu-id="fba20-146">The session broker could not find any available computers in the pool.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-147">0x0000409</span><span class="sxs-lookup"><span data-stu-id="fba20-147">0x0000409</span></span>
</dt> <dd>

<span data-ttu-id="fba20-148">Le courtier de session a annulé la connexion.</span><span class="sxs-lookup"><span data-stu-id="fba20-148">The session broker canceled the connection.</span></span>

</dd> <dt>

<span data-ttu-id="fba20-149">0x0000410</span><span class="sxs-lookup"><span data-stu-id="fba20-149">0x0000410</span></span>
</dt> <dd>

<span data-ttu-id="fba20-150">Le service session Broker n’a pas pu valider les paramètres de connexion.</span><span class="sxs-lookup"><span data-stu-id="fba20-150">The session broker could not validate the connection settings.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="fba20-151">*ppCbReq* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fba20-151">*ppCbReq* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fba20-152">Adresse d’un pointeur d’interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) que vous utilisez pour obtenir des mises à jour d’État pour une opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="fba20-152">The address of an [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) interface pointer that you use to obtain status updates for an asynchronous operation.</span></span> <span data-ttu-id="fba20-153">Cette interface est utilisée conjointement avec le paramètre *hStatusEvent* pour attendre et obtenir les résultats de cette opération asynchrone.</span><span class="sxs-lookup"><span data-stu-id="fba20-153">This interface is used in conjunction with the *hStatusEvent* parameter to wait for and get the results of this asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fba20-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fba20-154">Return value</span></span>

<span data-ttu-id="fba20-155">Retourne **E \_ en attente** si la requête asynchrone est créée.</span><span class="sxs-lookup"><span data-stu-id="fba20-155">Returns **E\_PENDING** if the asynchronous request is created.</span></span> <span data-ttu-id="fba20-156">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fba20-156">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fba20-157">Notes</span><span class="sxs-lookup"><span data-stu-id="fba20-157">Remarks</span></span>

<span data-ttu-id="fba20-158">Cette méthode est asynchrone.</span><span class="sxs-lookup"><span data-stu-id="fba20-158">This method is asynchronous.</span></span> <span data-ttu-id="fba20-159">Les paramètres *pTargetInfo* et *pResult* doivent rester valides jusqu’à ce que la méthode [**IConnectionBrokerRequest :: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) obtienne la **demande d’État CB \_ \_ \_ terminée**.</span><span class="sxs-lookup"><span data-stu-id="fba20-159">The *pTargetInfo* and *pResult* parameters must remain valid until the [**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md) method obtains **CB\_STATUS\_REQUEST\_COMPLETED**.</span></span>

<span data-ttu-id="fba20-160">Pour plus d’informations sur l’utilisation de cette méthode, voir [How to use the connexion Bureau à distance Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span><span class="sxs-lookup"><span data-stu-id="fba20-160">For more information about how to use this method, see [How to use the Remote Desktop Connection Broker client API](use-the-remote-desktop-connection-broker-client-api.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fba20-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fba20-161">Requirements</span></span>



| <span data-ttu-id="fba20-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fba20-162">Requirement</span></span> | <span data-ttu-id="fba20-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="fba20-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fba20-164">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba20-164">Minimum supported client</span></span><br/> | <span data-ttu-id="fba20-165">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fba20-165">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="fba20-166">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fba20-166">Minimum supported server</span></span><br/> | <span data-ttu-id="fba20-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fba20-167">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="fba20-168">En-tête</span><span class="sxs-lookup"><span data-stu-id="fba20-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="fba20-169"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fba20-169"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fba20-170">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fba20-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="fba20-171"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fba20-171"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="fba20-172">DLL</span><span class="sxs-lookup"><span data-stu-id="fba20-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba20-173"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba20-173"><dt>Cbclient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba20-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fba20-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba20-175">**IConnectionBrokerClient**</span><span class="sxs-lookup"><span data-stu-id="fba20-175">**IConnectionBrokerClient**</span></span>](iconnectionbrokerclient.md)
</dt> </dl>

 

 





