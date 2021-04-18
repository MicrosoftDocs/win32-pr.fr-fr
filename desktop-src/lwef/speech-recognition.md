---
title: Reconnaissance vocale
description: Reconnaissance vocale
ms.assetid: cb5ac509-12a4-4ca4-8776-424568cf780d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d5c037ced96c386a5e0baf18eeba258422e0193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512693"
---
# <a name="speech-recognition"></a>Reconnaissance vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La reconnaissance vocale offre une interface très naturelle et familière pour l’interaction avec les caractères. Toutefois, l’entrée vocale présente également de nombreux défis. Les moteurs de reconnaissance vocale fonctionnent actuellement sans parties substantielles du répertoire des communications vocales humaines, telles que les gestes, les intonation et les expressions faciales. En outre, la parole naturelle est généralement illimitée. Il est facile pour l’orateur de dépasser le vocabulaire actuel ou la *grammaire* du moteur. De même, la formulation ou l’ordre des mots peut varier pour une requête ou une réponse donnée. En outre, les moteurs de reconnaissance vocale doivent souvent gérer des variations importantes dans l’environnement de l’orateur. Par exemple, le bruit de fond, la qualité du microphone et l’emplacement peuvent affecter la qualité d’entrée. De même, des prononciations de haut-parleur ou même des variations de haut-parleur, comme lorsque l’orateur a un froid, compliquent la conversion des données acoustiques en présentation de la présentation. Enfin, les moteurs de reconnaissance vocale doivent également gérer des mots ou expressions similaires dans une langue, par exemple « nouveau », « savait », « GNU » ou « Wreck a Nice Beach » et « reconnaître la parole ».

La reconnaissance vocale n’est pas toujours la meilleure forme d’entrée pour une tâche. En raison de la nature de la reconnaissance vocale, elle peut souvent être plus lente que les autres formes d’entrée. Comme le clavier, l’entrée vocale est une interface médiocre pour le pointage, sauf si un type de représentation mnémonique est fourni. Par conséquent, déterminez toujours si la parole est l’entrée la plus appropriée pour une tâche. Il est préférable d’éviter d’utiliser la parole comme interface exclusive pour n’importe quelle tâche. Fournissez d’autres façons d’accéder à toutes les fonctionnalités de base à l’aide de méthodes telles que la souris ou le clavier. En outre, tirez parti de la nature multimodale de l’utilisation de la reconnaissance vocale dans l’interface visuelle en combinant les entrées vocales avec des informations visuelles qui permettent de spécifier le contexte et les options.

Enfin, l’utilisation réussie de l’entrée vocale est due uniquement en partie à la qualité de la technologie. Même la reconnaissance humaine, qui dépasse toute technologie de reconnaissance en cours, peut parfois échouer. Toutefois, dans la communication humaine, nous utilisons des stratégies qui améliorent la probabilité de réussite et qui fournissent une récupération d’erreur en cas de problème. Par conséquent, l’efficacité de l’entrée vocale dépend également de la qualité de l’interface utilisateur qui la présente.

L’étude des modèles humains d’interaction vocale peut être utile lors de la conception d’interfaces vocales plus naturelles. L’enregistrement de boîtes de dialogue vocales réelles pour des scénarios particuliers peut vous aider à mieux comprendre les constructions et les modèles utilisés, ainsi que des formes efficaces de commentaires et de récupération d’erreur. Il peut aider à déterminer le vocabulaire approprié à utiliser (pour l’entrée et la sortie). Il est préférable de concevoir une interface vocale basée sur la façon dont les gens parlent vraiment de les dériver de l’interface graphique dans laquelle elles fonctionnent.

Notez que Microsoft Agent utilise l’API Microsoft Speech (SAPI) pour prendre en charge la reconnaissance vocale. Cela permet d’utiliser Microsoft Agent avec un large éventail de moteurs compatibles. Bien que Microsoft Agent spécifie certaines interfaces de base, les exigences en matière de performances et la qualité d’un moteur peuvent varier.

La reconnaissance vocale n’est pas le seul moyen de prendre en charge les interfaces de conversation. Vous pouvez également utiliser le traitement en langage naturel de l’entrée au clavier à la place de ou en plus de la reconnaissance vocale. Dans ces situations, vous pouvez toujours appliquer des recommandations pour l’entrée vocale.

-   [Écoutez, ne reconnaissez pas](listen--dont-just-recognize.md)
-   [Clarifier et limiter les choix](clarify-and-limit-choices.md)
-   [Fournir une bonne récupération d’erreur](provide-good-error-recovery.md)

 

 




