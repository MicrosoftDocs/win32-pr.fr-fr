---
description: PNRP utilise la fonction WSALookupServiceNext pour faire correspondre les requêtes spécifiées dans un appel précédent à WSALookupServiceBegin.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP et WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517709"
---
# <a name="pnrp-and-wsalookupservicenext"></a><span data-ttu-id="616b8-103">PNRP et WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="616b8-103">PNRP and WSALookupServiceNext</span></span>

<span data-ttu-id="616b8-104">PNRP utilise la fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) pour faire correspondre les requêtes spécifiées dans un appel précédent à **WSALookupServiceBegin**.</span><span class="sxs-lookup"><span data-stu-id="616b8-104">PNRP uses the [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function to match queries specified in a previous call to **WSALookupServiceBegin**.</span></span> <span data-ttu-id="616b8-105">Les résultats de la fonction **WSALookupServiceNext** sont déterminés par les paramètres de la structure **WSAQUERYSET** passée dans l’appel de fonction **WSALookupServiceBegin** initial.</span><span class="sxs-lookup"><span data-stu-id="616b8-105">The results of the **WSALookupServiceNext** function are determined by settings in the **WSAQUERYSET** structure passed in the initial **WSALookupServiceBegin** function call.</span></span> <span data-ttu-id="616b8-106">Cette fonction est utilisée pour exécuter les deux fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="616b8-106">This function is used to perform the following two functions:</span></span>

-   <span data-ttu-id="616b8-107">Résolution d’un nom d’homologue en une liste d’adresses</span><span class="sxs-lookup"><span data-stu-id="616b8-107">Resolving a peer name to a list of addresses</span></span>
-   <span data-ttu-id="616b8-108">Énumération des clouds réseau</span><span class="sxs-lookup"><span data-stu-id="616b8-108">Enumerating network clouds</span></span>

<span data-ttu-id="616b8-109">À l’aide de [**WSANSPIoctl**](winsock-nsp-reference-links.md), le service de recherche peut être utilisé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="616b8-109">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="616b8-110">Pour plus d’informations sur l’utilisation des fonctions de service de recherche de manière asynchrone, consultez [PNRP et WSANSPIoctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="616b8-110">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="616b8-111">La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloque même si **WSANSPIoctl** est appelé.</span><span class="sxs-lookup"><span data-stu-id="616b8-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="616b8-112">Avant d’appeler **WSALookupServiceNext**, une application doit attendre jusqu’à ce qu’elle reçoive une notification, si le blocage est un problème.</span><span class="sxs-lookup"><span data-stu-id="616b8-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a><span data-ttu-id="616b8-113">Résolution d’un nom d’homologue en une liste d’adresses</span><span class="sxs-lookup"><span data-stu-id="616b8-113">Resolving a Peer Name to a List of Addresses</span></span>

<span data-ttu-id="616b8-114">Lors de la résolution d’un nom d’homologue en une liste d’adresses, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retournée dans le paramètre *lpqsResults* contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="616b8-114">When resolving a peer name to a list of addresses, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="616b8-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="616b8-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-116">Retourne la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="616b8-116">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="616b8-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-118">Retourne un nom d’homologue, si **lup \_ Return \_ Name**, **lup \_ Return \_ All** ou **null** sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="616b8-118">Returns a peer name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="616b8-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-120">Retourne **SVCID \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="616b8-120">Returns **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="616b8-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-122">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-122">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="616b8-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-124">Retourne un commentaire : si **lup \_ retourne un \_ Commentaire**, **lup \_ retourne \_ All** ou **null** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="616b8-124">Returns a comment—if **LUP\_RETURN\_COMMENT**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="616b8-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-126">Retourne **NS \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="616b8-126">Returns **NS\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="616b8-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-128">Retourne **le \_ fournisseur NS \_ PNRPNAME**.</span><span class="sxs-lookup"><span data-stu-id="616b8-128">Returns **NS\_PROVIDER\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="616b8-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-130">Retourne le nom du Cloud si **lup \_ Return \_ Name**, **lup \_ Return \_ All** ou **null** sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="616b8-130">Returns the cloud name if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="616b8-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-132">Retourne zéro (0).</span><span class="sxs-lookup"><span data-stu-id="616b8-132">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="616b8-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="616b8-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-134">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-134">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="616b8-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-136">Retourne le nombre d’entrées dans le \_ tableau d’informations CSADDR si **lup \_ renvoie \_ addr**, **lup \_ Return \_ All** ou **null** sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="616b8-136">Returns the number of entries in the CSADDR\_INFO array if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="616b8-137">Cette valeur et les informations contenues dans **lpcsaBuffer** sont les bits clés des informations retournées dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="616b8-137">This value and the information in **lpcsaBuffer** are the key bits of information returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="616b8-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-139">Retourne un pointeur vers un tableau de \_ structures CSADDR info si **lup \_ renvoie \_ addr**, **lup \_ Return \_ All** ou **null** est spécifié.</span><span class="sxs-lookup"><span data-stu-id="616b8-139">Returns a pointer to an array of CSADDR\_INFO structures if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="616b8-140">Cette mémoire tampon et la valeur dans **dwNumberOfCsAddrs** sont les bits d’informations de clé retournés dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="616b8-140">This buffer and the value in **dwNumberOfCsAddrs** are the key information bits returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="616b8-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-142">Retourne zéro (0).</span><span class="sxs-lookup"><span data-stu-id="616b8-142">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="616b8-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="616b8-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-144">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-144">Returns **NULL**.</span></span>

</dd> </dl>

## <a name="enumerating-network-clouds"></a><span data-ttu-id="616b8-145">Énumération des clouds réseau</span><span class="sxs-lookup"><span data-stu-id="616b8-145">Enumerating Network Clouds</span></span>

<span data-ttu-id="616b8-146">Lors de l’énumération de Clouds, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retournée dans le paramètre *lpqsResults* contient les valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="616b8-146">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="616b8-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="616b8-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-148">Retourne la taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="616b8-148">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span><span class="sxs-lookup"><span data-stu-id="616b8-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-150">Retourne un nom de Cloud, si **lup \_ Return \_ Name**, **lup \_ Return \_ All** ou **null** sont spécifiés.</span><span class="sxs-lookup"><span data-stu-id="616b8-150">Returns a cloud name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span><span class="sxs-lookup"><span data-stu-id="616b8-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-152">Retourne **SVCID \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="616b8-152">Returns **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span><span class="sxs-lookup"><span data-stu-id="616b8-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-154">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-154">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span><span class="sxs-lookup"><span data-stu-id="616b8-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-156">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-156">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span><span class="sxs-lookup"><span data-stu-id="616b8-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-158">Retourne **NS \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="616b8-158">Returns **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span><span class="sxs-lookup"><span data-stu-id="616b8-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-160">Retourne **le \_ fournisseur NS \_ PNRPCLOUD**.</span><span class="sxs-lookup"><span data-stu-id="616b8-160">Returns **NS\_PROVIDER\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span><span class="sxs-lookup"><span data-stu-id="616b8-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-162">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-162">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span><span class="sxs-lookup"><span data-stu-id="616b8-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-164">Retourne zéro (0).</span><span class="sxs-lookup"><span data-stu-id="616b8-164">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="616b8-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span><span class="sxs-lookup"><span data-stu-id="616b8-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-166">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-166">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span><span class="sxs-lookup"><span data-stu-id="616b8-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-168">Retourne zéro (0).</span><span class="sxs-lookup"><span data-stu-id="616b8-168">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="616b8-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span><span class="sxs-lookup"><span data-stu-id="616b8-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-170">Retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="616b8-170">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span><span class="sxs-lookup"><span data-stu-id="616b8-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-172">Retourne zéro (0).</span><span class="sxs-lookup"><span data-stu-id="616b8-172">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="616b8-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span><span class="sxs-lookup"><span data-stu-id="616b8-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-174">Retourne un pointeur vers une structure [**BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) , si **lup \_ retourne un \_ objet BLOB**, **lup \_ retourne \_ All** ou si la **valeur null** est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="616b8-174">Returns a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure—if **LUP\_RETURN\_BLOB**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a><span data-ttu-id="616b8-175">PNRPCLOUDINFO, structure</span><span class="sxs-lookup"><span data-stu-id="616b8-175">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="616b8-176">Lors de l’énumération des noms de Cloud, les valeurs suivantes sont retournées dans la structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :</span><span class="sxs-lookup"><span data-stu-id="616b8-176">When enumerating cloud names, the following values are returned in the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure:</span></span>

<dl> <dt>

<span data-ttu-id="616b8-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="616b8-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-178">La taille de cette structure.</span><span class="sxs-lookup"><span data-stu-id="616b8-178">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Pluie**</span><span class="sxs-lookup"><span data-stu-id="616b8-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-180">Valeur de Cloud réelle.</span><span class="sxs-lookup"><span data-stu-id="616b8-180">The actual cloud value.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span><span class="sxs-lookup"><span data-stu-id="616b8-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-182">État actuel d’un Cloud.</span><span class="sxs-lookup"><span data-stu-id="616b8-182">The current state of a cloud.</span></span> <span data-ttu-id="616b8-183">[**PNRP \_ \_État du Cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) spécifie les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="616b8-183">[**PNRP\_CLOUD\_STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifies the valid values.</span></span>

</dd> <dt>

<span data-ttu-id="616b8-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span><span class="sxs-lookup"><span data-stu-id="616b8-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span></span>
</dt> <dd>

<span data-ttu-id="616b8-185">Indique qu’un nom de Cloud est valide sur un réseau ou valide uniquement sur un ordinateur actuel.</span><span class="sxs-lookup"><span data-stu-id="616b8-185">Indicates that a cloud name is valid on a network, or only valid on a current computer.</span></span> <span data-ttu-id="616b8-186">[**PNRP \_ \_Indicateurs de Cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) spécifie les valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="616b8-186">[**PNRP\_CLOUD\_FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifies the valid values.</span></span> <span data-ttu-id="616b8-187">Certains noms de Cloud sont valides sur tous les ordinateurs du même réseau.</span><span class="sxs-lookup"><span data-stu-id="616b8-187">Some cloud names are valid on any computer on the same network.</span></span> <span data-ttu-id="616b8-188">Les autres noms de Cloud sont valides uniquement sur un ordinateur actuel et peuvent être valides uniquement pendant une période donnée.</span><span class="sxs-lookup"><span data-stu-id="616b8-188">Other cloud names are valid only on a current computer, and may be valid only for a period of time.</span></span>

-   <span data-ttu-id="616b8-189">Si **enCloudFlags** est défini sur **le \_ nom de Cloud PNRP \_ \_ local,** le nom n’est valide que localement.</span><span class="sxs-lookup"><span data-stu-id="616b8-189">If **enCloudFlags** is set to **PNRP\_CLOUD\_NAME\_LOCAL,** the name is only valid locally.</span></span>
-   <span data-ttu-id="616b8-190">Si **enCloudFlags** n’est pas défini, le nom du Cloud peut être transféré à d’autres ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="616b8-190">If **enCloudFlags** is not set, then the cloud name can be transferred to other computers.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="616b8-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="616b8-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616b8-192">PNRP et objet BLOB</span><span class="sxs-lookup"><span data-stu-id="616b8-192">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="616b8-193">PNRP et WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="616b8-193">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="616b8-194">PNRP et WSANSPIoctl</span><span class="sxs-lookup"><span data-stu-id="616b8-194">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="616b8-195">PNRP et WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="616b8-195">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="616b8-196">**PNRPCLOUDINFO**</span><span class="sxs-lookup"><span data-stu-id="616b8-196">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="616b8-197">**PNRPINFO**</span><span class="sxs-lookup"><span data-stu-id="616b8-197">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="616b8-198">Codes d’erreur du NSP PNRP</span><span class="sxs-lookup"><span data-stu-id="616b8-198">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="616b8-199">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="616b8-199">**WSALookupServiceBegin**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



