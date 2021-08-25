---
title: Méthode CreateInstanceFromPropertyData de la classe MicrosoftDNS_NXTType
description: La méthode CreateInstanceFromPropertyData instancie un enregistrement de ressource suivant (NXT).
ms.assetid: d0e4f3bf-f835-4341-a614-539975e6be11
keywords:
- Méthode CreateInstanceFromPropertyData DNS
- Méthode CreateInstanceFromPropertyData DNS, classe MicrosoftDNS_NXTType
- MicrosoftDNS_NXTType de la classe DNS, méthode CreateInstanceFromPropertyData
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1075574ec2e2fecceacc24701f67105ac9796a41a45e20c468a9021d7ff20899
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815669"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_nxttype-class"></a>Méthode CreateInstanceFromPropertyData de la \_ classe MicrosoftDNS NXTType

La méthode **CreateInstanceFromPropertyData** instancie un enregistrement de ressource suivant (NXT).

## <a name="syntax"></a>Syntaxe


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
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



| Value                                                                                                | Signification                  |
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

*NextDomainName* \[ dans\]
</dt> <dd>

Nom de domaine suivant.

</dd> <dt>

*Types* \[ dans\]
</dt> <dd>

Liste séparée par des espaces des mnémoniques de type RR pour le nom de propriétaire de l’enregistrement de ressource NXT.

</dd> <dt>

*RR* \[ out, Ref\]
</dt> <dd>

Référence au nouvel objet.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)
</dt> <dt>

[**Modifier la méthode de la \_ classe NXTType MicrosoftDNS**](microsoftdns-nxttype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





