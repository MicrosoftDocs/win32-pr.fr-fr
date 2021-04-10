---
title: Classe MicrosoftDNS_RootHints
description: La \_ classe MicrosoftDNS RootHints décrit les RootHints stockés dans un fichier cache sur un serveur DNS. Cette classe simplifie la visualisation de la relation contenant-contenu des objets DNS, plutôt que la représentation d’un objet réel.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints de la classe DNS
- MicrosoftDNS_RootHints de la classe DNS, Description
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104158"
---
# <a name="microsoftdns_roothints-class"></a>MicrosoftDNS \_ RootHints, classe

La classe **MicrosoftDNS \_ RootHints** décrit les RootHints stockés dans un fichier cache sur un serveur DNS. Cette classe simplifie la visualisation de la relation contenant-contenu des objets DNS, plutôt que la représentation d’un objet réel.

**MicrosoftDNS \_ RootHints** est un conteneur pour les enregistrements de ressources stockés par le serveur DNS dans un fichier cache. Chaque instance de la **classe \_ RootHints MicrosoftDNS** doit être affectée à un seul serveur DNS. Il peut être associé à plusieurs instances de la [**classe \_ ResourceRecord MicrosoftDNS**](microsoftdns-resourcerecord.md) .

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Membres

La classe **MicrosoftDNS \_ RootHints** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

La classe **MicrosoftDNS \_ RootHints** possède ces méthodes.



| Méthode                        | Description                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **GetDistinguishedName**      | Récupère le nom unique de la zone. <br/> Qualificateurs : implémentés<br/>   |
| **WriteBackRootHintDatafile** | Réécrit le RootHints dans le fichier cache DNS. <br/> Qualificateurs : implémentés<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Espace de noms<br/>                | \\MicrosoftDNS racine<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Domaine MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Méthode WriteBackRootHintDatafile de la \_ classe MicrosoftDNS RootHints**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Méthode GetDistinguishedName de la \_ classe MicrosoftDNS RootHints**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





