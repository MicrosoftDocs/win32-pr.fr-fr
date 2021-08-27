---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_WINSType
description: la méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource Windows Internet Name Service (WINS).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_WINSType
- MicrosoftDNS_WINSType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f39b360c29ca859c0d0fd0188f0b065dec58293207c27e0a0267572472aabe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077049"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a>Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS WINSType

la méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource Windows Internet Name Service (WINS).

## <a name="syntax"></a>Syntaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DnsServerName* \[ dans\]
</dt> <dd>

Nom de domaine complet ou adresse IP du serveur DNS qui contient ce RR.

</dd> <dt>

*ContainerName* \[ dans\]
</dt> <dd>

Nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient ce RR.

</dd> <dt>

*OwnerName* \[ dans\]
</dt> <dd>

Nom du propriétaire de l’enregistrement de ressource.

</dd> <dt>

*RecordClass* \[ dans, facultatif\]
</dt> <dd>

Classe de l’enregistrement de ressource. La valeur par défaut est 1. Les valeurs suivantes sont valides.



| Valeur                                                                                                | Signification                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | DANS (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ dans, facultatif\]
</dt> <dd>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de résolution DNS.

</dd> <dt>

*MappingFlag* \[ dans\]
</dt> <dd>

Indicateur de mappage WINS qui spécifie si l’enregistrement doit être inclus dans la réplication de zone. Elle ne peut avoir que deux valeurs : 0x80000000 et 0x00010000 correspondant respectivement aux indicateurs de réplication et de non-réplication (enregistrement local). Les valeurs suivantes sont valides.



| Valeur                                                                                                                                               | Signification                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Indicateur de réplication<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Indicateur de non-réplication (enregistrement local)<br/> |



 

</dd> <dt>

*LookupTimeout* \[ dans\]
</dt> <dd>

Durée, en secondes, pendant laquelle un serveur DNS tente de résoudre à l’aide de la recherche WINS.

</dd> <dt>

*CacheTimeout* \[ dans\]
</dt> <dd>

Durée, en secondes, pendant laquelle un serveur DNS qui utilise WINS peut mettre en cache la réponse du serveur WINS.

</dd> <dt>

*WinsServers* \[ dans\]
</dt> <dd>

Liste des adresses IP séparées par des virgules des serveurs WINS utilisés dans les recherches WINS.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe WINSType MicrosoftDNS**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





