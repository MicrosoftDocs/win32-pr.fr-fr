---
description: Bien qu’un&\# 160 ; contexte de reconnaissance&\# 160 ; ne soit pas accessible sur deux threads simultanément par la plateforme Tablet PC, la fonction AdviseInkChange peut être appelée à tout moment sur n’importe quel thread.
ms.assetid: 2cd19819-08d0-418d-830b-2288a66ca0d0
title: Considérations sur les threads de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4297cc28e084bbb7c1c09593deb5babc2319ab43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530130"
---
# <a name="recognizer-threading-considerations"></a><span data-ttu-id="d7349-103">Considérations sur les threads de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="d7349-103">Recognizer Threading Considerations</span></span>

<span data-ttu-id="d7349-104">Bien qu’un contexte de module de [reconnaissance](hrecocontext-handle.md) ne soit pas accessible sur deux threads simultanément par la plateforme Tablet PC, la fonction [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) peut être appelée à tout moment sur n’importe quel thread.</span><span class="sxs-lookup"><span data-stu-id="d7349-104">Although a [recognizer context](hrecocontext-handle.md) cannot be accessed on two threads simultaneously by the Tablet PC platform, the [**AdviseInkChange**](/windows/desktop/api/recapis/nf-recapis-adviseinkchange) function can be called at any time on any thread.</span></span> <span data-ttu-id="d7349-105">Étant donné que la plateforme Tablet PC ne garantit pas qu’il n’existe qu’un seul contexte de reconnaissance à la fois, deux contextes de reconnaissance distincts dans des threads distincts peuvent tenter d’accéder simultanément à votre module de [reconnaissance](hrecognizer-handle.md).</span><span class="sxs-lookup"><span data-stu-id="d7349-105">Because the Tablet PC platform does not ensure that there is only one recognizer context at a time, two separate recognizer contexts in separate threads may simultaneously attempt to access your [recognizer](hrecognizer-handle.md).</span></span> <span data-ttu-id="d7349-106">Par conséquent, les variables globales de votre moteur de reconnaissance doivent être thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d7349-106">Therefore, global variables in your recognition engine must be thread-safe.</span></span>

<span data-ttu-id="d7349-107">Les listes de mots sont une implémentation facultative qui permet d’améliorer la précision.</span><span class="sxs-lookup"><span data-stu-id="d7349-107">Word lists are an optional implementation used to increase accuracy.</span></span> <span data-ttu-id="d7349-108">Si votre module de reconnaissance implémente des listes de mots, il doit être thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d7349-108">If your recognizer implements word lists, it must be thread-safe.</span></span> <span data-ttu-id="d7349-109">Pour plus d’informations sur l’utilisation des listes de mots, consultez [utilisation de dictionnaires d’applications](using-application-dictionaries.md).</span><span class="sxs-lookup"><span data-stu-id="d7349-109">For more information about using word lists, see [Using Application Dictionaries](using-application-dictionaries.md).</span></span>

<span data-ttu-id="d7349-110">Pour plus d’informations sur les autres considérations relatives aux threads, consultez Considérations sur les [Threads Tablet PC](tablet-pc-threading-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="d7349-110">For details about other threading considerations, see [Tablet PC Threading Considerations](tablet-pc-threading-considerations.md).</span></span>

 

 



