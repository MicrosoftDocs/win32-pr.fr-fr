---
description: La routine de rappel de file d’attente par défaut peut être spécifiée pour gérer les notifications envoyées par SetupCommitFileQueue, ou elle peut être appelée par une routine de rappel personnalisée qui repose sur les fonctionnalités de la routine de rappel de file d’attente par défaut.
ms.assetid: df8ae7b5-f3a2-4343-a603-440ab5c02b88
title: Utilisation de la routine de rappel de file d’attente par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51bceadf309257b9faf2b3ce3b8a12771572664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538887"
---
# <a name="using-the-default-queue-callback-routine"></a>Utilisation de la routine de rappel de file d’attente par défaut

La routine de rappel de file d’attente par défaut peut être spécifiée pour gérer les notifications envoyées par [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), ou elle peut être appelée par une routine de rappel personnalisée qui repose sur les fonctionnalités de la routine de rappel de file d’attente par défaut.

Les sections suivantes expliquent comment initialiser et terminer le contexte utilisé par une routine de rappel de file d’attente par défaut. Les sections décrivent également comment utiliser la routine de rappel de file d’attente par défaut avec [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) ou une routine de rappel personnalisée.

-   [Initialisation et fin du contexte de rappel](initializing-and-terminating-the-callback-context.md)
-   [Appel de la routine de rappel de file d’attente par défaut](calling-the-default-queue-callback-routine.md)

 

 



