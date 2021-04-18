---
description: Par défaut, toutes les exceptions FP sont désactivées sur le système.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Exceptions de virgule flottante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519200"
---
# <a name="floating-point-exceptions"></a><span data-ttu-id="e1410-103">Exceptions de virgule flottante</span><span class="sxs-lookup"><span data-stu-id="e1410-103">Floating-Point Exceptions</span></span>

<span data-ttu-id="e1410-104">Par défaut, toutes les exceptions FP sont désactivées sur le système.</span><span class="sxs-lookup"><span data-stu-id="e1410-104">By default, the system has all FP exceptions turned off.</span></span> <span data-ttu-id="e1410-105">Par conséquent, les calculs aboutissent à NAN ou à Infinity, plutôt qu’à une exception.</span><span class="sxs-lookup"><span data-stu-id="e1410-105">Therefore, computations result in NAN or INFINITY, rather than an exception.</span></span> <span data-ttu-id="e1410-106">Avant de pouvoir intercepter les exceptions à virgule flottante (FP) à l’aide de la gestion structurée des exceptions, vous devez appeler la fonction de la bibliothèque Runtime C [ \_ controlfp \_ ](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) pour activer toutes les exceptions FP possibles.</span><span class="sxs-lookup"><span data-stu-id="e1410-106">Before you can trap floating-point (FP) exceptions using structured exception handling, you must call the [\_controlfp\_s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C run-time library function to turn on all possible FP exceptions.</span></span> <span data-ttu-id="e1410-107">Pour intercepter uniquement des exceptions particulières, utilisez uniquement les indicateurs qui correspondent aux exceptions à intercepter.</span><span class="sxs-lookup"><span data-stu-id="e1410-107">To trap only particular exceptions, use only the flags that correspond to the exceptions to be trapped.</span></span> <span data-ttu-id="e1410-108">Notez que tout gestionnaire d’erreurs FP doit appeler [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) comme première instruction FP.</span><span class="sxs-lookup"><span data-stu-id="e1410-108">Note that any handler for FP errors should call [\_clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) as its first FP instruction.</span></span> <span data-ttu-id="e1410-109">Cette fonction efface les exceptions à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="e1410-109">This function clears floating-point exceptions.</span></span>

 

 
