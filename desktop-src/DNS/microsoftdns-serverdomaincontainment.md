---
title: Classe MicrosoftDNS_ServerDomainContainment
description: Chaque instance de la \_ classe WMI de l’Association de serveurs MicrosoftDNS peut contenir plusieurs instances de la classe de domaine MicrosoftDNS \_ .
ms.assetid: a16a11fb-65fc-4f12-903c-b3a61f6a4720
keywords:
- MicrosoftDNS_ServerDomainContainment de la classe DNS
- MicrosoftDNS_ServerDomainContainment de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_ServerDomainContainment
- MicrosoftDNS_ServerDomainContainment.GroupComponent
- MicrosoftDNS_ServerDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc747cae72ac4733ad9bec7288858731b6250312d43476a000d2f99a989267d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527249"
---
# <a name="microsoftdns_serverdomaincontainment-class"></a>MicrosoftDNS \_ ServerDomainContainment, classe

Chaque instance de la classe WMI de l’Association de [**\_ serveurs MicrosoftDNS**](microsoftdns-server.md) peut contenir plusieurs instances de la classe de [**\_ domaine MicrosoftDNS**](microsoftdns-domain.md) . Chaque instance de la classe de **\_ domaine MicrosoftDNS** appartient à une instance unique de la classe de **\_ serveur MicrosoftDNS** et est définie comme étant faible à ce serveur.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_ServerDomainContainment : CIM_Component
{
  MicrosoftDNS_Server REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ ServerDomainContainment** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ ServerDomainContainment** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ serveur MicrosoftDNS**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Qualificateurs : clé, remplacement ("GroupComponent"), min (1), Max (1)

Description : serveur DNS.

Hérité du **\_ composant CIM**.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ domaine MicrosoftDNS**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Qualificateurs : clé, remplacement ("PartComponent")

Description : domaine, zone, cache ou RootHints géré par le serveur DNS.

Hérité du **\_ composant CIM**.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **MicrosoftDNS \_ ServerDomainContainment** est dérivée de la classe de **\_ composant CIM** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





