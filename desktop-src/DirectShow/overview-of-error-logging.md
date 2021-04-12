---
description: Vue d’ensemble de la journalisation des erreurs
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Vue d’ensemble de la journalisation des erreurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109079"
---
# <a name="overview-of-error-logging"></a><span data-ttu-id="3af12-103">Vue d’ensemble de la journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="3af12-103">Overview of Error Logging</span></span>

<span data-ttu-id="3af12-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="3af12-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3af12-105">Pour offrir aux applications une flexibilité maximale dans la gestion des erreurs, les [services d’édition DirectShow](directshow-editing-services.md) utilisent un mécanisme de rappel.</span><span class="sxs-lookup"><span data-stu-id="3af12-105">To give applications maximum flexibility in handling errors, [DirectShow Editing Services](directshow-editing-services.md) uses a callback mechanism.</span></span> <span data-ttu-id="3af12-106">Votre application implémente une méthode de journalisation d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="3af12-106">Your application implements a method for logging an error.</span></span> <span data-ttu-id="3af12-107">Au moment de l’exécution, si une erreur se produit, l’algorithme DES appelle la méthode que vous avez fournie.</span><span class="sxs-lookup"><span data-stu-id="3af12-107">At run time, if an error occurs, DES calls the method you have provided.</span></span> <span data-ttu-id="3af12-108">La méthode accepte des paramètres qui décrivent l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3af12-108">The method takes parameters that describe the error.</span></span> <span data-ttu-id="3af12-109">Ce que fait la méthode avec ces informations vous revient.</span><span class="sxs-lookup"><span data-stu-id="3af12-109">What the method does with this information is up to you.</span></span> <span data-ttu-id="3af12-110">(Toutefois, il doit retourner aussi rapidement que possible, mais peut interférer avec l’exécution du programme.)</span><span class="sxs-lookup"><span data-stu-id="3af12-110">(It should return as quickly as possible, however, or it might interfere with the execution of the program.)</span></span>

<span data-ttu-id="3af12-111">La méthode de rappel d’enregistrement des erreurs est contenue dans une interface COM, [**IAMErrorLog**](iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="3af12-111">The error logging callback method is contained in a COM interface, [**IAMErrorLog**](iamerrorlog.md).</span></span> <span data-ttu-id="3af12-112">Votre application doit implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="3af12-112">Your application must implement this interface.</span></span> <span data-ttu-id="3af12-113">Comme toutes les interfaces COM, **IAMErrorLog** hérite de l’interface **IUnknown** , donc votre application doit également l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="3af12-113">Like all COM interfaces, **IAMErrorLog** inherits the **IUnknown** interface, so your application must implement that as well.</span></span>

<span data-ttu-id="3af12-114">Vous avez le choix entre plusieurs options pour implémenter ces interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="3af12-114">You have several choices for implementing these COM interfaces.</span></span> <span data-ttu-id="3af12-115">Vous pouvez utiliser la Active Template Library (ATL), qui fournit des implémentations de stock des méthodes **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="3af12-115">You can use the Active Template Library (ATL), which provides stock implementations of the **IUnknown** methods.</span></span> <span data-ttu-id="3af12-116">DirectShow fournit également une classe de base C++, [**CUnknown**](cunknown.md), qui permet d’implémenter facilement une interface com.</span><span class="sxs-lookup"><span data-stu-id="3af12-116">DirectShow also provides a C++ base class, [**CUnknown**](cunknown.md), that makes it easy to implement a COM interface.</span></span> <span data-ttu-id="3af12-117">Pour plus d’informations sur l’utilisation de **CUnknown**, consultez [How to implement IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="3af12-117">For information on using **CUnknown**, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

<span data-ttu-id="3af12-118">L’exemple de code de cet article définit une classe C++ autonome qui implémente à la fois **IUnknown** et **IAMErrorLog**.</span><span class="sxs-lookup"><span data-stu-id="3af12-118">The sample code in this article defines a self-contained C++ class, which implements both **IUnknown** and **IAMErrorLog**.</span></span> <span data-ttu-id="3af12-119">Le résultat n’est pas un vrai objet COM, car il ne prend pas en charge **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="3af12-119">The result is not a true COM object, because it does not support **CoCreateInstance**.</span></span> <span data-ttu-id="3af12-120">Toutefois, cette approche est adaptée à l’objectif de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="3af12-120">However, this approach is adequate for the purpose of the example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3af12-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3af12-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3af12-122">Journalisation des erreurs</span><span class="sxs-lookup"><span data-stu-id="3af12-122">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



