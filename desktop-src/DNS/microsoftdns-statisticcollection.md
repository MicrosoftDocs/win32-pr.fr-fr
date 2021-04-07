---
title: MicrosoftDNS_StatisticCollection
description: La \_ classe MicrosoftDNS StatisticCollection représente une collection de statistiques de serveur DNS associées.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f9c65714fb3b1db58b5a6439ade5531792501
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028967"
---
# <a name="microsoftdns_statisticcollection"></a>MicrosoftDNS \_ StatisticCollection

La \_ classe MicrosoftDNS StatisticCollection représente une collection de statistiques de serveur DNS associées.

La syntaxe suivante est simplifiée à partir du code MOF.

``` syntax
class MicrosoftDNS_StatisticCollection : CIM_LogicalElement
{
  string Name;
  uint32 StatId;
  MicrosoftDNS_Statistic Statistics[];
};
```

## <a name="properties"></a>Propriétés

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**
</dt> <dd>

Nom de la collection de statistiques.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**StatId**
</dt> <dd>

Représentation numérique de la collection de statistiques.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**\_Statistiques statistiques MicrosoftDNS\[\]**
</dt> <dd>

Tableau de valeurs associées à la statistique.

</dd> </dl>

## <a name="methods"></a>Méthodes

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Cette classe n’a pas de méthode.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_Statistiques MicrosoftDNS**](microsoftdns-statistic.md)
</dt> </dl>

 

 




