---
title: Classe MicrosoftDNS_DomainResourceRecordContainment
description: La \_ classe DomainResourceRecordContainment MicrosoftDNS est utilisée pour la relation contenant-contenu des RR ; chaque instance du \_ domaine MicrosoftDNS peut contenir plusieurs instances de la \_ classe ResourceRecord MicrosoftDNS.
ms.assetid: 556c5e8d-58a1-4cb4-b4e9-eebdd86ed6a0
keywords:
- MicrosoftDNS_DomainResourceRecordContainment de la classe DNS
- MicrosoftDNS_DomainResourceRecordContainment de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainResourceRecordContainment
- MicrosoftDNS_DomainResourceRecordContainment.GroupComponent
- MicrosoftDNS_DomainResourceRecordContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddf172c3e320fd5c3a3b04d85d766a0252abd97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465334"
---
# <a name="microsoftdns_domainresourcerecordcontainment-class"></a>MicrosoftDNS \_ DomainResourceRecordContainment, classe

La **classe \_ DomainResourceRecordContainment MicrosoftDNS** est utilisée pour la relation contenant-contenu des RR ; chaque instance du [**\_ domaine MicrosoftDNS**](microsoftdns-domain.md) peut contenir plusieurs instances de la classe [**\_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) . Chaque instance de la **classe \_ ResourceRecord MicrosoftDNS** appartient à une instance unique de la classe de **\_ domaine MicrosoftDNS** et est définie comme étant faible à cette instance.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_DomainResourceRecordContainment : CIM_Component
{
  MicrosoftDNS_Domain         REF GroupComponent;
  MicrosoftDNS_ResourceRecord REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ DomainResourceRecordContainment** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ DomainResourceRecordContainment** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ domaine MicrosoftDNS**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Qualificateurs : clé, substitution ("GroupComponent")

Description : zone, cache, RootHints ou domaine directement contenant l’enregistrement de ressource.

Hérité du \_ composant CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données : **MicrosoftDNS \_ ResourceRecord**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Qualificateurs : clé, remplacement ("PartComponent")

Description : l’enregistrement de ressource contenu dans un domaine, une zone, un cache ou un RootHints.

Hérité du \_ composant CIM.

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

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ DomainDomainContainment**](microsoftdns-domaindomaincontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





