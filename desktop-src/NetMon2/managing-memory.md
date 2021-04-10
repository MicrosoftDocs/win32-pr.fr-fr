---
description: Si un expert échoue au moment de l’exécution, si vous utilisez Moniteur réseau Functions pour la gestion de la mémoire, Moniteur réseau libère la mémoire allouée.
ms.assetid: b6f5749b-161e-47a7-82cf-d85ad3703ecd
title: Gestion de la mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2e2a6cca89a095c03c5c0cad25642b87d2c252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951269"
---
# <a name="managing-memory"></a><span data-ttu-id="2ea7a-103">Gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="2ea7a-103">Managing Memory</span></span>

<span data-ttu-id="2ea7a-104">Si un expert échoue au moment de l’exécution, si vous utilisez Moniteur réseau Functions pour la gestion de la mémoire, Moniteur réseau libère la mémoire allouée.</span><span class="sxs-lookup"><span data-stu-id="2ea7a-104">Should an expert fail during run time, if you use Network Monitor functions for memory management, Network Monitor will free allocated memory.</span></span> <span data-ttu-id="2ea7a-105">Toutefois, lorsque vous écrivez un expert, il peut être nécessaire d’acquérir des ressources système et des informations sur la structure des données.</span><span class="sxs-lookup"><span data-stu-id="2ea7a-105">However, when you write an expert, it might be necessary to acquire system resources and data structure information.</span></span> <span data-ttu-id="2ea7a-106">Par exemple, l’expert de la fusion de protocole Moniteur réseau acquiert un descripteur de fichier pour générer une nouvelle capture.</span><span class="sxs-lookup"><span data-stu-id="2ea7a-106">For example, the Network Monitor Protocol Coalesce Expert acquires a file handle to build a new capture.</span></span> <span data-ttu-id="2ea7a-107">Chaque expert doit créer son propre traitement **try/catch** afin que l’expert puisse libérer les ressources qu’il a acquises.</span><span class="sxs-lookup"><span data-stu-id="2ea7a-107">Each expert must build its own **try/catch** handling so that the expert can free resources it acquired.</span></span>

<span data-ttu-id="2ea7a-108">Lorsque la mémoire est allouée, utilisez les fonctions de mémoire existantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ea7a-108">When memory is allocated, use the following existing memory functions:</span></span>

-   [<span data-ttu-id="2ea7a-109">**ExpertAllocMemory**</span><span class="sxs-lookup"><span data-stu-id="2ea7a-109">**ExpertAllocMemory**</span></span>](expertallocmemory.md)
-   [<span data-ttu-id="2ea7a-110">**ExpertReallocMemory**</span><span class="sxs-lookup"><span data-stu-id="2ea7a-110">**ExpertReallocMemory**</span></span>](expertreallocmemory.md)

 

 



