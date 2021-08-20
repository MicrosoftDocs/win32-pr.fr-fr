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
ms.openlocfilehash: 721931bfa05a96ca47fd69f643a02076201bb5f93eff003afa83714f2d14b519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950948"
---
# <a name="add-sslcert"></a>add sslcert

Ajoute une nouvelle liaison de certificat de serveur SSL (Secure Sockets Layer) (SSL) et les stratégies de certificat client correspondantes pour une adresse IP et un port.

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

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = adresse IP : port\]**
</dt> <dd>

Spécifie l’adresse IP et le port de la liaison.

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash = chaîne\]**
</dt> <dd>

Spécifie le hachage SHA du certificat. Ce hachage a une longueur de 20 octets et est spécifié sous forme de chaîne hexadécimale.

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[AppID = GUID\]**
</dt> <dd>

Spécifie le GUID permettant d’identifier l’application propriétaire.

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename = chaîne\]**
</dt> <dd>

Spécifie le nom du stockage pour le certificat. Défini par défaut sur MY. Le certificat doit être stocké dans le contexte de l’ordinateur local.

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {activer la \| désactivation}\]**
</dt> <dd>

Active ou turnsoff la vérification de la révocation des certificats clients.

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {activer la \| désactivation}\]**
</dt> <dd>

Active ou désactive l’utilisation du certificat client mis en cache uniquement pour la vérification de la révocation.

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {activer la \| désactivation}\]**
</dt> <dd>

Active ou désactive la vérification de l’utilisation. Par défaut, l’utilisation est activée.

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[RevocationFreshnessTime = u-int\]**
</dt> <dd>

Spécifie l’intervalle de temps à vérifier pour une liste de révocation de certificats (CRL) mise à jour. Si cette valeur est égale à 0, la nouvelle liste de révocation de certificats est mise à jour uniquement si la précédente expire (en secondes).

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[UrlRetrievalTimeout = u-int\]**
</dt> <dd>

Spécifie l’intervalle de délai d’attente pour les tentatives de récupération de la liste de révocation de certificats pour l’URL distante (en millisecondes).

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[SslCtlIdentifier = chaîne\]**
</dt> <dd>

Répertorie les émetteurs de certificats qui peuvent être approuvés. Cette liste peut être un sous-ensemble des émetteurs de certificats qui sont approuvés par l’ordinateur.

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[SslCtlStoreName = chaîne\]**
</dt> <dd>

Spécifie le nom du magasin sous l' \_ ordinateur local où SslCtlIdentifier est stocké.

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {activer la \| désactivation}\]**
</dt> <dd>

Active ou désactive les mappeurs DS. Par défaut, elle est désactivée.

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation = {activer la \| désactivation}\]**
</dt> <dd>

Active ou désactive la négociation du certificat. Par défaut, elle est désactivée.

</dd> </dl>

## <a name="examples"></a>Exemples

**Ajouter sslcert ipport = 1.1.1.1:443**

**certhash = 0102030405060708090A0B0C0D0E0F1011121314**

**AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}**

 

 




