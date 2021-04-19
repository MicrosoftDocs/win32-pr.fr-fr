---
description: 'En savoir plus sur : événements de suivi de gestion de la mémoire'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Événements de suivi de gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522462"
---
# <a name="memory-management-tracing-events"></a><span data-ttu-id="cc93a-103">Événements de suivi de gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="cc93a-103">Memory Management Tracing Events</span></span>

<span data-ttu-id="cc93a-104">Cette section fournit des informations détaillées sur les détails des événements de suivi de gestion de la mémoire spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cc93a-104">This section describes detailed information on specific Memory management tracing event details.</span></span>

<span data-ttu-id="cc93a-105">Le suivi de la gestion de la mémoire est une fonctionnalité de résolution des problèmes qui peut être activée dans les binaires de la version commerciale pour suivre certains événements de gestion de la mémoire avec une charge minimale.</span><span class="sxs-lookup"><span data-stu-id="cc93a-105">Memory management tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain memory management events with minimal overhead.</span></span> <span data-ttu-id="cc93a-106">Cette fonctionnalité permet de meilleures fonctionnalités de diagnostic pour les développeurs et le support technique.</span><span class="sxs-lookup"><span data-stu-id="cc93a-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="cc93a-107">Le suivi des événements de gestion de la mémoire prend en charge le suivi de l’allocation des tas, la réallocation et les opérations gratuites.</span><span class="sxs-lookup"><span data-stu-id="cc93a-107">Memory management event tracing supports tracing heap allocation, reallocation, and free operations.</span></span>

<span data-ttu-id="cc93a-108">Le suivi d’événements de gestion de la mémoire utilise Suivi d’v nements pour Windows (ETW), une fonctionnalité de traçage à usage général et à haut débit fournie par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cc93a-108">Memory management event tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="cc93a-109">ETW fournit un mécanisme de suivi pour les événements déclenchés par les applications en mode utilisateur et les pilotes de périphérique en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="cc93a-109">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="cc93a-110">ETW permet d’activer et de désactiver la journalisation dynamique, ce qui facilite l’exécution du suivi détaillé dans les environnements de production sans nécessiter de redémarrage ou de redémarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="cc93a-110">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="cc93a-111">Le suivi d’événements de gestion de la mémoire à l’aide d’ETW est pris en charge sur Windows 7, Windows Server 2008 R2 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="cc93a-111">Memory management event tracing using ETW is supported on Windows 7 , Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="cc93a-112">Pour obtenir des informations générales sur ETW, consultez [améliorer le débogage et le réglage des performances avec ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="cc93a-112">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="cc93a-113">La liste suivante fournit des informations détaillées pour chaque événement de suivi de gestion de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc93a-113">The following list provides detailed information for each memory management tracing event.</span></span> <span data-ttu-id="cc93a-114">Pour plus d’informations sur les événements, cliquez sur le nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="cc93a-114">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="cc93a-115">Nom de l'événement</span><span class="sxs-lookup"><span data-stu-id="cc93a-115">Event Name</span></span>                                                  | <span data-ttu-id="cc93a-116">Description</span><span class="sxs-lookup"><span data-stu-id="cc93a-116">Description</span></span>                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="cc93a-117">**\_allocation d' \_ événement du tas ETW \_**</span><span class="sxs-lookup"><span data-stu-id="cc93a-117">**ETW\_HEAP\_EVENT\_ALLOC**</span></span>](etw-heap-event-alloc.md)     | <span data-ttu-id="cc93a-118">Événement de suivi de gestion de la mémoire pour une opération d’allocation de tas.</span><span class="sxs-lookup"><span data-stu-id="cc93a-118">Memory management tracing event for a heap allocation operation.</span></span>    |
| [<span data-ttu-id="cc93a-119">**\_événement de tas ETW \_ \_ gratuit**</span><span class="sxs-lookup"><span data-stu-id="cc93a-119">**ETW\_HEAP\_EVENT\_FREE**</span></span>](etw-heap-event-free.md)       | <span data-ttu-id="cc93a-120">Événement de suivi de gestion de la mémoire pour une opération libre de segment de mémoire.</span><span class="sxs-lookup"><span data-stu-id="cc93a-120">Memory management tracing event for a heap free operation.</span></span>          |
| [<span data-ttu-id="cc93a-121">**réallocation d' \_ événements de tas ETW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc93a-121">**ETW\_HEAP\_EVENT\_REALLOC**</span></span>](etw-heap-event-realloc.md) | <span data-ttu-id="cc93a-122">Événement de suivi de gestion de la mémoire pour une opération de réallocation de tas.</span><span class="sxs-lookup"><span data-stu-id="cc93a-122">Memory management tracing event for a heap re-allocation operation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cc93a-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc93a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc93a-124">Améliorer le débogage et le réglage des performances à l'aide du suivi ETW</span><span class="sxs-lookup"><span data-stu-id="cc93a-124">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
