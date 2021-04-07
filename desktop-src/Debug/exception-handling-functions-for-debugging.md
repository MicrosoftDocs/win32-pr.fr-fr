---
description: Quand une exception se produit dans un processus en cours de débogage, le système notifie le débogueur en lui passant l’exception. C’est ce que l’on appelle une notification de première chance. Le système suspend ensuite tous les threads du processus en cours de débogage.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Fonctions de gestion des exceptions pour le débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846933"
---
# <a name="exception-handling-functions-for-debugging"></a><span data-ttu-id="a2d94-105">Fonctions de gestion des exceptions pour le débogage</span><span class="sxs-lookup"><span data-stu-id="a2d94-105">Exception Handling Functions for Debugging</span></span>

<span data-ttu-id="a2d94-106">Quand une exception se produit dans un processus en cours de débogage, le système notifie le débogueur en lui passant l’exception.</span><span class="sxs-lookup"><span data-stu-id="a2d94-106">When an exception occurs in a process that is being debugged, the system notifies the debugger by passing the exception to it.</span></span> <span data-ttu-id="a2d94-107">C’est ce que l’on appelle *une notification de première chance*.</span><span class="sxs-lookup"><span data-stu-id="a2d94-107">This is known as *first-chance notification*.</span></span> <span data-ttu-id="a2d94-108">Le système suspend ensuite tous les threads du processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="a2d94-108">The system then suspends all threads in the process being debugged.</span></span>

<span data-ttu-id="a2d94-109">Si le débogueur ne gère pas l’exception, le système tente de localiser un gestionnaire d’exceptions approprié.</span><span class="sxs-lookup"><span data-stu-id="a2d94-109">If the debugger does not handle the exception, the system attempts to locate an appropriate exception handler.</span></span> <span data-ttu-id="a2d94-110">Si le système ne parvient pas à localiser un ordinateur approprié, le système informe à nouveau le débogueur qu’une exception s’est produite.</span><span class="sxs-lookup"><span data-stu-id="a2d94-110">If the system cannot locate an appropriate one, the system again notifies the debugger that an exception has occurred.</span></span> <span data-ttu-id="a2d94-111">C’est ce que l’on appelle la « *notification de dernière chance »*.</span><span class="sxs-lookup"><span data-stu-id="a2d94-111">This is known as *last-chance notification*.</span></span> <span data-ttu-id="a2d94-112">Si le débogueur ne gère pas l’exception après la dernière notification de chance, le système met fin au processus en cours de débogage.</span><span class="sxs-lookup"><span data-stu-id="a2d94-112">If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.</span></span>

<span data-ttu-id="a2d94-113">Pour plus d’informations, consultez [gestion des exceptions du débogueur](debugger-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="a2d94-113">For more information, see [Debugger Exception Handling](debugger-exception-handling.md).</span></span>

 

 



