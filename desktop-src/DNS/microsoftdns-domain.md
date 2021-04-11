---
title: Classe MicrosoftDNS_Domain
description: La \_ classe de domaine MicrosoftDNS représente un domaine dans une hiérarchie DNS.
ms.assetid: 4b3124d6-aa5c-4950-b461-c6dd7bc96945
keywords:
- MicrosoftDNS_Domain de la classe DNS
- MicrosoftDNS_Domain de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_Domain
- MicrosoftDNS_Domain.GetDistinguishedName
- MicrosoftDNS_Domain.DnsServerName
- MicrosoftDNS_Domain.ContainerName
- MicrosoftDNS_Domain.Name
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 108badc046e22f27d9bb02abd0d8f26314da456c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103708"
---
# <a name="microsoftdns_domain-class"></a>\_Classe de domaine MicrosoftDNS

La classe de **\_ domaine MicrosoftDNS** représente un domaine dans une hiérarchie DNS.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_Domain : CIM_LogicalElement
{
  string DnsServerName;
  string ContainerName;
  string Name;
};
```

## <a name="members"></a>Membres

La classe de **\_ domaine MicrosoftDNS** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe de **\_ domaine MicrosoftDNS** possède ces méthodes.



| Méthode                   | Description                                                                                |
|:-------------------------|:-------------------------------------------------------------------------------------------|
| **GetDistinguishedName** | Obtient le nom unique du service d’annuaire pour la zone. <br/> Qualificateurs : implémentés<br/> |



 

### <a name="properties"></a>Propriétés

La classe de **\_ domaine MicrosoftDNS** possède ces propriétés.

<dl> <dt>

**ContainerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom du conteneur du domaine, qui peut être une zone, un cache ou une RootHints.

Dans les cas où le conteneur est une zone (une instance de la classe de [**\_ zone MicrosoftDNS**](microsoftdns-zone.md) ), cette propriété contient le nom de domaine complet de la zone.

Lorsque le conteneur est la zone racine, la chaîne \\ \\ doit être utilisée.

Dans les cas où le conteneur est le cache DNS des enregistrements de ressource (une instance de la classe de [**\_ cache MicrosoftDNS**](microsoftdns-cache.md) ), cette propriété est définie sur la chaîne \\ . Cache \\ .

Si le conteneur est RootHints (une instance de la classe [**MicrosoftDNS \_ RootHints**](microsoftdns-roothints.md) ), cette propriété doit avoir la valeur \\ .. RootHints \\ .

</dd> <dt>

**DnsServerName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet ou adresse IP du serveur DNS qui contient le domaine.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom de domaine complet du domaine.

Pour les instances de cache DNS ou RootHints, les chaînes \\ .. Cache \\ et \\ .. RootHints \\ doit être utilisé, respectivement.

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

[**Méthode GetDistinguishedName de la \_ classe de domaine MicrosoftDNS**](microsoftdns-domain-getdistinguishedname.md)
</dt> </dl>

 

 





