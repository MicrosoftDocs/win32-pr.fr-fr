---
title: MicrosoftDNS_StatisticCollection
description: La \_ classe MicrosoftDNS StatisticCollection représente une collection de statistiques de serveur DNS associées.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fda276433290ab2b151b4b6a34abae7a0113ee3db75054f6c66c0536009dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109089"
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

 

 




