---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitations de Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc283704ea96e3303de6755a217e454b506bdc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523766"
---
# <a name="schema-imposed-limitations"></a>Limitations de Schema-Imposed

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Le schéma PrintCapabilities fournit aux auteurs PrintCapabilities un degré élevé de flexibilité et d’expressivité qui peuvent être utilisés dans les descriptions des appareils. Toutefois, les dépendances de configuration imposent une limitation à cette flexibilité et à l’expressivité. Les instances ParameterDef, la liste des éléments de fonctionnalité, la liste des instances d’option dans chaque fonctionnalité et les instances ScoredProperty dans chaque option ne doivent pas contenir de dépendances de configuration. Le fournisseur de documents PrintCapabilities doit détecter les combinaisons de configurations non valides et doit les résoudre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



