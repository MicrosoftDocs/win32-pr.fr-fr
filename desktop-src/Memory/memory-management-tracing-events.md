---
description: 'En savoir plus sur : événements de suivi de gestion de la mémoire'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Événements de suivi de gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb395082d46ddd668cbb91ee396f211a4055472f49682ab75efc90cedca7ad5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809006"
---
# <a name="memory-management-tracing-events"></a>Événements de suivi de gestion de la mémoire

Cette section fournit des informations détaillées sur les détails des événements de suivi de gestion de la mémoire spécifiques.

Le suivi de la gestion de la mémoire est une fonctionnalité de résolution des problèmes qui peut être activée dans les binaires de la version commerciale pour suivre certains événements de gestion de la mémoire avec une charge minimale. Cette fonctionnalité permet de meilleures fonctionnalités de diagnostic pour les développeurs et le support technique. Le suivi des événements de gestion de la mémoire prend en charge le suivi de l’allocation des tas, la réallocation et les opérations gratuites.

le suivi d’événements de gestion de la mémoire utilise Suivi d’v nements pour Windows (ETW), une fonctionnalité de traçage à usage général et à haut débit fournie par le système d’exploitation. ETW fournit un mécanisme de suivi pour les événements déclenchés par les applications en mode utilisateur et les pilotes de périphérique en mode noyau. ETW permet d’activer et de désactiver la journalisation dynamique, ce qui facilite l’exécution du suivi détaillé dans les environnements de production sans nécessiter de redémarrage ou de redémarrage de l’application. le suivi d’événements de gestion de la mémoire à l’aide d’ETW est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures. Pour obtenir des informations générales sur ETW, consultez [améliorer le débogage et le réglage des performances avec ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

La liste suivante fournit des informations détaillées pour chaque événement de suivi de gestion de la mémoire. Pour plus d’informations sur les événements, cliquez sur le nom de l’événement.



| Nom de l'événement                                                  | Description                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_allocation d' \_ événement du tas ETW \_**](etw-heap-event-alloc.md)     | Événement de suivi de gestion de la mémoire pour une opération d’allocation de tas.    |
| [**\_événement de tas ETW \_ \_ gratuit**](etw-heap-event-free.md)       | Événement de suivi de gestion de la mémoire pour une opération libre de segment de mémoire.          |
| [**réallocation d' \_ événements de tas ETW \_ \_**](etw-heap-event-realloc.md) | Événement de suivi de gestion de la mémoire pour une opération de réallocation de tas. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Améliorer le débogage et le réglage des performances à l'aide du suivi ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
