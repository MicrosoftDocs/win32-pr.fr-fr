---
description: Les mécanismes de gestion structurée des exceptions et de gestion des arrêts sont des parties entières du système. ils permettent au système d’être robuste. Vous pouvez utiliser ces mécanismes pour créer de manière cohérente des applications fiables et fiables.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: À propos de la gestion structurée des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200911"
---
# <a name="about-structured-exception-handling"></a><span data-ttu-id="65f64-104">À propos de la gestion structurée des exceptions</span><span class="sxs-lookup"><span data-stu-id="65f64-104">About Structured Exception Handling</span></span>

<span data-ttu-id="65f64-105">Les mécanismes de gestion structurée des exceptions et de gestion des arrêts sont des parties entières du système. ils permettent au système d’être robuste.</span><span class="sxs-lookup"><span data-stu-id="65f64-105">The structured exception handling and termination handling mechanisms are integral parts of the system; they enable the system to be robust.</span></span> <span data-ttu-id="65f64-106">Vous pouvez utiliser ces mécanismes pour créer de manière cohérente des applications fiables et fiables.</span><span class="sxs-lookup"><span data-stu-id="65f64-106">You can use these mechanisms to create consistently robust and reliable applications.</span></span>

<span data-ttu-id="65f64-107">La gestion structurée des exceptions est rendue disponible principalement via la prise en charge du compilateur.</span><span class="sxs-lookup"><span data-stu-id="65f64-107">Structured exception handling is made available primarily through compiler support.</span></span> <span data-ttu-id="65f64-108">Par exemple, le compilateur d’optimisation Microsoft C/C++ prend en charge le mot clé **\_ \_ try** qui identifie un corps de code protégé, le mot clé **\_ \_ except** qui identifie un gestionnaire d’exceptions et le mot clé **\_ \_ finally** qui identifie un gestionnaire d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="65f64-108">For example, the Microsoft C/C++ Optimizing Compiler supports the **\_\_try** keyword that identifies a guarded body of code, the **\_\_except** keyword that identifies an exception handler, and the **\_\_finally** keyword that identifies a termination handler.</span></span> <span data-ttu-id="65f64-109">Bien que cette vue d’ensemble utilise des exemples spécifiques au compilateur Microsoft C/C++, d’autres compilateurs fournissent également cette prise en charge.</span><span class="sxs-lookup"><span data-stu-id="65f64-109">Although this overview uses examples specific to the Microsoft C/C++ compiler, other compilers provide this support as well.</span></span>

-   [<span data-ttu-id="65f64-110">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="65f64-110">Exception Handling</span></span>](exception-handling.md)
-   [<span data-ttu-id="65f64-111">Gestion des exceptions basée sur des frames</span><span class="sxs-lookup"><span data-stu-id="65f64-111">Frame-based Exception Handling</span></span>](frame-based-exception-handling.md)
-   [<span data-ttu-id="65f64-112">Gestion des exceptions vectorisées</span><span class="sxs-lookup"><span data-stu-id="65f64-112">Vectored Exception Handling</span></span>](vectored-exception-handling.md)
-   [<span data-ttu-id="65f64-113">Gestion des arrêts</span><span class="sxs-lookup"><span data-stu-id="65f64-113">Termination Handling</span></span>](termination-handling.md)
-   [<span data-ttu-id="65f64-114">Syntaxe du gestionnaire</span><span class="sxs-lookup"><span data-stu-id="65f64-114">Handler Syntax</span></span>](handler-syntax.md)

 

 



