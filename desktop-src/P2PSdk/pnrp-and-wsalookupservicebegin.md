---
description: PNRP utilise la fonction WSALookupServiceBegin pour démarrer le processus qui permet à une application d’effectuer les opérations suivantes.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP et WSALookupServiceBegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106522558"
---
# <a name="pnrp-and-wsalookupservicebegin"></a>PNRP et WSALookupServiceBegin

PNRP utilise la fonction [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) pour démarrer le processus qui permet à une application d’effectuer les opérations suivantes :

-   [Résolution d’un nom](#resolving-a-name)
-   [Énumération des clouds réseau](#enumerating-network-clouds)

Les clients qui tentent d’exécuter l’une des fonctions utilisent les fonctions [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** et **WSALookupServiceEnd** .

À l’aide de [**WSANSPIoctl**](winsock-nsp-reference-links.md), le service de recherche peut être utilisé de manière asynchrone. Pour plus d’informations sur l’utilisation des fonctions de service de recherche de manière asynchrone, consultez [PNRP et WSANSPIoctl](pnrp-and-wsanspioctl.md).

Le processus d’utilisation des noms d’homologues diffère de l’utilisation des clouds. Chaque processus est décrit séparément dans cette rubrique.

## <a name="resolving-a-name"></a>Résolution d’un nom

Une application utilise [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) pour obtenir l’adresse IP, le port et le protocole d’un service homologue inscrit sur un autre ordinateur. La fonction **WSALookupServiceBegin** est utilisée pour démarrer le processus de résolution de noms, et pour configurer les paramètres et les restrictions. Un descripteur est retourné et doit être utilisé lors de l’appel de **WSALookupServiceNext** et **WSANSPIoctl**.

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Lors de la résolution d’un nom d’homologue, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRestrictions* doit contenir les valeurs suivantes :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Spécifie la taille de cette structure.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Spécifie un nom d’homologue à résoudre.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Doit être **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Il doit s’agir de **NS \_ PNRPNAME** ou **NS \_ All**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Doit être un **\_ fournisseur NS \_ PNRPNAME** ou **null**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Doit être un nom de Cloud, une chaîne vide ou une **valeur null**. Si cette valeur est **null** ou une chaîne vide, le Cloud par défaut, « global \_ », est utilisé. Dans le cas contraire, il doit pointer vers un nom de Cloud valide.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Doit être un pointeur vers une structure [**BLOB**](winsock-nsp-reference-links.md) ou **null**. Si la **valeur est null**, les valeurs par défaut sont utilisées. S’il est défini, **lpBlob** pointe vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) , et les paramètres spécifiques de la structure **PNRPINFO** doivent être définis. Pour plus d’informations, consultez les descriptions suivantes de la structure PNRPINFO.

</dd> </dl>

PNRPINFO, structure

Si le membre **lpBlob** de la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) est défini, les membres suivants de la structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) doivent être définis :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Spécifie la taille de cette structure.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Spécifie le nombre demandé de résolutions.

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Spécifie le délai d’attente demandé pour les réponses. La valeur par défaut est 30 secondes. La valeur maximale est de 600 secondes (10 minutes).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Doit être l’une des valeurs autorisées. La valeur par défaut est **PNRP \_ résoudre les \_ critères \_ non actifs du nom de l' \_ \_ \_ homologue \_**. Les valeurs valides sont spécifiées par les [**\_ \_ critères de résolution PNRP**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Doit avoir la valeur zéro (0) ou l' **\_ indicateur PNRPINFO**. La valeur par défaut est zéro (0).

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**
</dt> <dd>

Spécifie l’adresse IP de l’indicateur. L’indicateur est utilisé lors de la tentative de recherche du nom de pair le plus proche. Le format de l’indicateur est une adresse IPv6. Si **sahint** n’est pas spécifié lors de la recherche du nom d’homologue le plus proche, une adresse IPv6 de l’ordinateur local est utilisée à la place. Ce membre est ignoré si **dwFlags** n’est pas défini.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

Les indicateurs de \_ retour lup suivants \_ \* sont pris en charge par PNRP :



| Valeur                | Description                                |
|----------------------|--------------------------------------------|
| LUP \_ nom de retour \_    | Retourne un nom et un contexte.                |
| LUP \_ retourner le \_ Commentaire | Retourne un commentaire associé à un nom.  |
| LUP \_ retour \_ addr    | Retourne une adresse associée à un nom. |



 

## <a name="enumerating-network-clouds"></a>Énumération des clouds réseau

### <a name="lpqsrestrictions"></a>lpqsRestrictions

Lors de l’énumération de Clouds, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRestrictions* doit contenir les valeurs suivantes :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Spécifie la taille de cette structure.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Doit avoir la **valeur null**.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Doit être **SVCID \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Doit être **NS \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Doit être un **\_ fournisseur NS \_ PNRPCLOUD** ou **null**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Réservé, doit avoir la **valeur null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Pointeur vers une structure d' [**objet BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) . Si **lpBlob** a la **valeur null**, tous les clouds sont énumérés.

</dd> </dl>

PNRPCLOUDINFO, structure

Lors de l’énumération de Clouds, les membres suivants de la structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) doivent être définis :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Spécifie la taille de cette structure.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Pluie**
</dt> <dd>

Pointe vers une structure qui spécifie les critères que vous pouvez utiliser pour filtrer les résultats de la recherche. Le membre **Cloud. Scope** peut correspondre à l' **\_ étendue PNRP Any \_**, à l’étendue **\_ globale \_ PNRP**, à l' **\_ \_ \_ étendue locale du site PNRP** ou à l' **\_ \_ \_ étendue locale du lien PNRP**. Si **\_ \_ l’étendue PNRP** est spécifiée, tous les clouds sont retournés. Sinon, seuls les clouds qui correspondent au **Cloud. Scope** sont retournés.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

Réservé, doit avoir la valeur zéro (0).

</dd> </dl>

### <a name="dwcontrolflags"></a>dwControlFlags

Les indicateurs de \_ retour lup suivants \_ \* sont pris en charge par PNRP :



| Valeur             | Description                                                       |
|-------------------|-------------------------------------------------------------------|
| LUP \_ nom de retour \_ | Retourne un nom et un contexte.                                       |
| LUP \_ retourne un \_ objet BLOB | Retourne l' [objet BLOB](pnrp-and-blob.md) associé à ce Cloud. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[PNRP et objet BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP et WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP et WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[PNRP et WSANSPIoctl](pnrp-and-wsanspioctl.md)
</dt> <dt>

[PNRP et WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Codes d’erreur du NSP PNRP](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



