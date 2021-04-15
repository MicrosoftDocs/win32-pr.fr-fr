---
description: Fonctions de débogage des sections critiques
ms.assetid: 2e58ff06-d9b2-45fe-bd40-d637aa434339
title: Fonctions de débogage des sections critiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098558a97e38168595dc89c3c81175c9d6635c5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520991"
---
# <a name="critical-section-debugging-functions"></a><span data-ttu-id="121e7-103">Fonctions de débogage des sections critiques</span><span class="sxs-lookup"><span data-stu-id="121e7-103">Critical Section Debugging Functions</span></span>

<span data-ttu-id="121e7-104">Ces fonctions permettent de déboguer des sections critiques dans votre code, ce qui peut faciliter la recherche de la cause d’un blocage.</span><span class="sxs-lookup"><span data-stu-id="121e7-104">These functions help to debug critical sections in your code, which can make it easier to find the cause of a deadlock.</span></span> <span data-ttu-id="121e7-105">Ces fonctions utilisent la classe d’assistance [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="121e7-105">These functions use the [**CCritSec**](ccritsec.md) helper class.</span></span>



| <span data-ttu-id="121e7-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="121e7-106">Function</span></span>                             | <span data-ttu-id="121e7-107">Description</span><span class="sxs-lookup"><span data-stu-id="121e7-107">Description</span></span>                                                                  |
|--------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="121e7-108">**CritCheckIn**</span><span class="sxs-lookup"><span data-stu-id="121e7-108">**CritCheckIn**</span></span>](critcheckin.md)   | <span data-ttu-id="121e7-109">Retourne la **valeur true** si le thread actuel possède la section critique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="121e7-109">Returns **TRUE** if the current thread owns the specified critical section.</span></span>  |
| [<span data-ttu-id="121e7-110">**CritCheckOut**</span><span class="sxs-lookup"><span data-stu-id="121e7-110">**CritCheckOut**</span></span>](critcheckout.md) | <span data-ttu-id="121e7-111">Retourne la **valeur false** si le thread actuel possède la section critique spécifiée.</span><span class="sxs-lookup"><span data-stu-id="121e7-111">Returns **FALSE** if the current thread owns the specified critical section.</span></span> |
| [<span data-ttu-id="121e7-112">**DbgLockTrace**</span><span class="sxs-lookup"><span data-stu-id="121e7-112">**DbgLockTrace**</span></span>](dbglocktrace.md) | <span data-ttu-id="121e7-113">Active ou désactive la journalisation du débogage pour une section critique donnée.</span><span class="sxs-lookup"><span data-stu-id="121e7-113">Enables or disables debug logging for a given critical section.</span></span>              |



 

## <a name="related-topics"></a><span data-ttu-id="121e7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="121e7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="121e7-115">Utilitaires de débogage</span><span class="sxs-lookup"><span data-stu-id="121e7-115">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



