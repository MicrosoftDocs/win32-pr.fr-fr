---
title: Constantes de type NAP (NapTypes. h)
description: Les constantes NAP suivantes sont définies.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110570"
---
# <a name="nap-type-constants"></a>Constantes de type NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

Les constantes NAP suivantes sont définies.

Les constantes NAP suivantes sont définies dans NapTypes. h :

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



Nombre maximal d’objets [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) type-length-value (TLV) associés à un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Taille maximale, en octets, d’un objet [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) associé à un paquet de déclaration d’intégrité ([**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh)).


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



Taille minimale, en octets, d’un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Taille maximale, en octets, d’un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) .


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/sizeof (DWORD)
</dt> <dt>



Nombre maximal de valeurs DWORD associées à un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x4
</dt> <dt>



Nombre maximal d’adresses IPv4 associées à un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x10
</dt> <dt>



Nombre maximal d’adresses IPv6 associées à un [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute).


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



Longueur maximale d’une chaîne spécifiée par la structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**
</dt> <dd> <dl> <dt>

(maxStringLength + 1) \* sizeof (WCHAR)
</dt> <dt>



Longueur maximale, en octets, d’une chaîne spécifiée par la structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) .


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Nombre maximal d’entités d’intégrité système, telles que les validateurs d’intégrité et les Sha.


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**
</dt> <dd> <dl> <dt>

\[Plage (0, maxSystemHealthEntityCount)\] 
</dt> <dt>



Plage de valeurs possibles pour le nombre d’entités d’intégrité du système.


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Nombre maximal d’entités d’application, telles que QEC.


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**
</dt> <dd> <dl> <dt>

\[Plage (0, maxEnforcerCount)\]
</dt> <dt>



Plage de valeurs possibles pour le nombre d’entités d’application.


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**
</dt> <dd> <dl> <dt>

0xC8
</dt> <dt>



Taille maximale, en octets, d’une structure [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) .


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Nombre maximal d’objets [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) associés à une entité d’application.


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**
</dt> <dd> <dl> <dt>

maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer
</dt> <dt>



Nombre maximal de connexions SoH mises en cache pour toutes les entités d’intégrité du système et d’application.


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Spécifie qu’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)est dû à une nouvelle demande, et non à une demande mise en cache. Cet indicateur est utilisé par l’agent NAP sur un objet [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) .


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Spécifie que la correction est requise. Cet indicateur est utilisé par un SHA.


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Nombre de catégories d’échec contenues dans une structure [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Le composant est un client de contrainte de mise en quarantaine (QEC) qui envoie un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) intrabande lors de l’authentification de la connexion.

> [!Note]  
> Cette valeur n’est pas utilisée par les Sha et les validateurs d’intégrité du système.

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Le composant est un QEC qui implémente [**INapCertRelyingParty**](inapcertrelyingparty.md) et doit interagir avec le serveur de certificats d’intégrité (HCS) afin d’obtenir un certificat d’intégrité.

> [!Note]  
> Cette valeur n’est pas utilisée par les Sha et les validateurs d’intégrité du système.

 


</dt> </dl> </dd> </dl>

Les constantes NAP suivantes sont définies dans NapEnforcementClient. h.

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x0FA0
</dt> <dt>



Taille maximale par défaut, en octets, d’un paquet SoH.


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



Taille maximale possible, en octets, d’un paquet SoH.


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x012C
</dt> <dt>



Plus petite taille maximale possible, en octets, d’un paquet SoH. La taille réelle du paquet SoH peut être inférieure à **minProtocolMaxSize**.


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**
</dt> <dd> <dl> <dt>

Plage (minProtocolMaxSize, maxProtocolMaxSize)
</dt> <dt>



Plage de valeurs possibles pour la taille maximale d’un paquet SoH.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                                                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                                                                                |
| En-tête<br/>                   | <dl> <dt>NapTypes. h ; </dt> <dt>NapEnforcementClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Constantes NAP**](nap-constants.md)
</dt> </dl>

 

 





