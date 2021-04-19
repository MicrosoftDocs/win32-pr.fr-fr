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
# <a name="pnrp-and-wsalookupservicenext"></a>PNRP et WSALookupServiceNext

PNRP utilise la fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) pour faire correspondre les requêtes spécifiées dans un appel précédent à **WSALookupServiceBegin**. Les résultats de la fonction **WSALookupServiceNext** sont déterminés par les paramètres de la structure **WSAQUERYSET** passée dans l’appel de fonction **WSALookupServiceBegin** initial. Cette fonction est utilisée pour exécuter les deux fonctions suivantes :

-   Résolution d’un nom d’homologue en une liste d’adresses
-   Énumération des clouds réseau

À l’aide de [**WSANSPIoctl**](winsock-nsp-reference-links.md), le service de recherche peut être utilisé de manière asynchrone. Pour plus d’informations sur l’utilisation des fonctions de service de recherche de manière asynchrone, consultez [PNRP et WSANSPIoctl](pnrp-and-wsanspioctl.md).

La fonction [**WSALookupServiceNext**](winsock-nsp-reference-links.md) se bloque même si **WSANSPIoctl** est appelé. Avant d’appeler **WSALookupServiceNext**, une application doit attendre jusqu’à ce qu’elle reçoive une notification, si le blocage est un problème.

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a>Résolution d’un nom d’homologue en une liste d’adresses

Lors de la résolution d’un nom d’homologue en une liste d’adresses, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retournée dans le paramètre *lpqsResults* contient les valeurs suivantes :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Retourne la taille de la structure.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Retourne un nom d’homologue, si **lup \_ Return \_ Name**, **lup \_ Return \_ All** ou **null** sont spécifiés.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Retourne **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Retourne la **valeur null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Retourne un commentaire : si **lup \_ retourne un \_ Commentaire**, **lup \_ retourne \_ All** ou **null** est spécifié.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Retourne **NS \_ PNRPNAME**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Retourne **le \_ fournisseur NS \_ PNRPNAME**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Retourne le nom du Cloud si **lup \_ Return \_ Name**, **lup \_ Return \_ All** ou **null** sont spécifiés.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Retourne zéro (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Retourne la **valeur null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Retourne le nombre d’entrées dans le \_ tableau d’informations CSADDR si **lup \_ renvoie \_ addr**, **lup \_ Return \_ All** ou **null** sont spécifiés. Cette valeur et les informations contenues dans **lpcsaBuffer** sont les bits clés des informations retournées dans cette structure.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Retourne un pointeur vers un tableau de \_ structures CSADDR info si **lup \_ renvoie \_ addr**, **lup \_ Return \_ All** ou **null** est spécifié. Cette mémoire tampon et la valeur dans **dwNumberOfCsAddrs** sont les bits d’informations de clé retournés dans cette structure.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Retourne zéro (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Retourne la **valeur null**.

</dd> </dl>

## <a name="enumerating-network-clouds"></a>Énumération des clouds réseau

Lors de l’énumération de Clouds, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) retournée dans le paramètre *lpqsResults* contient les valeurs suivantes :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Retourne la taille de la structure.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Retourne un nom de Cloud, si **lup \_ Return \_ Name**, **lup \_ Return \_ All** ou **null** sont spécifiés.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Retourne **SVCID \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Retourne la **valeur null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Retourne la **valeur null**.

</dd> <dt>

<span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**
</dt> <dd>

Retourne **NS \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**
</dt> <dd>

Retourne **le \_ fournisseur NS \_ PNRPCLOUD**.

</dd> <dt>

<span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**
</dt> <dd>

Retourne la **valeur null**.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Retourne zéro (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Retourne la **valeur null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Retourne zéro (0).

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Retourne la **valeur null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Retourne zéro (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Retourne un pointeur vers une structure [**BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) , si **lup \_ retourne un \_ objet BLOB**, **lup \_ retourne \_ All** ou si la **valeur null** est spécifiée.

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a>PNRPCLOUDINFO, structure

Lors de l’énumération des noms de Cloud, les valeurs suivantes sont retournées dans la structure [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

La taille de cette structure.

</dd> <dt>

<span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Pluie**
</dt> <dd>

Valeur de Cloud réelle.

</dd> <dt>

<span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**
</dt> <dd>

État actuel d’un Cloud. [**PNRP \_ \_État du Cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) spécifie les valeurs valides.

</dd> <dt>

<span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**
</dt> <dd>

Indique qu’un nom de Cloud est valide sur un réseau ou valide uniquement sur un ordinateur actuel. [**PNRP \_ \_Indicateurs de Cloud**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) spécifie les valeurs valides. Certains noms de Cloud sont valides sur tous les ordinateurs du même réseau. Les autres noms de Cloud sont valides uniquement sur un ordinateur actuel et peuvent être valides uniquement pendant une période donnée.

-   Si **enCloudFlags** est défini sur **le \_ nom de Cloud PNRP \_ \_ local,** le nom n’est valide que localement.
-   Si **enCloudFlags** n’est pas défini, le nom du Cloud peut être transféré à d’autres ordinateurs.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[PNRP et objet BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP et WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
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
</dt> <dt>

[**WSALookupServiceBegin**](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



