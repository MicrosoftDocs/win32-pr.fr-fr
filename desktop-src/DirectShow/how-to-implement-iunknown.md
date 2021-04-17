---
description: Comment implémenter IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Comment implémenter IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520500"
---
# <a name="how-to-implement-iunknown"></a><span data-ttu-id="7e7be-103">Comment implémenter IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e7be-103">How to Implement IUnknown</span></span>

<span data-ttu-id="7e7be-104">Microsoft DirectShow est basé sur le modèle COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="7e7be-104">Microsoft DirectShow is based on the Component Object Model (COM).</span></span> <span data-ttu-id="7e7be-105">Si vous écrivez votre propre filtre, vous devez l’implémenter en tant qu’objet COM.</span><span class="sxs-lookup"><span data-stu-id="7e7be-105">If you write your own filter, you must implement it as a COM object.</span></span> <span data-ttu-id="7e7be-106">Les classes de base DirectShow fournissent une infrastructure à partir de laquelle effectuer cette opération.</span><span class="sxs-lookup"><span data-stu-id="7e7be-106">The DirectShow base classes provide a framework from which to do this.</span></span> <span data-ttu-id="7e7be-107">L’utilisation des classes de base n’est pas obligatoire, mais elle peut simplifier le processus de développement.</span><span class="sxs-lookup"><span data-stu-id="7e7be-107">Using the base classes is not required, but it can simplify the development process.</span></span> <span data-ttu-id="7e7be-108">Cet article décrit quelques-uns des détails internes des objets COM et leur implémentation dans les classes de base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7e7be-108">This article describes some of the internal details of COM objects and their implementation in the DirectShow base classes.</span></span>

<span data-ttu-id="7e7be-109">Cet article suppose que vous savez comment programmer des applications clientes COM, en d’autres termes, que vous comprenez les méthodes dans **IUnknown**, mais ne suppose pas d’expérience préalable du développement d’objets com.</span><span class="sxs-lookup"><span data-stu-id="7e7be-109">This article assumes that you know how to program COM client applications—in other words, that you understand the methods in **IUnknown**—but does not assume any prior experience developing COM objects.</span></span> <span data-ttu-id="7e7be-110">DirectShow gère un grand nombre des détails du développement d’un objet COM.</span><span class="sxs-lookup"><span data-stu-id="7e7be-110">DirectShow handles many of the details of developing a COM object.</span></span> <span data-ttu-id="7e7be-111">Si vous avez des difficultés à développer des objets COM, vous devez lire la section [à l’aide de CUnknown](using-cunknown.md), qui décrit la classe de base [**CUnknown**](cunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="7e7be-111">If you have experience developing COM objects, you should read the section [Using CUnknown](using-cunknown.md), which describes the [**CUnknown**](cunknown.md) base class.</span></span>

<span data-ttu-id="7e7be-112">COM est une spécification, et non une implémentation.</span><span class="sxs-lookup"><span data-stu-id="7e7be-112">COM is a specification, not an implementation.</span></span> <span data-ttu-id="7e7be-113">Il définit les règles qu’un composant doit suivre ; le fait de placer ces règles en vigueur est laissé au développeur.</span><span class="sxs-lookup"><span data-stu-id="7e7be-113">It defines the rules that a component must follow; putting those rules into effect is left to the developer.</span></span> <span data-ttu-id="7e7be-114">Dans DirectShow, tous les objets dérivent d’un ensemble de classes de base C++.</span><span class="sxs-lookup"><span data-stu-id="7e7be-114">In DirectShow, all objects derive from a set of C++ base classes.</span></span> <span data-ttu-id="7e7be-115">Les constructeurs et les méthodes de la classe de base effectuent la plupart des tâches de « comptabilité » COM, telles que la conservation d’un décompte de références cohérent.</span><span class="sxs-lookup"><span data-stu-id="7e7be-115">The base class constructors and methods do most of the COM "bookkeeping" work, such as keeping a consistent reference count.</span></span> <span data-ttu-id="7e7be-116">En dérivant votre filtre à partir d’une classe de base, vous héritez des fonctionnalités de la classe.</span><span class="sxs-lookup"><span data-stu-id="7e7be-116">By deriving your filter from a base class, you inherit the functionality of the class.</span></span> <span data-ttu-id="7e7be-117">Pour utiliser efficacement les classes de base, vous avez besoin d’une compréhension générale de la façon dont elles implémentent la spécification COM.</span><span class="sxs-lookup"><span data-stu-id="7e7be-117">To use base classes effectively, you need a general understanding of how they implement the COM specification.</span></span>

<span data-ttu-id="7e7be-118">Cet article contient les rubriques suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e7be-118">This article contains the following topics.</span></span>

-   [<span data-ttu-id="7e7be-119">Fonctionnement de IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e7be-119">How IUnknown Works</span></span>](how-iunknown-works.md)
-   [<span data-ttu-id="7e7be-120">Utilisation de CUnknown</span><span class="sxs-lookup"><span data-stu-id="7e7be-120">Using CUnknown</span></span>](using-cunknown.md)

## <a name="related-topics"></a><span data-ttu-id="7e7be-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e7be-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e7be-122">DirectShow et COM</span><span class="sxs-lookup"><span data-stu-id="7e7be-122">DirectShow and COM</span></span>](directshow-and-com.md)
</dt> </dl>

 

 



