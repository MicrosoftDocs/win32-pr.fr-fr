---
description: Les techniques de débogage pour les applications COM+ dépendent du langage dans lequel vous choisissez d’écrire votre composant.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Débogage des applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db096ceb525cd988afa55e49cc88fda0ddf52549
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748868"
---
# <a name="debugging-com-applications"></a><span data-ttu-id="ad91b-103">Débogage des applications COM+</span><span class="sxs-lookup"><span data-stu-id="ad91b-103">Debugging COM+ Applications</span></span>

<span data-ttu-id="ad91b-104">Les techniques de débogage pour les applications COM+ dépendent du langage dans lequel vous choisissez d’écrire votre composant.</span><span class="sxs-lookup"><span data-stu-id="ad91b-104">Debugging techniques for COM+ applications depend on the language in which you choose to write your component.</span></span>

<span data-ttu-id="ad91b-105">Si vous codez dans Microsoft Visual C++, vous pouvez lancer le débogueur en C++ ou, avec un client distant, vous pouvez procéder au débogage à l’aide du contrôle de procédure à distance (RPC) OLE et du débogage juste-à-temps (JIT).</span><span class="sxs-lookup"><span data-stu-id="ad91b-105">If you code in Microsoft Visual C++, you can launch the debugger in C++ or, with a remote client, you can debug by using OLE remote procedure control (RPC) and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="ad91b-106">Vous pouvez toujours utiliser l’outil d’administration Services de composants pour déboguer votre composant à l’aide du paramètre **lancement com+ dans le débogueur** sous l’onglet **avancé** de la boîte de dialogue **Propriétés** de l’application com+.</span><span class="sxs-lookup"><span data-stu-id="ad91b-106">You can always use the Component Services administrative tool to debug your component with the COM+ **Launch in debugger** setting on the **Advanced** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="ad91b-107">Pour plus d’informations sur le débogage des composants codés en C++, consultez [débogage de composants écrits en Visual C++](debugging-components-written-in-visual-c--.md).</span><span class="sxs-lookup"><span data-stu-id="ad91b-107">For more information on debugging components coded in C++, see [Debugging Components Written in Visual C++](debugging-components-written-in-visual-c--.md).</span></span>

<span data-ttu-id="ad91b-108">À moins que vous ne déboguez actuellement le multithreading, le suivi des composants, les appels distants ou l’isolation des processus, vous pouvez utiliser l’environnement Microsoft Visual Basic à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="ad91b-108">Unless you are currently debugging multithreading, component tracking, remote calls, or process isolation, you can use the Microsoft Visual Basic environment for debugging purposes.</span></span> <span data-ttu-id="ad91b-109">Les [composants de débogage écrits en Visual Basic](debugging-components-written-in-visual-basic.md) décrivent le processus de débogage dans un environnement Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ad91b-109">[Debugging Components Written in Visual Basic](debugging-components-written-in-visual-basic.md) describes the debugging process within a Visual Basic environment.</span></span>

<span data-ttu-id="ad91b-110">La rubrique [débogage dans l’IDE Visual Basic](debugging-in-the-visual-basic-ide.md) fournit une vue d’ensemble générale avec des indications, des conseils et une procédure de débogage dans l’environnement de développement intégré (IDE).</span><span class="sxs-lookup"><span data-stu-id="ad91b-110">The topic [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md) provides a general overview with guidelines, tips and a procedure on debugging in the integrated development environment (IDE).</span></span>

<span data-ttu-id="ad91b-111">Pour plus d’informations sur le débogage des processus avancés, consultez [débogage de composants Visual Basic compilés](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="ad91b-111">To view more information about debugging advanced processes, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

> [!Note]  
> <span data-ttu-id="ad91b-112">Plusieurs limitations associées à l’utilisation de l’environnement de Visual Basic pour déboguer des composants avec MTS ont été résolues pour COM+.</span><span class="sxs-lookup"><span data-stu-id="ad91b-112">Several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="ad91b-113">Pour plus d’informations, consultez [prise en charge du débogage des Visual Basic com+ et différences avec MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="ad91b-113">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ad91b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ad91b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad91b-115">Gestion des erreurs dans COM+</span><span class="sxs-lookup"><span data-stu-id="ad91b-115">Handling Errors in COM+</span></span>](handling-errors-in-com-.md)
</dt> </dl>

 

 



