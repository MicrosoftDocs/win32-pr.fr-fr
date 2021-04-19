---
description: PNRP utilise la fonction WSASetService pour inscrire ou supprimer des noms d’homologue.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP et WSASetService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527897"
---
# <a name="pnrp-and-wsasetservice"></a>PNRP et WSASetService

PNRP utilise la fonction [**WSASetService**](winsock-nsp-reference-links.md) pour inscrire ou supprimer des [noms d’homologue](peer-names.md).

## <a name="registering-a-name"></a>Inscription d’un nom

L’inscription comprend un nom d’homologue et un ensemble de points de terminaison dans lesquels un service peut être contacté. Une inscription est spécifique à un Cloud PNRP. Une fois qu’un homologue est inscrit, il y a un délai entre l’inscription et la propagation des informations d’inscription à d’autres nœuds. Pendant ce temps, les autres nœuds peuvent ne pas être en mesure de résoudre un homologue nouvellement inscrit.

L’inscription du service n’est pas persistante.

-   Si un processus client qui inscrit un nom d’homologue s’arrête ou appelle [**WSACleanup**](winsock-nsp-reference-links.md), le nom de l’homologue n’est pas inscrit.
-   Si un nom d’homologue spécifié est déjà inscrit dans le même Cloud par le processus en cours, il est remplacé par de nouvelles valeurs d’inscription.

Lors de l’inscription d’un nom d’homologue, les valeurs de paramètre suivantes doivent être indiquées :

-   le paramètre *essOperation* doit avoir la valeur **RNRSERVICE \_ Register**.
-   le paramètre *dwControlFlags* doit être égal à zéro (0).

Lors de l’inscription d’un nom d’homologue, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRegInfo* doit contenir les valeurs suivantes :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Spécifie la taille de cette structure.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Spécifie un nom d’homologue à inscrire. Si le [nom d’homologue](peer-names.md) n’est pas sécurisé, l’identité est facultative. Si l’identité est spécifiée comme étant **null**, PNRP utilise l’identité locale de l’ordinateur, par défaut.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Doit être SVCID \_ PNRPNAME.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignoré. Affectez la valeur **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignoré. Toutefois, la chaîne doit toujours contenir moins de 40 caractères, y compris la marque de fin **null** .

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

Doit être un nom de Cloud, une chaîne vide ou une **valeur null**. Si cette valeur est **null** ou une chaîne vide, le Cloud par défaut, « global », est utilisé. Dans le cas contraire, il doit pointer vers un nom de Cloud valide.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignoré. Affectez la valeur **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Spécifie le nombre d’adresses inscrites par un service. Le nombre maximal d’adresses pouvant être inscrites pour un seul nom est de 10.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Pointeur vers une liste d’adresses à inscrire.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Pointeur vers une structure d' [**objet BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) . Les paramètres spécifiques de la structure **PNRPINFO** doivent être définis. Pour plus d’informations, consultez la section structure **PNRPINFO** suivante.

</dd> </dl>

## <a name="pnrpinfo-structure"></a>PNRPINFO, structure

Si le membre **lpBlob** de la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) est défini, les membres suivants de la structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) doivent être définis :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Spécifie la taille de cette structure.

</dd> <dt>

<span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**
</dt> <dd>

Spécifie l’identité du nom d’homologue créé à l’aide de [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Si un nom d’homologue n’est pas sécurisé, l’identité est facultative. Si l’identité est spécifiée comme étant **null**, PNRP utilise l’identité locale de l’ordinateur, par défaut.

</dd> <dt>

<span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> <dt>

<span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> <dt>

<span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**
</dt> <dd>

Spécifie le nombre de secondes entre les opérations d’actualisation.

</dd> <dt>

<span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**
</dt> <dd>

Doit avoir la valeur zéro (0) ou l' **\_ indicateur PNRPINFO**. La valeur par défaut est zéro (0). Cela signifie que la partie emplacement du service de l’ID PNRP est créée à l’aide de l’adresse IP dans **sahint**. Dans le cas contraire, l’emplacement du service est généré à l’aide de la première adresse IP de la première entrée IPv6 du membre **lpcsaBuffer** .

</dd> <dt>

<span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**
</dt> <dd>

Spécifie l’adresse IPv6 de l’indicateur.

</dd> <dt>

<span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> </dl>

## <a name="unregistering-a-peer-name"></a>Annulation de l’inscription d’un nom d’homologue

La liste suivante identifie les informations importantes sur l’annulation de l’inscription d’un nom d’homologue.

-   Seule une application qui inscrit un nom d’homologue peut annuler son inscription.
-   Un nom d’homologue est annulé automatiquement si [**WSACleanup**](winsock-nsp-reference-links.md) est appelé.
-   Le protocole PNRP supprime toujours l’enregistrement complet du nom de service. Elle n’autorise pas la suppression d’adresses individuelles.
-   Lors de l’annulation de l’inscription d’un nom, le paramètre *essOperation* doit avoir la valeur **RNRSERVICE \_ Delete**.
-   PNRP ne prend pas en charge la valeur **RNRSERVICE \_ Unregister**.
-   Le paramètre *dwControlFlags* doit avoir la valeur zéro (0).

Lors de l’annulation de l’inscription d’un nom, la structure [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) référencée par le paramètre *lpqsRegInfo* doit contenir les valeurs suivantes :

<dl> <dt>

<span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize nul**
</dt> <dd>

Spécifie la taille de cette structure.

</dd> <dt>

<span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**
</dt> <dd>

Spécifie un nom d’homologue dont l’inscription doit être annulée.

</dd> <dt>

<span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**
</dt> <dd>

Doit être **SVCID \_ PNRPNAME**.

</dd> <dt>

<span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**
</dt> <dd>

Ignoré. Affectez la valeur **null**.

</dd> <dt>

<span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**
</dt> <dd>

Ignoré. Affectez la valeur **null**.

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

Doit être un nom de Cloud, une chaîne vide ou une **valeur null**. Si cette valeur est **null** ou une chaîne vide, le Cloud par défaut, « global », est utilisé. Dans le cas contraire, il doit pointer vers un nom de Cloud valide.

</dd> <dt>

<span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> <dt>

<span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**
</dt> <dd>

Ignoré. Affectez la valeur **null**.

</dd> <dt>

<span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**
</dt> <dd>

Ignoré. Affectez la valeur **null**.

</dd> <dt>

<span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**
</dt> <dd>

Ignoré. Affectez la valeur **null**.

</dd> <dt>

<span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**
</dt> <dd>

Ignoré. A la valeur zéro (0).

</dd> <dt>

<span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**
</dt> <dd>

Pointeur vers une structure d' [**objet BLOB**](winsock-nsp-reference-links.md) qui pointe vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) . Le membre **lpszIdentity** de la structure **lpBlob** identifie le nom de l’identité qui est utilisée pour enregistrer un nom d’homologue. Les membres restants doivent être définis sur les mêmes valeurs que celles utilisées lors de l’inscription d’un nom.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[PNRP et objet BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP et WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[Codes d’erreur du NSP PNRP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSACleanup**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSASetService**
</dt> </dl>

 

 



