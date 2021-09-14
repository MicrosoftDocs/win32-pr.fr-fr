---
description: En savoir plus sur les limitations imposées par le schéma PrintCapabilities. Le fournisseur PrintCapabilities doit détecter les configurations non valides et les résoudre.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitations de Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191860"
---
# <a name="schema-imposed-limitations"></a>Limitations de Schema-Imposed

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le schéma PrintCapabilities fournit aux auteurs PrintCapabilities un degré élevé de flexibilité et d’expressivité qui peuvent être utilisés dans les descriptions des appareils. Toutefois, les dépendances de configuration imposent une limitation à cette flexibilité et à l’expressivité. Les instances ParameterDef, la liste des éléments de fonctionnalité, la liste des instances d’option dans chaque fonctionnalité et les instances ScoredProperty dans chaque option ne doivent pas contenir de dépendances de configuration. Le fournisseur de documents PrintCapabilities doit détecter les combinaisons de configurations non valides et doit les résoudre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



