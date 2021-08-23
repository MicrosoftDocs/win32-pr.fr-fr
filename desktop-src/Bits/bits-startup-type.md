---
title: Type de démarrage BITS
description: Le type de démarrage pour BITS est retardé automatiquement. avant Windows Vista, le Type de démarrage pour BITS est manuel. Quand une tâche BITS est créée, le type de démarrage passe à automatique. Le type de démarrage revient à manuel lorsque toutes les tâches sont terminées ou annulées.
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: defafff5b3dd0a9b03e18b61b84fa6c32022035ce58913599151ee526fd52d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579429"
---
# <a name="bits-startup-type"></a>Type de démarrage BITS

Le **type de démarrage** pour bits est le démarrage automatique différé (s’il y a des travaux en bits actifs) ou le démarrage à la demande (s’il n’y a pas de travaux actifs). les Versions de Windows antérieures à la mise à jour de novembre utilisaient uniquement le type de démarrage à démarrage automatique retardé ; les versions antérieures à Vista utilisaient le type de démarrage manuel.

Vous ne devez pas définir le **type de démarrage** sur désactivé. La désactivation du service BITS peut perturber les applications qui reposent sur BITS pour transférer des fichiers.

 

 




