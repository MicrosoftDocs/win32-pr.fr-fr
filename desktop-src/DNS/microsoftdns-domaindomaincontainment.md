---
title: Classe MicrosoftDNS_DomainDomainContainment
description: La \_ classe DomainDomainContainment MicrosoftDNS est utilisée pour la relation contenant-contenu d’un domaine ; Les domaines DNS peuvent contenir d’autres domaines DNS.
ms.assetid: 43faa046-30bf-4fb3-9698-98d09c424fad
keywords:
- MicrosoftDNS_DomainDomainContainment de la classe DNS
- MicrosoftDNS_DomainDomainContainment de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_DomainDomainContainment
- MicrosoftDNS_DomainDomainContainment.GroupComponent
- MicrosoftDNS_DomainDomainContainment.PartComponent
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55c5b67ee8026055bc2fa8098cb33e8c767528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033105"
---
# <a name="microsoftdns_domaindomaincontainment-class"></a>MicrosoftDNS \_ DomainDomainContainment, classe

La **classe \_ DomainDomainContainment MicrosoftDNS** est utilisée pour la relation contenant-contenu d’un domaine ; Les domaines DNS peuvent contenir d’autres domaines DNS. Chaque instance de la classe de [**\_ domaine MicrosoftDNS**](microsoftdns-domain.md) peut contenir plusieurs autres instances **du \_ domaine MicrosoftDNS**. Une instance d’un objet de **\_ domaine MicrosoftDNS** est directement contenue dans un seul **\_ domaine MicrosoftDNS** de niveau supérieur.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_DomainDomainContainment : CIM_Component
{
  MicrosoftDNS_Domain REF GroupComponent;
  MicrosoftDNS_Domain REF PartComponent;
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ DomainDomainContainment** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MicrosoftDNS \_ DomainDomainContainment** a ces propriétés.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ domaine MicrosoftDNS**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Qualificateurs : clé, Max (1), override ("GroupComponent")

Description : domaine, zone, cache ou RootHints de niveau supérieur.

Hérité du \_ composant CIM

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ domaine MicrosoftDNS**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Qualificateurs : clé, remplacement ("PartComponent")

Description : domaine contenu par un domaine de niveau supérieur, zone, cache ou RootHints.

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

[**MicrosoftDNS \_ DomainResourceRecordContainment**](microsoftdns-domainresourcerecordcontainment.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**MicrosoftDNS \_ ServerDomainContainment**](microsoftdns-serverdomaincontainment.md)
</dt> </dl>

 

 





