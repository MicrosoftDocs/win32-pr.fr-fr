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
# <a name="using-the-default-queue-callback-routine"></a><span data-ttu-id="8c246-103">Utilisation de la routine de rappel de file d’attente par défaut</span><span class="sxs-lookup"><span data-stu-id="8c246-103">Using the Default Queue Callback Routine</span></span>

<span data-ttu-id="8c246-104">La routine de rappel de file d’attente par défaut peut être spécifiée pour gérer les notifications envoyées par [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), ou elle peut être appelée par une routine de rappel personnalisée qui repose sur les fonctionnalités de la routine de rappel de file d’attente par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c246-104">The default queue callback routine can be specified to handle notifications sent by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), or it can be called by a custom callback routine that builds on the functionality of the default queue callback routine.</span></span>

<span data-ttu-id="8c246-105">Les sections suivantes expliquent comment initialiser et terminer le contexte utilisé par une routine de rappel de file d’attente par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c246-105">The following sections explain how to initialize and terminate the context used by a default queue callback routine.</span></span> <span data-ttu-id="8c246-106">Les sections décrivent également comment utiliser la routine de rappel de file d’attente par défaut avec [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) ou une routine de rappel personnalisée.</span><span class="sxs-lookup"><span data-stu-id="8c246-106">The sections also describe how to use the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) or a custom callback routine.</span></span>

-   [<span data-ttu-id="8c246-107">Initialisation et fin du contexte de rappel</span><span class="sxs-lookup"><span data-stu-id="8c246-107">Initializing and Terminating the Callback Context</span></span>](initializing-and-terminating-the-callback-context.md)
-   [<span data-ttu-id="8c246-108">Appel de la routine de rappel de file d’attente par défaut</span><span class="sxs-lookup"><span data-stu-id="8c246-108">Calling the Default Queue Callback Routine</span></span>](calling-the-default-queue-callback-routine.md)

 

 



