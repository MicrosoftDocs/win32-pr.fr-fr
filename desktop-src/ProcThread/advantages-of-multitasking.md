---
description: Pour l’utilisateur, l’avantage du multitâche est la possibilité de permettre à plusieurs applications d’être ouvertes et opérationnelles en même temps. Par exemple, un utilisateur peut modifier un fichier avec une application alors qu’une autre application recalcule une feuille de calcul.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Avantages de la multitâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519893"
---
# <a name="advantages-of-multitasking"></a><span data-ttu-id="ecad7-104">Avantages de la multitâche</span><span class="sxs-lookup"><span data-stu-id="ecad7-104">Advantages of Multitasking</span></span>

<span data-ttu-id="ecad7-105">Pour l’utilisateur, l’avantage du multitâche est la possibilité de permettre à plusieurs applications d’être ouvertes et opérationnelles en même temps.</span><span class="sxs-lookup"><span data-stu-id="ecad7-105">To the user, the advantage of multitasking is the ability to have several applications open and working at the same time.</span></span> <span data-ttu-id="ecad7-106">Par exemple, un utilisateur peut modifier un fichier avec une application alors qu’une autre application recalcule une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="ecad7-106">For example, a user can edit a file with one application while another application is recalculating a spreadsheet.</span></span>

<span data-ttu-id="ecad7-107">Pour le développeur d’applications, l’avantage du multitâche est la possibilité de créer des applications qui utilisent plusieurs processus et de créer des processus qui utilisent plusieurs threads d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ecad7-107">To the application developer, the advantage of multitasking is the ability to create applications that use more than one process and to create processes that use more than one thread of execution.</span></span> <span data-ttu-id="ecad7-108">Par exemple, un processus peut avoir un thread d’interface utilisateur qui gère les interactions avec l’utilisateur (entrée de clavier et de souris) et les threads de travail qui effectuent d’autres tâches pendant que le thread d’interface utilisateur attend des entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecad7-108">For example, a process can have a user interface thread that manages interactions with the user (keyboard and mouse input), and worker threads that perform other tasks while the user interface thread waits for user input.</span></span> <span data-ttu-id="ecad7-109">Si vous attribuez une priorité plus élevée au thread d’interface utilisateur, l’application sera plus réactive pour l’utilisateur, tandis que les threads de travail utiliseront efficacement le processeur pendant les périodes où il n’y a aucune entrée d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecad7-109">If you give the user interface thread a higher priority, the application will be more responsive to the user, while the worker threads use the processor efficiently during the times when there is no user input.</span></span>

 

 



