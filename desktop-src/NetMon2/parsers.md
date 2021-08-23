---
description: Un analyseur est le composant Moniteur réseau qui inspecte les données dans une capture différée et transmet des informations de protocole spécifiques à l’application qui appelle l’analyseur. Un analyseur est passif, car il fonctionne uniquement quand Moniteur réseau ou un expert l’appelle.
ms.assetid: 6c135a24-5718-429a-988b-a2abd6b563d1
title: Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf6f7c799782a75905d366c56157a99fd6f774f5682e302dcec4a9d6c788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555512"
---
# <a name="parser"></a>Parser

Un analyseur est le composant Moniteur réseau qui inspecte les données dans une [*capture différée*](d.md)et transmet des informations de protocole spécifiques à l’application qui appelle l’analyseur. Un analyseur est passif, car il fonctionne uniquement quand Moniteur réseau ou un [*expert*](e.md) l’appelle.

Chaque analyseur identifie un protocole, et en général, un analyseur est implémenté dans sa propre DLL d’analyseur. Toutefois, une DLL d’analyseur peut contenir plusieurs analyseurs, ce qui signifie qu’une DLL peut être utilisée pour détecter plusieurs protocoles.

Les données transmises à un analyseur sont extraites d’une [*capture différée*](d.md)et transmises à l’analyseur image par image. Vous ne pouvez pas analyser une capture en temps réel.

Pour analyser les données dans un frame, l’analyseur doit reconnaître l’instance de protocole, identifier les propriétés qui existent dans l’instance de protocole et attacher une définition de propriété à chaque propriété. N’oubliez pas que le frame contient uniquement un flux de données. Le frame ne contient pas de données indiquant les protocoles ou les propriétés de protocole que les données représentent.

L’illustration suivante montre un frame qui contient une instance d’un protocole.

![Frame qui contient une instance de protocole](images/parser1.png)

Si Moniteur réseau affiche des données analysées dans l’interface utilisateur, l’analyseur doit mettre en forme les données. Toutefois, certains experts utilisent la sortie de l’analyseur par programme et n’affichent pas la sortie dans l’interface utilisateur Moniteur réseau. Les données affichées incluent à la fois les données définies par l’analyseur et les données de la capture. Par exemple, l’analyseur fournit en général à la fois un nom pour une propriété qui est affichée et les données de la capture qui est associée à la propriété.



| Pour obtenir des informations sur                                         | Consultez                                                                    |
|---------------------------------------------------------------|------------------------------------------------------------------------|
| Les points d’entrée doivent être implémentés dans la DLL de l’analyseur. | [Architecture des DLL de l’analyseur](parser-dll-architecture.md)                 |
| Comment implémenter les fonctions d’exportation de DLL de l’analyseur.                 | [Écriture d’un analyseur de protocole](writing-a-protocol-parser.md)             |
| Les fonctions et les analyseurs de structures qui utilisent.                   | [Structures et fonctions de l’analyseur](parser-functions-and-structures.md) |



 

 

 



