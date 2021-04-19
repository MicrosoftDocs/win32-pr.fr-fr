---
title: Méthode IMsTscAxEvents OnDisconnected
description: Appelé lorsque le contrôle client a été déconnecté du serveur de l’hôte de session Bureau à distance (Bureau à distance).
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnDisconnected
- Méthode OnDisconnected Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnDisconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372ad98c73b1b0e90753891e01e46c61a78c23dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513795"
---
# <a name="imstscaxeventsondisconnected-method"></a><span data-ttu-id="13ea0-106">IMsTscAxEvents :: OnDisconnected, méthode</span><span class="sxs-lookup"><span data-stu-id="13ea0-106">IMsTscAxEvents::OnDisconnected method</span></span>

<span data-ttu-id="13ea0-107">Appelé lorsque le contrôle client a été déconnecté du serveur de l’hôte de session Bureau à distance (Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="13ea0-107">Called when the client control has been disconnected from the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="13ea0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13ea0-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a><span data-ttu-id="13ea0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="13ea0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13ea0-110">*discReason* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="13ea0-110">*discReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13ea0-111">Spécifie la raison de la déconnexion.</span><span class="sxs-lookup"><span data-stu-id="13ea0-111">Specifies the reason for the disconnection.</span></span> <span data-ttu-id="13ea0-112">La liste suivante répertorie les codes d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-112">The following is a list of error codes.</span></span> <span data-ttu-id="13ea0-113">Certains de ces codes d’erreur sont définis dans Wincred. h.</span><span class="sxs-lookup"><span data-stu-id="13ea0-113">Some of these error codes are defined in Wincred.h.</span></span>

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span data-ttu-id="13ea0-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span><span class="sxs-lookup"><span data-stu-id="13ea0-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-115">Socket fermé.</span><span class="sxs-lookup"><span data-stu-id="13ea0-115">Socket closed.</span></span>

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span data-ttu-id="13ea0-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="13ea0-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-117">Déconnexion distante par le serveur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-117">Remote disconnection by server.</span></span> <span data-ttu-id="13ea0-118">Il ne s’agit pas d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-118">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span data-ttu-id="13ea0-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span><span class="sxs-lookup"><span data-stu-id="13ea0-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-120">Erreur de décompression.</span><span class="sxs-lookup"><span data-stu-id="13ea0-120">Decompression error.</span></span>

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span data-ttu-id="13ea0-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span><span class="sxs-lookup"><span data-stu-id="13ea0-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-122">Délai de connexion dépassé.</span><span class="sxs-lookup"><span data-stu-id="13ea0-122">Connection timed out.</span></span>

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span data-ttu-id="13ea0-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span><span class="sxs-lookup"><span data-stu-id="13ea0-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-124">Erreur de déchiffrement.</span><span class="sxs-lookup"><span data-stu-id="13ea0-124">Decryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span data-ttu-id="13ea0-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span><span class="sxs-lookup"><span data-stu-id="13ea0-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-126">Échec de la recherche de nom DNS.</span><span class="sxs-lookup"><span data-stu-id="13ea0-126">DNS name lookup failure.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span data-ttu-id="13ea0-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span><span class="sxs-lookup"><span data-stu-id="13ea0-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-128">Échec de la recherche DNS.</span><span class="sxs-lookup"><span data-stu-id="13ea0-128">DNS lookup failed.</span></span>

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span data-ttu-id="13ea0-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span><span class="sxs-lookup"><span data-stu-id="13ea0-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-130">Erreur de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="13ea0-130">Encryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span data-ttu-id="13ea0-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span><span class="sxs-lookup"><span data-stu-id="13ea0-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-132">Échec de l’appel [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="13ea0-132">Windows Sockets [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span data-ttu-id="13ea0-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span><span class="sxs-lookup"><span data-stu-id="13ea0-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-134">Erreur de l’hôte introuvable.</span><span class="sxs-lookup"><span data-stu-id="13ea0-134">Host not found error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span data-ttu-id="13ea0-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span><span class="sxs-lookup"><span data-stu-id="13ea0-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-136">Erreur interne.</span><span class="sxs-lookup"><span data-stu-id="13ea0-136">Internal error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span data-ttu-id="13ea0-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span><span class="sxs-lookup"><span data-stu-id="13ea0-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-138">Erreur de sécurité interne.</span><span class="sxs-lookup"><span data-stu-id="13ea0-138">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span data-ttu-id="13ea0-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span><span class="sxs-lookup"><span data-stu-id="13ea0-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-140">Erreur de sécurité interne.</span><span class="sxs-lookup"><span data-stu-id="13ea0-140">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span data-ttu-id="13ea0-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span><span class="sxs-lookup"><span data-stu-id="13ea0-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-142">La méthode de chiffrement spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="13ea0-142">The encryption method specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span data-ttu-id="13ea0-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span><span class="sxs-lookup"><span data-stu-id="13ea0-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-144">Adresse IP incorrecte spécifiée.</span><span class="sxs-lookup"><span data-stu-id="13ea0-144">Bad IP address specified.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span data-ttu-id="13ea0-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span><span class="sxs-lookup"><span data-stu-id="13ea0-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-146">Les données de sécurité du serveur ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="13ea0-146">Server security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span data-ttu-id="13ea0-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span><span class="sxs-lookup"><span data-stu-id="13ea0-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-148">Les données de sécurité ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="13ea0-148">Security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span data-ttu-id="13ea0-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span><span class="sxs-lookup"><span data-stu-id="13ea0-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-150">L’adresse IP spécifiée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="13ea0-150">The IP address specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span data-ttu-id="13ea0-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span><span class="sxs-lookup"><span data-stu-id="13ea0-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-152">Échec de la négociation de la licence.</span><span class="sxs-lookup"><span data-stu-id="13ea0-152">License negotiation failed.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span data-ttu-id="13ea0-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span><span class="sxs-lookup"><span data-stu-id="13ea0-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-154">Délai d’expiration de la licence.</span><span class="sxs-lookup"><span data-stu-id="13ea0-154">Licensing time-out.</span></span>

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span data-ttu-id="13ea0-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="13ea0-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-156">Déconnexion locale.</span><span class="sxs-lookup"><span data-stu-id="13ea0-156">Local disconnection.</span></span> <span data-ttu-id="13ea0-157">Il ne s’agit pas d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-157">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span data-ttu-id="13ea0-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="13ea0-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-159">Aucune information n'est disponible.</span><span class="sxs-lookup"><span data-stu-id="13ea0-159">No information is available.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span data-ttu-id="13ea0-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span><span class="sxs-lookup"><span data-stu-id="13ea0-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-161">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="13ea0-161">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span data-ttu-id="13ea0-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span><span class="sxs-lookup"><span data-stu-id="13ea0-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-163">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="13ea0-163">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span data-ttu-id="13ea0-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span><span class="sxs-lookup"><span data-stu-id="13ea0-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-165">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="13ea0-165">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span data-ttu-id="13ea0-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="13ea0-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-167">Déconnexion distante par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-167">Remote disconnection by user.</span></span> <span data-ttu-id="13ea0-168">Il ne s’agit pas d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-168">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span data-ttu-id="13ea0-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span><span class="sxs-lookup"><span data-stu-id="13ea0-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-170">Échec de la décompression du certificat du serveur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-170">Failed to unpack server certificate.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span data-ttu-id="13ea0-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span><span class="sxs-lookup"><span data-stu-id="13ea0-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-172">Échec de la [**connexion**](/windows/desktop/api/winsock2/nf-winsock2-connect) à Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="13ea0-172">Windows Sockets [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) failed.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span data-ttu-id="13ea0-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span><span class="sxs-lookup"><span data-stu-id="13ea0-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-174">Échec de l’appel de [**réception**](/windows/desktop/api/winsock/nf-winsock-recv) Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="13ea0-174">Windows Sockets [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span data-ttu-id="13ea0-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span><span class="sxs-lookup"><span data-stu-id="13ea0-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-176">Le délai d’attente a expiré.</span><span class="sxs-lookup"><span data-stu-id="13ea0-176">Time-out occurred.</span></span>

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span data-ttu-id="13ea0-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span><span class="sxs-lookup"><span data-stu-id="13ea0-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-178">Erreur de minuteur interne.</span><span class="sxs-lookup"><span data-stu-id="13ea0-178">Internal timer error.</span></span>

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span data-ttu-id="13ea0-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span><span class="sxs-lookup"><span data-stu-id="13ea0-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-180">Échec de l’appel d' [**envoi**](/windows/desktop/api/winsock2/nf-winsock2-send) Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="13ea0-180">Windows Sockets [**send**](/windows/desktop/api/winsock2/nf-winsock2-send) call failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span data-ttu-id="13ea0-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**Protocole SSL \_ \_Compte Err \_ désactivé** (2823 (0xB07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL\_ERR\_ACCOUNT\_DISABLED** (2823 (0xB07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-182">Le compte est désactivé.</span><span class="sxs-lookup"><span data-stu-id="13ea0-182">The account is disabled.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span data-ttu-id="13ea0-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**Protocole SSL \_ Compte d’erreur \_ \_ expiré** (3591 (0xE07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL\_ERR\_ACCOUNT\_EXPIRED** (3591 (0xE07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-184">Le compte a expiré.</span><span class="sxs-lookup"><span data-stu-id="13ea0-184">The account is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span data-ttu-id="13ea0-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**Protocole SSL \_ Compte d’erreur \_ \_ verrouillé \_** (3335 (0xD07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL\_ERR\_ACCOUNT\_LOCKED\_OUT** (3335 (0xD07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-186">Le compte est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="13ea0-186">The account is locked out.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span data-ttu-id="13ea0-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**Protocole SSL \_ \_ \_ Restriction de compte ERR** (3079 (0xC07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL\_ERR\_ACCOUNT\_RESTRICTION** (3079 (0xC07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-188">Le compte est limité.</span><span class="sxs-lookup"><span data-stu-id="13ea0-188">The account is restricted.</span></span>

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span data-ttu-id="13ea0-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**Protocole SSL \_ Le \_ certificat d’erreur \_ a expiré** (6919 (0x1B07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL\_ERR\_CERT\_EXPIRED** (6919 (0x1B07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-190">Le certificat reçu a expiré.</span><span class="sxs-lookup"><span data-stu-id="13ea0-190">The received certificate is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span data-ttu-id="13ea0-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**Protocole SSL \_ \_ \_ Stratégie de délégation d’erreur** (5639 (0x1607))</span><span class="sxs-lookup"><span data-stu-id="13ea0-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL\_ERR\_DELEGATION\_POLICY** (5639 (0x1607))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-192">La stratégie ne prend pas en charge la délégation des informations d’identification au serveur cible.</span><span class="sxs-lookup"><span data-stu-id="13ea0-192">The policy does not support delegation of credentials to the target server.</span></span>

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span data-ttu-id="13ea0-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**Protocole SSL \_ ERR \_ actualité \_ cred \_ requise \_ par le \_ serveur** (8455 (0x2107))</span><span class="sxs-lookup"><span data-stu-id="13ea0-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL\_ERR\_FRESH\_CRED\_REQUIRED\_BY\_SERVER** (8455 (0x2107))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-194">La stratégie d’authentification serveur n’autorise pas les demandes de connexion à l’aide des informations d’identification enregistrées.</span><span class="sxs-lookup"><span data-stu-id="13ea0-194">The server authentication policy does not allow connection requests using saved credentials.</span></span> <span data-ttu-id="13ea0-195">L’utilisateur doit entrer de nouvelles informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="13ea0-195">The user must enter new credentials.</span></span>

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span data-ttu-id="13ea0-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**Protocole SSL \_ \_ \_ Erreur d’ouverture de session** (2055 (0x807))</span><span class="sxs-lookup"><span data-stu-id="13ea0-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL\_ERR\_LOGON\_FAILURE** (2055 (0x807))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-197">Échec de la connexion.</span><span class="sxs-lookup"><span data-stu-id="13ea0-197">Login failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span data-ttu-id="13ea0-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**Protocole SSL \_ ERR \_ aucune \_ \_ autorité d’authentification** (6151 (0x1807))</span><span class="sxs-lookup"><span data-stu-id="13ea0-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL\_ERR\_NO\_AUTHENTICATING\_AUTHORITY** (6151 (0x1807))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-199">Aucune autorité n’a pu être contactée pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="13ea0-199">No authority could be contacted for authentication.</span></span> <span data-ttu-id="13ea0-200">Le nom de domaine du tiers d’authentification peut être incorrect, le domaine peut être inaccessible ou une relation d’approbation a peut-être échoué.</span><span class="sxs-lookup"><span data-stu-id="13ea0-200">The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span data-ttu-id="13ea0-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**Protocole SSL \_ ERR \_ non de \_ ce type d' \_ utilisateur** (2567 (0xA07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL\_ERR\_NO\_SUCH\_USER** (2567 (0xA07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-202">L’utilisateur spécifié n’a pas de compte.</span><span class="sxs-lookup"><span data-stu-id="13ea0-202">The specified user has no account.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span data-ttu-id="13ea0-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**Protocole SSL \_ Le \_ mot de passe Err \_ a expiré** (3847 (0xF07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL\_ERR\_PASSWORD\_EXPIRED** (3847 (0xF07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-204">Le mot de passe a expiré.</span><span class="sxs-lookup"><span data-stu-id="13ea0-204">The password is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span data-ttu-id="13ea0-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**Protocole SSL \_ Le \_ mot de passe Err \_ doit \_ changer** (4615 (0x1207))</span><span class="sxs-lookup"><span data-stu-id="13ea0-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL\_ERR\_PASSWORD\_MUST\_CHANGE** (4615 (0x1207))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-206">Le mot de passe de l’utilisateur doit être modifié avant d’ouvrir une session pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="13ea0-206">The user password must be changed before logging on for the first time.</span></span>

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span data-ttu-id="13ea0-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**Protocole SSL \_ Stratégie d’erreur \_ \_ NTLM \_ uniquement** (5895 (0x1707))</span><span class="sxs-lookup"><span data-stu-id="13ea0-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL\_ERR\_POLICY\_NTLM\_ONLY** (5895 (0x1707))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-208">La délégation des informations d’identification au serveur cible n’est pas autorisée, sauf si l’authentification mutuelle a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="13ea0-208">Delegation of credentials to the target server is not allowed unless mutual authentication has been achieved.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span data-ttu-id="13ea0-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**Protocole SSL \_ \_Carte à puce Err \_ \_ bloquée** (8711 (0x2207))</span><span class="sxs-lookup"><span data-stu-id="13ea0-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL\_ERR\_SMARTCARD\_CARD\_BLOCKED** (8711 (0x2207))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-210">La carte à puce est bloquée.</span><span class="sxs-lookup"><span data-stu-id="13ea0-210">The smart card is blocked.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span data-ttu-id="13ea0-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**Protocole SSL \_ \_ \_ \_ Code pin d’erreur de carte à puce erronée** (7175 (0x1C07))</span><span class="sxs-lookup"><span data-stu-id="13ea0-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL\_ERR\_SMARTCARD\_WRONG\_PIN** (7175 (0x1C07))</span></span>


</dt> <dd>

<span data-ttu-id="13ea0-212">Un code confidentiel incorrect a été présenté à la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="13ea0-212">An incorrect PIN was presented to the smart card.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13ea0-213">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="13ea0-213">Return value</span></span>

<span data-ttu-id="13ea0-214">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="13ea0-214">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="13ea0-215">Notes</span><span class="sxs-lookup"><span data-stu-id="13ea0-215">Remarks</span></span>

<span data-ttu-id="13ea0-216">Pour récupérer une description de l’erreur de déconnexion, appelez la méthode [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) et transmettez-lui le paramètre *discReason* et la propriété [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) de l’interface [**IMsRdpClient**](imsrdpclient-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="13ea0-216">To retrieve a description of the disconnect error, call the [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) method and pass it the *discReason* parameter and the [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) property of the [**IMsRdpClient**](imsrdpclient-interface.md) interface.</span></span>

<span data-ttu-id="13ea0-217">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="13ea0-217">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13ea0-218">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="13ea0-218">Requirements</span></span>



| <span data-ttu-id="13ea0-219">Condition requise</span><span class="sxs-lookup"><span data-stu-id="13ea0-219">Requirement</span></span> | <span data-ttu-id="13ea0-220">Valeur</span><span class="sxs-lookup"><span data-stu-id="13ea0-220">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13ea0-221">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ea0-221">Minimum supported client</span></span><br/> | <span data-ttu-id="13ea0-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13ea0-222">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="13ea0-223">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="13ea0-223">Minimum supported server</span></span><br/> | <span data-ttu-id="13ea0-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13ea0-224">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="13ea0-225">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="13ea0-225">Type library</span></span><br/>             | <dl> <span data-ttu-id="13ea0-226"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13ea0-226"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="13ea0-227">DLL</span><span class="sxs-lookup"><span data-stu-id="13ea0-227">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13ea0-228"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13ea0-228"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="13ea0-229">IID</span><span class="sxs-lookup"><span data-stu-id="13ea0-229">IID</span></span><br/>                      | <span data-ttu-id="13ea0-230">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="13ea0-230">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="13ea0-231">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="13ea0-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13ea0-232">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="13ea0-232">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

