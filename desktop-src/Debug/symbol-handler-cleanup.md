---
description: Pour libérer toute la mémoire utilisée par le gestionnaire de symboles pour un processus, utilisez la fonction SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Nettoyage du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860925"
---
# <a name="symbol-handler-cleanup"></a><span data-ttu-id="3fe38-103">Nettoyage du gestionnaire de symboles</span><span class="sxs-lookup"><span data-stu-id="3fe38-103">Symbol Handler Cleanup</span></span>

<span data-ttu-id="3fe38-104">Pour libérer toute la mémoire utilisée par le gestionnaire de symboles pour un processus, utilisez la fonction [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) .</span><span class="sxs-lookup"><span data-stu-id="3fe38-104">To free all the memory used by the symbol handler for a process, use the [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) function.</span></span> <span data-ttu-id="3fe38-105">Cette fonction énumère tous les modules chargés, libère chaque module et libère la mémoire allouée pour la liste de modules.</span><span class="sxs-lookup"><span data-stu-id="3fe38-105">This function enumerates all loaded modules, frees each module, and frees the memory allocated for the list of modules.</span></span> <span data-ttu-id="3fe38-106">Après avoir appelé **SymCleanup**, vous ne pouvez pas utiliser le handle de processus dans les fonctions de gestion de symboles tant que vous n’avez pas appelé la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="3fe38-106">After you call **SymCleanup**, you cannot use the process handle in the symbol handling functions until you call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

 

 



