---
title: PxeProviderRecvRequest fonction de rappel
description: Appelée lorsqu’une demande est reçue d’un client.
ms.assetid: 704972d5-177a-490e-881f-d2b3025babda
keywords:
- Fonction de rappel PxeProviderRecvRequest des services de déploiement Windows
topic_type:
- apiref
api_name:
- PxeProviderRecvRequest
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a173c6ba356d98dfd44beb64033f491b9c200d58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384664"
---
# <a name="pxeproviderrecvrequest-callback-function"></a><span data-ttu-id="aea2c-104">PxeProviderRecvRequest fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="aea2c-104">PxeProviderRecvRequest callback function</span></span>

<span data-ttu-id="aea2c-105">Appelée lorsqu’une demande est reçue d’un client.</span><span class="sxs-lookup"><span data-stu-id="aea2c-105">Called when a request is received from a client.</span></span> <span data-ttu-id="aea2c-106">Cette fonction est inscrite en appelant la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) avec le paramètre *CallbackType* défini sur la **\_ \_ \_ demande de rappel PXE**.</span><span class="sxs-lookup"><span data-stu-id="aea2c-106">This function is registered by calling the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function with the *CallbackType* parameter set to **PXE\_CALLBACK\_RECV\_REQUEST**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aea2c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aea2c-107">Syntax</span></span>


```C++
DWORD PXEAPI PxeProviderRecvRequest(
  _In_  HANDLE          hClientRequest,
  _In_  PVOID           pPacket,
  _In_  ULONG           uPacketLen,
  _In_  PXE_ADDRESS     *pLocalAddress,
  _In_  PXE_ADDRESS     *pRemoteAddress,
  _Out_ PXE_BOOT_ACTION pAction,
  _In_  PVOID           pContext
);
```



## <a name="parameters"></a><span data-ttu-id="aea2c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aea2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aea2c-109">*hClientRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-109">*hClientRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aea2c-110">Handle d’une demande reçue d’un client.</span><span class="sxs-lookup"><span data-stu-id="aea2c-110">Handle to a request received from a client.</span></span>

</dd> <dt>

<span data-ttu-id="aea2c-111">*pPacket* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-111">*pPacket* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aea2c-112">Pointeur vers la mémoire tampon qui contient le paquet reçu.</span><span class="sxs-lookup"><span data-stu-id="aea2c-112">Pointer to the memory buffer that contains the received packet.</span></span>

</dd> <dt>

<span data-ttu-id="aea2c-113">*uPacketLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-113">*uPacketLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aea2c-114">Longueur, en octets, de la mémoire tampon vers laquelle pointe le paramètre *pPacket* .</span><span class="sxs-lookup"><span data-stu-id="aea2c-114">Length, in bytes, of the buffer pointed to by the *pPacket* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="aea2c-115">*pLocalAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-115">*pLocalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aea2c-116">Pointeur vers une structure d' [**\_ adresse PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) qui contient l’adresse locale sur laquelle le paquet a été reçu.</span><span class="sxs-lookup"><span data-stu-id="aea2c-116">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the local address on which the packet was received.</span></span>

</dd> <dt>

<span data-ttu-id="aea2c-117">*pRemoteAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-117">*pRemoteAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aea2c-118">Pointeur vers une structure d' [**\_ adresse PXE**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) qui contient l’adresse source du paquet.</span><span class="sxs-lookup"><span data-stu-id="aea2c-118">Pointer to a [**PXE\_ADDRESS**](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address) structure that contains the source address of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="aea2c-119">*Pacte* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-119">*pAction* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aea2c-120">Spécifie l’action que le système doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="aea2c-120">Specifies the action that the system should take.</span></span>



| <span data-ttu-id="aea2c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="aea2c-121">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="aea2c-122">Signification</span><span class="sxs-lookup"><span data-stu-id="aea2c-122">Meaning</span></span>                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PXE_BA_NBP"></span><span id="pxe_ba_nbp"></span><dl> <span data-ttu-id="aea2c-123">Environnement <dt>**PXE \_ E \_ NBP**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="aea2c-123"><dt>**PXE\_BA\_NBP**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="aea2c-124">Le fournisseur a répondu à un client avec un paquet de réponse DHCP standard qui contient un chemin d’accès au programme de démarrage réseau.</span><span class="sxs-lookup"><span data-stu-id="aea2c-124">The provider replied to a client with a standard DHCP response packet that contains a path to the Network Boot Program.</span></span> <span data-ttu-id="aea2c-125">Le retour de cette action signifie que le fournisseur a terminé la demande du client en appelant la fonction [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="aea2c-125">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                        |
| <span id="PXE_BA_CUSTOM"></span><span id="pxe_ba_custom"></span><dl> <span data-ttu-id="aea2c-126">Environnement <dt>**PXE \_ BA \_ personnalisé**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="aea2c-126"><dt>**PXE\_BA\_CUSTOM**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="aea2c-127">Le fournisseur a répondu à un client à l’aide d’une réponse personnalisée qui n’est pas conforme aux spécifications DHCP.</span><span class="sxs-lookup"><span data-stu-id="aea2c-127">The provider replied to a client by using a custom response that does not conform to DHCP specifications.</span></span> <span data-ttu-id="aea2c-128">Le retour de cette action signifie que le fournisseur a terminé la demande du client en appelant la fonction [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="aea2c-128">Returning this action means that the provider successfully completed the client request by calling the [**PxeSendReply**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply) function at least once.</span></span><br/>                                      |
| <span id="PXE_BA_IGNORE"></span><span id="pxe_ba_ignore"></span><dl> <span data-ttu-id="aea2c-129">Environnement <dt>**PXE \_ BA \_ Ignorer**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="aea2c-129"><dt>**PXE\_BA\_IGNORE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="aea2c-130">Le fournisseur ne souhaite pas traiter la demande du client et la demande ne doit pas être transmise au fournisseur suivant.</span><span class="sxs-lookup"><span data-stu-id="aea2c-130">The provider does not want to service the client request and the request should not be passed to the next provider.</span></span> <span data-ttu-id="aea2c-131">Toutes les ressources associées à la demande du client sont libérées et la demande du client est ignorée.</span><span class="sxs-lookup"><span data-stu-id="aea2c-131">All resources associated with the client request are released and the client request is ignored.</span></span> <span data-ttu-id="aea2c-132">Les fournisseurs peuvent également utiliser cette valeur s’ils reconnaissent le client mais que la demande est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="aea2c-132">Providers can also use this value if they recognize the client but the request was malformed.</span></span><br/> |
| <span id="PXE_BA_REJECTED"></span><span id="pxe_ba_rejected"></span><dl> <span data-ttu-id="aea2c-133">Environnement <dt>**PXE \_ BA a \_ rejeté**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="aea2c-133"><dt>**PXE\_BA\_REJECTED**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="aea2c-134">Le fournisseur ne souhaite pas traiter la demande du client.</span><span class="sxs-lookup"><span data-stu-id="aea2c-134">The provider does not want to service the client request.</span></span> <span data-ttu-id="aea2c-135">Le système transmet la demande au fournisseur suivant dans la liste des fournisseurs inscrits.</span><span class="sxs-lookup"><span data-stu-id="aea2c-135">The system passes the request to the next provider in the list of registered providers.</span></span> <span data-ttu-id="aea2c-136">S’il s’agit du dernier fournisseur de la liste, toutes les ressources associées à la demande du client sont libérées et la demande du client est ignorée.</span><span class="sxs-lookup"><span data-stu-id="aea2c-136">If this was the last provider in the list, then all resources associated with the client request are released and client request is ignored.</span></span><br/>                     |



 

</dd> <dt>

<span data-ttu-id="aea2c-137">*pContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-137">*pContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aea2c-138">Valeur de contexte passée à la fonction [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="aea2c-138">Context value passed to the [**PxeRegisterCallback**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aea2c-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aea2c-139">Return value</span></span>

<span data-ttu-id="aea2c-140">Si le fournisseur a correctement traité la demande du client, le rappel doit retourner la **\_ réussite** de l’erreur et l' **\_ \_ action de démarrage PXE** vers laquelle pointe le paramètre de *Pacte* contient l’action de démarrage appropriée pour cette demande.</span><span class="sxs-lookup"><span data-stu-id="aea2c-140">If the provider successfully processed the client request, the callback should return **ERROR\_SUCCESS** and the **PXE\_BOOT\_ACTION** pointed to by the *pAction* parameter contains the appropriate boot action for this request.</span></span> <span data-ttu-id="aea2c-141">Si le fournisseur traitera la demande du client de manière asynchrone, le rappel doit retourner des **\_ e/s d’erreur \_ en attente** et appeler la fonction [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) lorsque la demande du client a été traitée.</span><span class="sxs-lookup"><span data-stu-id="aea2c-141">If the provider will process the client request asynchronously, the callback should return **ERROR\_IO\_PENDING** and call the [**PxeAsyncRecvDone**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeasyncrecvdone) function when the client request has been processed.</span></span> <span data-ttu-id="aea2c-142">En cas d’échec, un code d’erreur approprié doit être retourné et le système se poursuivra comme si l’action de démarrage **\_ \_ rejetée par PXE BA** avait été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="aea2c-142">In case of failure, an appropriate error code should be returned and the system will proceed as if the **PXE\_BA\_REJECTED** boot action was specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="aea2c-143">Notes</span><span class="sxs-lookup"><span data-stu-id="aea2c-143">Remarks</span></span>

<span data-ttu-id="aea2c-144">Le type de paquets détectés par un fournisseur peut être modifié à l’aide de la fonction [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) .</span><span class="sxs-lookup"><span data-stu-id="aea2c-144">The type of packets seen by a provider can be changed with the [**PxeProviderSetAttribute**](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="aea2c-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aea2c-145">Requirements</span></span>



| <span data-ttu-id="aea2c-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aea2c-146">Requirement</span></span> | <span data-ttu-id="aea2c-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="aea2c-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aea2c-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aea2c-148">Minimum supported client</span></span><br/> | <span data-ttu-id="aea2c-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="aea2c-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="aea2c-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aea2c-150">Minimum supported server</span></span><br/> | <span data-ttu-id="aea2c-151">Windows Server 2008, Windows Server 2003 avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aea2c-151">Windows Server 2008, Windows Server 2003 with SP2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aea2c-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aea2c-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aea2c-153">Fonctions du serveur des services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="aea2c-153">Windows Deployment Services Server Functions</span></span>](windows-deployment-services-server-functions.md)
</dt> <dt>

[<span data-ttu-id="aea2c-154">**PxeRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="aea2c-154">**PxeRegisterCallback**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeregistercallback)
</dt> <dt>

[<span data-ttu-id="aea2c-155">**PxeSendReply**</span><span class="sxs-lookup"><span data-stu-id="aea2c-155">**PxeSendReply**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxesendreply)
</dt> <dt>

[<span data-ttu-id="aea2c-156">**PxeProviderSetAttribute**</span><span class="sxs-lookup"><span data-stu-id="aea2c-156">**PxeProviderSetAttribute**</span></span>](/windows/desktop/api/WdsPxe/nf-wdspxe-pxeprovidersetattribute)
</dt> </dl>

 

 





