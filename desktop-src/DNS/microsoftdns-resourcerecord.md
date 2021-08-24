---
title: Classe MicrosoftDNS_ResourceRecord
description: La \_ classe MicrosoftDNS ResourceRecord représente les propriétés générales d’un RR DNS. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 84d6d106-fcc9-44ae-8db2-181c60489aec
keywords:
- MicrosoftDNS_ResourceRecord de la classe DNS
- MicrosoftDNS_ResourceRecord de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
- MicrosoftDNS_ResourceRecord.DnsServerName
- MicrosoftDNS_ResourceRecord.ContainerName
- MicrosoftDNS_ResourceRecord.DomainName
- MicrosoftDNS_ResourceRecord.OwnerName
- MicrosoftDNS_ResourceRecord.RecordClass 1
- MicrosoftDNS_ResourceRecord.TTL
- MicrosoftDNS_ResourceRecord.TimeStamp
- MicrosoftDNS_ResourceRecord.RecordData
- MicrosoftDNS_ResourceRecord.TextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b54d23ae522291a2a38ad5d3f046fc444efdefd4d270519fbc3a2ee5739ba47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874799"
---
# <a name="microsoftdns_resourcerecord-class"></a>MicrosoftDNS \_ ResourceRecord, classe

La classe **MicrosoftDNS \_ ResourceRecord** représente les propriétés générales d’un RR DNS.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_ResourceRecord : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string DomainName;
  string OwnerName;
  uint16 RecordClass=1;
  uint32 TTL;
  uint32 TimeStamp;
  string RecordData;
  string TextRepresentation;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ ResourceRecord** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ ResourceRecord** possède ces méthodes.



| Méthode                                   | Description                                                                                                                                                                                                                                                            |
|:-----------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromTextRepresentation** | Analyse le RR dans la chaîne TextRepresentation, et avec les noms de conteneur et de serveur DNS d’entrée, définit et instancie un objet ResourceRecord. La méthode retourne une référence au nouvel objet sous la forme d’un paramètre de sortie. <br/> Qualificateurs : aucun<br/> |
| **GetObjectByTextRepresentation**        | Récupère une instance existante de la sous- \_ classe ResourceRecord MicrosoftDns, représentée par la chaîne TextRepresentation, ainsi que le nom du conteneur et du serveur DNS. <br/> Qualificateurs : aucun<br/>                                                        |



 

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ ResourceRecord** a ces propriétés.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le nom du conteneur de la zone, du cache ou de l’instance RootHints qui contient le RR.

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le nom de domaine complet ou l’adresse IP du serveur DNS qui contient le RR.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Représente le nom de domaine complet du domaine qui contient le RR. Cette propriété peut contenir les chaînes \\ .. Cache \\ ou \\ .. RootHints \\ si le cache interne ou RootHints contient le RR, respectivement.

</dd> <dt>

**OwnerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du propriétaire de l’enregistrement de ressource.

</dd> <dt>

**RecordClass = 1**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

* * Windows Server 2003 : * *

Cette chaîne représente la classe de l’enregistrement de ressource. Les valeurs valides sont les suivantes :

1 : dans (Internet)

2 : CS (CSNET)

3 : CH (CHAOS)

4 : HS (Hesiod)

</dd> <dt>

**RecordData**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Données d’enregistrement de ressource.

</dd> <dt>

**TextRepresentation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Représentation textuelle de l’ensemble du RR.

</dd> <dt>

**Confirmé**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Heure de la dernière actualisation de l’enregistrement de ressource, exprimée en heures écoulées depuis le 1er janvier 1601, heure de Greenwich (GMT).

</dd> <dt>

**TTL**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Durée, en secondes, pendant laquelle l’enregistrement de ressource peut être mis en cache par un programme de [*résolution*](r-gly.md)DNS.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode CreateInstanceFromTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> <dt>

[**Méthode GetObjectByTextRepresentation de la \_ classe MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





