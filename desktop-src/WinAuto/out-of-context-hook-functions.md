---
title: Fonctions de raccordement hors contexte
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'En savoir plus sur : fonctions de raccordement hors contexte'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867154"
---
# <a name="out-of-context-hook-functions"></a><span data-ttu-id="3d800-103">Fonctions de raccordement hors contexte</span><span class="sxs-lookup"><span data-stu-id="3d800-103">Out-of-Context Hook Functions</span></span>

<span data-ttu-id="3d800-104">La liste suivante présente les principaux aspects des fonctions de raccordement hors contexte :</span><span class="sxs-lookup"><span data-stu-id="3d800-104">The following list outlines the key aspects of out-of-context hook functions:</span></span>

-   <span data-ttu-id="3d800-105">Les fonctions de raccordement hors contexte se trouvent dans l’espace d’adressage du client, que ce soit dans le corps du code ou dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="3d800-105">Out-of-context hook functions are located in the client's address space, whether it is in the code body or in a DLL.</span></span>
-   <span data-ttu-id="3d800-106">Les fonctions de raccordement hors contexte ne sont pas mappées à l’espace d’adressage du serveur.</span><span class="sxs-lookup"><span data-stu-id="3d800-106">Out-of-context hook functions are not mapped into the server's address space.</span></span>
-   <span data-ttu-id="3d800-107">Lorsqu’un événement est déclenché, les paramètres de la fonction de raccordement sont marshalés au-delà des limites du processus.</span><span class="sxs-lookup"><span data-stu-id="3d800-107">When an event is triggered, the parameters for the hook function are marshaled across process boundaries.</span></span>
-   <span data-ttu-id="3d800-108">Les fonctions de raccordement hors contexte sont sensiblement plus lentes que les fonctions de raccordement dans le contexte en raison du marshaling.</span><span class="sxs-lookup"><span data-stu-id="3d800-108">Out-of-context hook functions are noticeably slower than in-context hook functions due to marshaling.</span></span>
-   <span data-ttu-id="3d800-109">Le système met en file d’attente les notifications d’événements afin qu’elles arrivent de manière asynchrone (en raison du temps nécessaire pour effectuer le marshaling).</span><span class="sxs-lookup"><span data-stu-id="3d800-109">The system queues the event notifications so that they arrive asynchronously (because of the time required to perform marshaling).</span></span>

<span data-ttu-id="3d800-110">Bien que les notifications d’événements soient asynchrones, Microsoft Active Accessibility garantit que la fonction de rappel reçoit tous les événements dans l’ordre dans lequel ils sont générés.</span><span class="sxs-lookup"><span data-stu-id="3d800-110">Although the event notifications are asynchronous, Microsoft Active Accessibility assures that the callback function receives all events in the order in which they are generated.</span></span>

<span data-ttu-id="3d800-111">Le composant utilisateur du système d’exploitation alloue de la mémoire pour les événements gérés par des fonctions de raccordement hors contexte.</span><span class="sxs-lookup"><span data-stu-id="3d800-111">The USER component of the operating system allocates memory for events that are handled by out-of-context hook functions.</span></span> <span data-ttu-id="3d800-112">La mémoire est libérée lorsque les fonctions de raccordement retournent.</span><span class="sxs-lookup"><span data-stu-id="3d800-112">The memory is freed when the hook functions return.</span></span> <span data-ttu-id="3d800-113">Si une fonction de raccordement ne traite pas les événements assez rapidement, les ressources utilisateur sont abaissées, ce qui finit par entraîner une erreur ou des temps de réponse extrêmement lents.</span><span class="sxs-lookup"><span data-stu-id="3d800-113">If a hook function does not process events quickly enough, USER resources are lowered, eventually resulting in a fault or extremely slow response times.</span></span> <span data-ttu-id="3d800-114">Ces problèmes peuvent se produire dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="3d800-114">These problems may occur if:</span></span>

-   <span data-ttu-id="3d800-115">Les événements sont déclenchés très rapidement.</span><span class="sxs-lookup"><span data-stu-id="3d800-115">Events are fired very rapidly.</span></span>
-   <span data-ttu-id="3d800-116">Le système est lent.</span><span class="sxs-lookup"><span data-stu-id="3d800-116">The system is slow.</span></span>
-   <span data-ttu-id="3d800-117">La fonction de raccordement traite les événements lentement.</span><span class="sxs-lookup"><span data-stu-id="3d800-117">The hook function processes events slowly.</span></span>
-   <span data-ttu-id="3d800-118">Le client s’exécute sous Windows 9x.</span><span class="sxs-lookup"><span data-stu-id="3d800-118">The client is running on Windows 9x.</span></span>

 

 




