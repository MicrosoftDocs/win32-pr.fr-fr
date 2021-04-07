---
title: Utilisation de COM dans votre application Windows
description: Le module 1 de cette série a montré comment créer une fenêtre et répondre aux messages de fenêtre tels que WM \_ Paint et WM \_ Close. Le module 2 présente le modèle COM (Component Object Model).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726949"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a><span data-ttu-id="5889b-104">Module 2.</span><span class="sxs-lookup"><span data-stu-id="5889b-104">Module 2.</span></span> <span data-ttu-id="5889b-105">Utilisation de COM dans votre programme Windows-Based</span><span class="sxs-lookup"><span data-stu-id="5889b-105">Using COM in Your Windows-Based Program</span></span>

<span data-ttu-id="5889b-106">Le [module 1](your-first-windows-program.md) de cette série a montré comment créer une fenêtre et répondre aux messages de fenêtre tels que [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) et [**WM \_ Close**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="5889b-106">[Module 1](your-first-windows-program.md) of this series showed how to create a window and respond to window messages such as [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span> <span data-ttu-id="5889b-107">Le module 2 présente le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="5889b-107">Module 2 introduces the Component Object Model (COM).</span></span>

<span data-ttu-id="5889b-108">COM est une spécification permettant de créer des composants logiciels réutilisables.</span><span class="sxs-lookup"><span data-stu-id="5889b-108">COM is a specification for creating reusable software components.</span></span> <span data-ttu-id="5889b-109">La plupart des fonctionnalités que vous allez utiliser dans un programme Windows moderne s’appuient sur COM, comme suit :</span><span class="sxs-lookup"><span data-stu-id="5889b-109">Many of the features that you will use in a modern Windows-based program rely on COM, such as the following:</span></span>

-   <span data-ttu-id="5889b-110">Graphiques (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="5889b-110">Graphics (Direct2D)</span></span>
-   <span data-ttu-id="5889b-111">Texte (DirectWrite)</span><span class="sxs-lookup"><span data-stu-id="5889b-111">Text (DirectWrite)</span></span>
-   <span data-ttu-id="5889b-112">Le shell Windows</span><span class="sxs-lookup"><span data-stu-id="5889b-112">The Windows Shell</span></span>
-   <span data-ttu-id="5889b-113">Contrôle de ruban</span><span class="sxs-lookup"><span data-stu-id="5889b-113">The Ribbon control</span></span>
-   <span data-ttu-id="5889b-114">Animation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="5889b-114">UI animation</span></span>

<span data-ttu-id="5889b-115">(Certaines technologies de cette liste utilisent un sous-ensemble de COM et ne sont donc pas des COM « purs ».)</span><span class="sxs-lookup"><span data-stu-id="5889b-115">(Some technologies on this list use a subset of COM and are therefore not "pure" COM.)</span></span>

<span data-ttu-id="5889b-116">COM offre une réputation difficile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="5889b-116">COM has a reputation for being difficult to learn.</span></span> <span data-ttu-id="5889b-117">Et il est vrai que l’écriture d’un nouveau module logiciel pour prendre en charge COM peut être délicate.</span><span class="sxs-lookup"><span data-stu-id="5889b-117">And it is true that writing a new software module to support COM can be tricky.</span></span> <span data-ttu-id="5889b-118">Mais si votre programme est strictement un *consommateur* de com, vous constaterez peut-être que com est plus facile à comprendre que prévu.</span><span class="sxs-lookup"><span data-stu-id="5889b-118">But if your program is strictly a *consumer* of COM, you may find that COM is easier to understand than you expect.</span></span>

<span data-ttu-id="5889b-119">Ce module montre comment appeler des API COM dans votre programme.</span><span class="sxs-lookup"><span data-stu-id="5889b-119">This module shows how to call COM-based APIs in your program.</span></span> <span data-ttu-id="5889b-120">Elle décrit également quelques-unes des raisons de la conception de COM.</span><span class="sxs-lookup"><span data-stu-id="5889b-120">It also describes some of the reasoning behind the design of COM.</span></span> <span data-ttu-id="5889b-121">Si vous comprenez pourquoi COM est conçu comme c’est le cas, vous pouvez le programmer plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="5889b-121">If you understand why COM is designed as it is, you can program with it more effectively.</span></span> <span data-ttu-id="5889b-122">La deuxième partie du module décrit quelques pratiques de programmation recommandées pour COM.</span><span class="sxs-lookup"><span data-stu-id="5889b-122">The second part of the module describes some recommended programming practices for COM.</span></span>

<span data-ttu-id="5889b-123">COM a été introduit dans 1993 pour prendre en charge la liaison et l’incorporation d’objets (OLE) 2,0.</span><span class="sxs-lookup"><span data-stu-id="5889b-123">COM was introduced in 1993 to support Object Linking and Embedding (OLE) 2.0.</span></span> <span data-ttu-id="5889b-124">Les gens pensent parfois que COM et OLE sont identiques.</span><span class="sxs-lookup"><span data-stu-id="5889b-124">People sometimes think that COM and OLE are the same thing.</span></span> <span data-ttu-id="5889b-125">Il peut s’agir d’une autre raison de croire que COM est difficile à apprendre.</span><span class="sxs-lookup"><span data-stu-id="5889b-125">This may be another reason for the perception that COM is difficult to learn.</span></span> <span data-ttu-id="5889b-126">OLE 2,0 repose sur COM, mais vous n’avez pas besoin de connaître OLE pour comprendre COM.</span><span class="sxs-lookup"><span data-stu-id="5889b-126">OLE 2.0 is built on COM, but you do not have to know OLE to understand COM.</span></span>

<span data-ttu-id="5889b-127">COM est une *norme binaire*, et non une norme de langage : elle définit l’interface binaire entre une application et un composant logiciel.</span><span class="sxs-lookup"><span data-stu-id="5889b-127">COM is a *binary standard*, not a language standard: It defines the binary interface between an application and a software component.</span></span> <span data-ttu-id="5889b-128">En tant que norme binaire, COM est indépendant du langage, bien qu’il corresponde naturellement à certaines constructions C++.</span><span class="sxs-lookup"><span data-stu-id="5889b-128">As a binary standard, COM is language-neutral, although it maps naturally to certain C++ constructs.</span></span> <span data-ttu-id="5889b-129">Ce module se concentrera sur trois objectifs principaux de COM :</span><span class="sxs-lookup"><span data-stu-id="5889b-129">This module will focus on three major goals of COM:</span></span>

-   <span data-ttu-id="5889b-130">Séparation de l’implémentation d’un objet de son interface.</span><span class="sxs-lookup"><span data-stu-id="5889b-130">Separating the implementation of an object from its interface.</span></span>
-   <span data-ttu-id="5889b-131">Gestion de la durée de vie d’un objet.</span><span class="sxs-lookup"><span data-stu-id="5889b-131">Managing the lifetime of an object.</span></span>
-   <span data-ttu-id="5889b-132">Découverte des fonctionnalités d’un objet au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5889b-132">Discovering the capabilities of an object at run time.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5889b-133">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="5889b-133">In this section</span></span>

-   [<span data-ttu-id="5889b-134">Qu’est-ce qu’une interface COM ?</span><span class="sxs-lookup"><span data-stu-id="5889b-134">What Is a COM Interface?</span></span>](what-is-a-com-interface-.md)
-   [<span data-ttu-id="5889b-135">Initialisation de la bibliothèque COM</span><span class="sxs-lookup"><span data-stu-id="5889b-135">Initializing the COM Library</span></span>](initializing-the-com-library.md)
-   [<span data-ttu-id="5889b-136">Codes d’erreur dans COM</span><span class="sxs-lookup"><span data-stu-id="5889b-136">Error Codes in COM</span></span>](error-codes-in-com.md)
-   [<span data-ttu-id="5889b-137">Création d’un objet dans COM</span><span class="sxs-lookup"><span data-stu-id="5889b-137">Creating an Object in COM</span></span>](creating-an-object-in-com.md)
-   [<span data-ttu-id="5889b-138">Exemple : la boîte de dialogue Ouvrir</span><span class="sxs-lookup"><span data-stu-id="5889b-138">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)
-   [<span data-ttu-id="5889b-139">Gestion de la durée de vie d’un objet</span><span class="sxs-lookup"><span data-stu-id="5889b-139">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)
-   [<span data-ttu-id="5889b-140">Demande d’un objet pour une interface</span><span class="sxs-lookup"><span data-stu-id="5889b-140">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)
-   [<span data-ttu-id="5889b-141">Allocation de mémoire dans COM</span><span class="sxs-lookup"><span data-stu-id="5889b-141">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)
-   [<span data-ttu-id="5889b-142">Pratiques de codage COM</span><span class="sxs-lookup"><span data-stu-id="5889b-142">COM Coding Practices</span></span>](com-coding-practices.md)
-   [<span data-ttu-id="5889b-143">Gestion des erreurs dans COM</span><span class="sxs-lookup"><span data-stu-id="5889b-143">Error Handling in COM</span></span>](error-handling-in-com.md)

## <a name="related-topics"></a><span data-ttu-id="5889b-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5889b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5889b-145">Apprendre à programmer pour Windows en C++</span><span class="sxs-lookup"><span data-stu-id="5889b-145">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 