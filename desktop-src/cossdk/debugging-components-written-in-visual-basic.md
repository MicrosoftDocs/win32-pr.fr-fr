---
description: Débogage de composants écrits en Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Débogage de composants écrits en Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516586"
---
# <a name="debugging-components-written-in-visual-basic"></a><span data-ttu-id="5c362-103">Débogage de composants écrits en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5c362-103">Debugging Components Written in Visual Basic</span></span>

<span data-ttu-id="5c362-104">Vous pouvez utiliser l’environnement de développement Microsoft Visual Basic 6,0 pour le débogage dans certains scénarios.</span><span class="sxs-lookup"><span data-stu-id="5c362-104">You can use the Microsoft Visual Basic 6.0 development environment for debugging within certain scenarios.</span></span> <span data-ttu-id="5c362-105">L’utilisation de Visual Basic pour le débogage permet d’accéder à des outils familiers aux programmeurs Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5c362-105">Using Visual Basic for debugging allows access to tools familiar to Visual Basic programmers.</span></span> <span data-ttu-id="5c362-106">En revanche, comme lors du débogage Visual Basic composants s’exécutent dans le processus de l’environnement Visual Basic, il peut être nécessaire de déboguer votre composant après qu’il a été compilé à l’aide de l’environnement de développement Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="5c362-106">On the other hand, because during debugging Visual Basic components run within the Visual Basic environment's process, it may be necessary to debug your component after it has been compiled by using the Microsoft Visual C++ development environment.</span></span>

<span data-ttu-id="5c362-107">Pour plus d’informations sur le débogage dans l’environnement de développement intégré (IDE) Visual Basic, consultez [débogage dans l’ide Visual Basic](debugging-in-the-visual-basic-ide.md).</span><span class="sxs-lookup"><span data-stu-id="5c362-107">For more information about debugging within the Visual Basic integrated development environment (IDE), see [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span></span> <span data-ttu-id="5c362-108">Pour plus d’informations sur le débogage des composants de Visual Basic une fois qu’ils sont compilés à l’aide de l’environnement de développement Visual C++, consultez [débogage de composants Visual Basic compilés](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="5c362-108">For more on debugging Visual Basic components after they're compiled using the Visual C++ development environment, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

<span data-ttu-id="5c362-109">En outre, plusieurs limitations associées à l’utilisation de l’environnement de Visual Basic pour déboguer des composants avec MTS ont été résolues pour COM+.</span><span class="sxs-lookup"><span data-stu-id="5c362-109">Also, several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="5c362-110">Pour plus d’informations, consultez [prise en charge du débogage des Visual Basic com+ et différences avec MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="5c362-110">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

> [!Note]  
> <span data-ttu-id="5c362-111">Si vous avez déjà utilisé Visual Basic sur le même ordinateur que COM+, vous avez peut-être remarqué que le complément services de composants est disponible dans l’environnement Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5c362-111">If you have already used Visual Basic on the same computer as COM+, you may have noticed the Component Services add-in available in the Visual Basic environment.</span></span> <span data-ttu-id="5c362-112">À l’origine dans MTS, cette fonctionnalité a été conçue pour mettre à jour le registre chaque fois que vous recompilez un composant dans une application COM+.</span><span class="sxs-lookup"><span data-stu-id="5c362-112">Originally in MTS, this feature was designed to update the registry each time you recompiled a component in a COM+ application.</span></span> <span data-ttu-id="5c362-113">Toutefois, étant donné la nature de l’interaction du Registre Microsoft Windows et de la base de données d’inscription COM+, certains paramètres peuvent ne pas être entièrement mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5c362-113">However, given the nature of the interaction of the Microsoft Windows Registry and the COM+ registration database, some settings may not be completely updated.</span></span> <span data-ttu-id="5c362-114">Par conséquent, au lieu d’utiliser les commandes disponibles avec ce complément, vous devez supprimer et réinstaller vos composants pour mettre à jour les paramètres après la recompilation.</span><span class="sxs-lookup"><span data-stu-id="5c362-114">Therefore, instead of using the commands available with this add-in, you should remove and reinstall your components to update settings after recompiling.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5c362-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c362-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c362-116">Débogage de composants écrits en Visual C++</span><span class="sxs-lookup"><span data-stu-id="5c362-116">Debugging Components Written in Visual C++</span></span>](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



