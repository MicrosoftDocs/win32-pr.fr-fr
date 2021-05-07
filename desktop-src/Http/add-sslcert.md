---
title: add sslcert
description: Ajoute une nouvelle liaison de certificat de serveur SSL (Secure Sockets Layer) (SSL) et les stratégies de certificat client correspondantes pour une adresse IP et un port.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- Ajouter sslcert HTTP
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309050be35748f39eefc8b40b8e590f8f6889fde
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644191"
---
# <a name="add-sslcert"></a><span data-ttu-id="04e43-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="04e43-104">add sslcert</span></span>

<span data-ttu-id="04e43-105">Ajoute une nouvelle liaison de certificat de serveur SSL (Secure Sockets Layer) (SSL) et les stratégies de certificat client correspondantes pour une adresse IP et un port.</span><span class="sxs-lookup"><span data-stu-id="04e43-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a><span data-ttu-id="04e43-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04e43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e43-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = adresse IP : port\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP Address:port\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-108">Spécifie l’adresse IP et le port de la liaison.</span><span class="sxs-lookup"><span data-stu-id="04e43-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash = chaîne\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-110">Spécifie le hachage SHA du certificat.</span><span class="sxs-lookup"><span data-stu-id="04e43-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="04e43-111">Ce hachage a une longueur de 20 octets et est spécifié sous forme de chaîne hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="04e43-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[AppID = GUID\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-113">Spécifie le GUID permettant d’identifier l’application propriétaire.</span><span class="sxs-lookup"><span data-stu-id="04e43-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename = chaîne\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-115">Spécifie le nom du stockage pour le certificat.</span><span class="sxs-lookup"><span data-stu-id="04e43-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="04e43-116">Défini par défaut sur MY.</span><span class="sxs-lookup"><span data-stu-id="04e43-116">Defaults to MY.</span></span> <span data-ttu-id="04e43-117">Le certificat doit être stocké dans le contexte de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="04e43-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {activer la \| désactivation}\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-119">Active ou turnsoff la vérification de la révocation des certificats clients.</span><span class="sxs-lookup"><span data-stu-id="04e43-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {activer la \| désactivation}\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-121">Active ou désactive l’utilisation du certificat client mis en cache uniquement pour la vérification de la révocation.</span><span class="sxs-lookup"><span data-stu-id="04e43-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {activer la \| désactivation}\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-123">Active ou désactive la vérification de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="04e43-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="04e43-124">Par défaut, l’utilisation est activée.</span><span class="sxs-lookup"><span data-stu-id="04e43-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[RevocationFreshnessTime = u-int\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-126">Spécifie l’intervalle de temps à vérifier pour une liste de révocation de certificats (CRL) mise à jour.</span><span class="sxs-lookup"><span data-stu-id="04e43-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="04e43-127">Si cette valeur est égale à 0, la nouvelle liste de révocation de certificats est mise à jour uniquement si la précédente expire (en secondes).</span><span class="sxs-lookup"><span data-stu-id="04e43-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="04e43-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[UrlRetrievalTimeout = u-int\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-129">Spécifie l’intervalle de délai d’attente pour les tentatives de récupération de la liste de révocation de certificats pour l’URL distante (en millisecondes).</span><span class="sxs-lookup"><span data-stu-id="04e43-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="04e43-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[SslCtlIdentifier = chaîne\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-131">Répertorie les émetteurs de certificats qui peuvent être approuvés.</span><span class="sxs-lookup"><span data-stu-id="04e43-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="04e43-132">Cette liste peut être un sous-ensemble des émetteurs de certificats qui sont approuvés par l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="04e43-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[SslCtlStoreName = chaîne\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-134">Spécifie le nom du magasin sous l' \_ ordinateur local où SslCtlIdentifier est stocké.</span><span class="sxs-lookup"><span data-stu-id="04e43-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {activer la \| désactivation}\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-136">Active ou désactive les mappeurs DS.</span><span class="sxs-lookup"><span data-stu-id="04e43-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="04e43-137">Par défaut, elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="04e43-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="04e43-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation = {activer la \| désactivation}\]**</span><span class="sxs-lookup"><span data-stu-id="04e43-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="04e43-139">Active ou désactive la négociation du certificat.</span><span class="sxs-lookup"><span data-stu-id="04e43-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="04e43-140">Par défaut, elle est désactivée.</span><span class="sxs-lookup"><span data-stu-id="04e43-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="04e43-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="04e43-141">Examples</span></span>

<span data-ttu-id="04e43-142">**Ajouter sslcert ipport = 1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="04e43-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="04e43-143">**certhash = 0102030405060708090A0B0C0D0E0F1011121314**</span><span class="sxs-lookup"><span data-stu-id="04e43-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="04e43-144">**AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="04e43-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




