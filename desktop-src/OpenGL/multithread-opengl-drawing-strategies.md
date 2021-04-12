---
title: Stratégies de dessin OpenGL multithread
description: GDI ne prend pas en charge plusieurs threads.
ms.assetid: 3930029d-b2d9-4beb-bad6-4962f952d7ee
keywords:
- OpenGL sur Windows, dessin multithread
- dessin OpenGL multithread OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bccb08d48bd8ccb62584f15911a1eb65080c4a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309793"
---
# <a name="multithread-opengl-drawing-strategies"></a><span data-ttu-id="edfe5-105">Stratégies de dessin OpenGL multithread</span><span class="sxs-lookup"><span data-stu-id="edfe5-105">Multithread OpenGL Drawing Strategies</span></span>

<span data-ttu-id="edfe5-106">GDI ne prend pas en charge plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="edfe5-106">The GDI does not support multiple threads.</span></span> <span data-ttu-id="edfe5-107">Vous devez utiliser un contexte de périphérique distinct et un contexte de rendu distinct pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="edfe5-107">You must use a distinct device context and a distinct rendering context for each thread.</span></span> <span data-ttu-id="edfe5-108">Cela a tendance à limiter les avantages en termes de performances liés à l’utilisation de plusieurs threads avec des systèmes à un seul processeur exécutant des applications OpenGL.</span><span class="sxs-lookup"><span data-stu-id="edfe5-108">This tends to limit the performance advantages of using multiple threads with single-processor systems running OpenGL applications.</span></span> <span data-ttu-id="edfe5-109">Toutefois, il existe des moyens d’utiliser des threads avec un système à processeur unique pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="edfe5-109">However, there are ways to use threads with a single processor system to greatly increase performance.</span></span> <span data-ttu-id="edfe5-110">Par exemple, vous pouvez utiliser un thread distinct pour passer des appels de rendu OpenGL au matériel 3D dédié.</span><span class="sxs-lookup"><span data-stu-id="edfe5-110">For example, you can use a separate thread to pass OpenGL rendering calls to dedicated 3-D hardware.</span></span>

<span data-ttu-id="edfe5-111">Les systèmes de multitraitement symétrique (SMP) peuvent tirer parti de l’utilisation de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="edfe5-111">Symmetric multiprocessing (SMP) systems can greatly benefit from using multiple threads.</span></span> <span data-ttu-id="edfe5-112">Une stratégie évidente consiste à utiliser un thread distinct pour chaque processeur afin de gérer le rendu OpenGL dans des fenêtres distinctes.</span><span class="sxs-lookup"><span data-stu-id="edfe5-112">An obvious strategy is to use a separate thread for each processor to handle OpenGL rendering in separate windows.</span></span> <span data-ttu-id="edfe5-113">Par exemple, dans une application de simulation de vol, vous pouvez utiliser des processeurs et des threads distincts pour afficher les vues avant, arrière et latérale.</span><span class="sxs-lookup"><span data-stu-id="edfe5-113">For example, in a flight-simulation application you could use separate processors and threads to render the front, back, and side views.</span></span>

<span data-ttu-id="edfe5-114">Un thread ne peut avoir qu’un seul contexte de rendu actif en cours.</span><span class="sxs-lookup"><span data-stu-id="edfe5-114">A thread can have only one current, active rendering context.</span></span> <span data-ttu-id="edfe5-115">Lorsque vous utilisez plusieurs threads et plusieurs contextes de rendu, vous devez veiller à synchroniser leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="edfe5-115">When you use multiple threads and multiple rendering contexts, you must be careful to synchronize their use.</span></span> <span data-ttu-id="edfe5-116">Par exemple, utilisez un seul thread pour appeler [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) une fois que tous les threads ont fini de dessiner.</span><span class="sxs-lookup"><span data-stu-id="edfe5-116">For example, use one thread only to call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers) after all threads finish drawing.</span></span>

 

 




