---
description: Pour économiser du temps et de la mémoire lors de l’utilisation de nombreux fichiers de symboles, utilisez la fonction SymSetOptions pour définir l’option de chargement différé des symboles ( \_ chargements différés SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Chargement de symboles différés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950384"
---
# <a name="deferred-symbol-loading"></a><span data-ttu-id="83473-103">Chargement de symboles différés</span><span class="sxs-lookup"><span data-stu-id="83473-103">Deferred Symbol Loading</span></span>

<span data-ttu-id="83473-104">Pour économiser du temps et de la mémoire lors de l’utilisation de nombreux fichiers de symboles, utilisez la fonction [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) pour définir l’option de chargement différé des symboles ( \_ chargements différés SYMOPT \_ ), puis utilisez la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) ou [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) pour charger les symboles différés pour tous les modules.</span><span class="sxs-lookup"><span data-stu-id="83473-104">To conserve time and memory when working with many symbol files, use the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to set the deferred symbol loading (SYMOPT\_DEFERRED\_LOADS) option, then use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function to load symbols deferred for all modules.</span></span> <span data-ttu-id="83473-105">Le gestionnaire de symboles répertorie les symboles qui sont disponibles pour les modules, mais ne mappe pas les informations de débogage en mémoire tant qu’il n’est pas demandé.</span><span class="sxs-lookup"><span data-stu-id="83473-105">The symbol handler will list symbols that are available for the modules, but will not map the debug information into memory until it is requested.</span></span> <span data-ttu-id="83473-106">Il s’agit de la méthode recommandée pour utiliser efficacement les symboles de débogage.</span><span class="sxs-lookup"><span data-stu-id="83473-106">This is the preferred method to efficiently use debugging symbols.</span></span> <span data-ttu-id="83473-107">Toutes les fonctions qui utilisent des symboles sont affectées par le chargement de symboles différés.</span><span class="sxs-lookup"><span data-stu-id="83473-107">All functions that use symbols are affected by deferred symbol loading.</span></span>

 

 



