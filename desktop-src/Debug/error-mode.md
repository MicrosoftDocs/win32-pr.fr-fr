---
description: Le mode d’erreur indique au système Comment l’application va répondre aux erreurs graves.
ms.assetid: 288be838-6094-4824-9cae-99b7ff9eea74
title: Mode d’erreur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75238e7ee64f40950c3df3aba36d28d95c953267
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109978"
---
# <a name="error-mode"></a><span data-ttu-id="56327-103">Mode d’erreur</span><span class="sxs-lookup"><span data-stu-id="56327-103">Error Mode</span></span>

<span data-ttu-id="56327-104">Le mode d’erreur indique au système Comment l’application va répondre aux erreurs graves.</span><span class="sxs-lookup"><span data-stu-id="56327-104">The error mode indicates to the system how the application is going to respond to serious errors.</span></span> <span data-ttu-id="56327-105">Les erreurs graves incluent les défaillances de disque, les erreurs de lecteur non prêt, le mauvais alignement des données et les exceptions non gérées.</span><span class="sxs-lookup"><span data-stu-id="56327-105">Serious errors include disk failure, drive-not-ready errors, data misalignment, and unhandled exceptions.</span></span> <span data-ttu-id="56327-106">Ce mode d’erreur peut être géré par thread ou par processus.</span><span class="sxs-lookup"><span data-stu-id="56327-106">This error mode can be managed by either a per-thread or per-process basis.</span></span> <span data-ttu-id="56327-107">Une application peut permettre au système d’afficher une boîte de message informant l’utilisateur qu’une erreur s’est produite, ou peut gérer les erreurs.</span><span class="sxs-lookup"><span data-stu-id="56327-107">An application can let the system display a message box informing the user that an error has occurred, or it can handle the errors.</span></span>

<span data-ttu-id="56327-108">Pour gérer ces erreurs sans intervention de l’utilisateur, utilisez [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) ou le [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode)spécifique au thread.</span><span class="sxs-lookup"><span data-stu-id="56327-108">To handle these errors without user intervention, use [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) or the thread-specific [**SetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setthreaderrormode).</span></span> <span data-ttu-id="56327-109">Après l’appel de l’une de ces fonctions et la spécification des indicateurs appropriés, le système n’affichera pas les boîtes de message d’erreur correspondantes.</span><span class="sxs-lookup"><span data-stu-id="56327-109">After calling one of these functions and specifying appropriate flags, the system will not display the corresponding error message boxes.</span></span>

<span data-ttu-id="56327-110">Un processus peut récupérer son mode d’erreur à l’aide de [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) ou [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span><span class="sxs-lookup"><span data-stu-id="56327-110">A process can retrieve its error mode using [**GetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-geterrormode) or [**GetThreadErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getthreaderrormode).</span></span>

<span data-ttu-id="56327-111">La meilleure pratique est que toutes les applications appellent la fonction [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) à l’ensemble du processus avec un paramètre de **SEM \_ FAILCRITICALERRORS** au démarrage.</span><span class="sxs-lookup"><span data-stu-id="56327-111">Best practice is that all applications call the process-wide [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with a parameter of **SEM\_FAILCRITICALERRORS** at startup.</span></span> <span data-ttu-id="56327-112">Cela permet d’empêcher les boîtes de dialogue du mode d’erreur de suspendre l’application.</span><span class="sxs-lookup"><span data-stu-id="56327-112">This is to prevent error mode dialogs from hanging the application.</span></span>

<span data-ttu-id="56327-113">À part cela, les appelants doivent privilégier les versions spécifiques aux threads de ces fonctions, car elles sont moins perturbatrices pour le comportement normal du système.</span><span class="sxs-lookup"><span data-stu-id="56327-113">Other than that, callers should favor the thread-specific versions of these functions since they are less disruptive to the normal behavior of the system.</span></span>

 

 
