---
description: Fonctions de débogage d’attente
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Fonctions de débogage d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529720"
---
# <a name="wait-debugging-functions"></a><span data-ttu-id="86a92-103">Fonctions de débogage d’attente</span><span class="sxs-lookup"><span data-stu-id="86a92-103">Wait Debugging Functions</span></span>

<span data-ttu-id="86a92-104">Microsoft DirectShow fournit plusieurs fonctions pour déboguer des attentes infinies.</span><span class="sxs-lookup"><span data-stu-id="86a92-104">Microsoft DirectShow provides several functions for debugging infinite waits.</span></span>

<span data-ttu-id="86a92-105">Dans les versions commerciales, les fonctions [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) et [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) fonctionnent comme leurs équivalents d’API Windows, **WaitForMultipleObjects** et **WaitForSingleObject**, avec des intervalles de délai d’attente infinis.</span><span class="sxs-lookup"><span data-stu-id="86a92-105">In retail builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions work like their Windows API counterparts, **WaitForMultipleObjects** and **WaitForSingleObject**, with infinite time-out intervals.</span></span>

<span data-ttu-id="86a92-106">Dans les versions Debug, ces fonctions utilisent une valeur de délai d’attente globale.</span><span class="sxs-lookup"><span data-stu-id="86a92-106">In debug builds, these functions use a global time-out value.</span></span> <span data-ttu-id="86a92-107">Si le délai d’attente expire, la fonction déclenche une assertion.</span><span class="sxs-lookup"><span data-stu-id="86a92-107">If the time-out expires, the function triggers an assert.</span></span> <span data-ttu-id="86a92-108">La clé de Registre suivante spécifie la valeur du délai d’attente, en millisecondes :</span><span class="sxs-lookup"><span data-stu-id="86a92-108">The following registry key specifies the time-out value, in milliseconds:</span></span>

<span data-ttu-id="86a92-109">**% \_ \_ \\ <DebugRoot> \\ <Module Name> \\ d’expiration de l’ordinateur local**</span><span class="sxs-lookup"><span data-stu-id="86a92-109">**HKEY\_LOCAL\_MACHINE\\<DebugRoot>\\<Module Name>\\TIMEOUT**</span></span>

<span data-ttu-id="86a92-110">où *<DebugRoot>* est le chemin d’accès au registre décrit dans la rubrique [fonctions de sortie de débogage](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="86a92-110">where *<DebugRoot>* is the registry path described in the topic [Debug Output Functions](debug-output-functions.md).</span></span>

<span data-ttu-id="86a92-111">Si la clé n’existe pas, la valeur du délai d’attente est définie par défaut sur Infinite.</span><span class="sxs-lookup"><span data-stu-id="86a92-111">If the key does not exist, the time-out value defaults to INFINITE.</span></span> <span data-ttu-id="86a92-112">Vous pouvez utiliser la fonction [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) pour remplacer l’entrée de registre.</span><span class="sxs-lookup"><span data-stu-id="86a92-112">You can use the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function to override the registry entry.</span></span>



| <span data-ttu-id="86a92-113">Fonction</span><span class="sxs-lookup"><span data-stu-id="86a92-113">Function</span></span>                                                       | <span data-ttu-id="86a92-114">Description</span><span class="sxs-lookup"><span data-stu-id="86a92-114">Description</span></span>                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="86a92-115">**DbgSetWaitTimeout**</span><span class="sxs-lookup"><span data-stu-id="86a92-115">**DbgSetWaitTimeout**</span></span>](dbgsetwaittimeout.md)                 | <span data-ttu-id="86a92-116">Définit la valeur du délai d’attente du débogage.</span><span class="sxs-lookup"><span data-stu-id="86a92-116">Sets the debugging time-out value.</span></span>                              |
| [<span data-ttu-id="86a92-117">**DbgWaitForMultipleObjects**</span><span class="sxs-lookup"><span data-stu-id="86a92-117">**DbgWaitForMultipleObjects**</span></span>](dbgwaitformultipleobjects.md) | <span data-ttu-id="86a92-118">Attend qu’un ou plusieurs des objets spécifiés soient signalés.</span><span class="sxs-lookup"><span data-stu-id="86a92-118">Waits for any (or all) of the specified objects to be signaled.</span></span> |
| [<span data-ttu-id="86a92-119">**DbgWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="86a92-119">**DbgWaitForSingleObject**</span></span>](dbgwaitforsingleobject.md)       | <span data-ttu-id="86a92-120">Attend qu’un objet soit signalé.</span><span class="sxs-lookup"><span data-stu-id="86a92-120">Waits for an object to become signaled.</span></span>                         |



 

 

 



