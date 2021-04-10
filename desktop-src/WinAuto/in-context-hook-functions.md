---
title: Fonctions de raccordement In-Context
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'En savoir plus sur : fonctions de raccordement In-Context'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210741"
---
# <a name="in-context-hook-functions"></a><span data-ttu-id="2d29b-103">Fonctions de raccordement In-Context</span><span class="sxs-lookup"><span data-stu-id="2d29b-103">In-Context Hook Functions</span></span>

<span data-ttu-id="2d29b-104">La liste suivante présente les aspects clés des fonctions de raccordement dans le contexte :</span><span class="sxs-lookup"><span data-stu-id="2d29b-104">The following list outlines the key aspects of in-context hook functions:</span></span>

-   <span data-ttu-id="2d29b-105">Les fonctions de raccordement dans le contexte doivent se trouver dans une bibliothèque de liens dynamiques (DLL) que le système mappe à l’espace d’adressage du serveur.</span><span class="sxs-lookup"><span data-stu-id="2d29b-105">In-context hooks functions must be located in a dynamic-link library (DLL) that the system maps into the server's address space.</span></span>
-   <span data-ttu-id="2d29b-106">Les fonctions de raccordement dans le contexte partagent l’espace d’adressage avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="2d29b-106">In-context hook functions share the address space with the server.</span></span>
-   <span data-ttu-id="2d29b-107">Lorsque le serveur déclenche un événement, le système appelle une fonction de raccordement sans marshaling (empaquetage et envoi de paramètres d’interface entre les limites de processus).</span><span class="sxs-lookup"><span data-stu-id="2d29b-107">When the server triggers an event, the system calls a hook function without marshaling (packaging and sending interface parameters across process boundaries).</span></span>
-   <span data-ttu-id="2d29b-108">Les fonctions de raccordement dans le contexte ont tendance à être très rapides et à recevoir des notifications d’événements de façon synchrone, car il n’existe aucun marshaling.</span><span class="sxs-lookup"><span data-stu-id="2d29b-108">In-context hook functions tend to be very fast and receive event notifications synchronously because there is no marshaling.</span></span>
-   <span data-ttu-id="2d29b-109">Certains événements peuvent être remis hors processus, même si vous demandez qu’ils soient remis en cours (à l’aide de l' \_ indicateur INCONTEXT WINEVENT).</span><span class="sxs-lookup"><span data-stu-id="2d29b-109">Some events may be delivered out-of-process, even though you request that they be delivered in-process (using the WINEVENT\_INCONTEXT flag).</span></span> <span data-ttu-id="2d29b-110">Vous pouvez voir cette situation avec des problèmes d’interopérabilité des applications 64 bits et 32 bits et avec les événements de la console Windows.</span><span class="sxs-lookup"><span data-stu-id="2d29b-110">You might see this situation with 64-bit and 32-bit application interoperability issues and with Windows console events.</span></span>

 

 




