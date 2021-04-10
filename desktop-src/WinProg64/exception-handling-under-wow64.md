---
title: Gestion des exceptions sous WOW64
description: WOW64 utilise des exceptions natives x64, ia64 ou ARM64 comme un transport pour les exceptions x86. Par conséquent, dans une application 32 bits s’exécutant sous WOW64, les exceptions non interceptées se comportent comme des exceptions 64 bits natives.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031720"
---
# <a name="exception-handling-under-wow64"></a><span data-ttu-id="42c3d-104">Gestion des exceptions sous WOW64</span><span class="sxs-lookup"><span data-stu-id="42c3d-104">Exception Handling under WOW64</span></span>

<span data-ttu-id="42c3d-105">WOW64 utilise des exceptions natives x64, ia64 ou ARM64 comme un transport pour les exceptions x86.</span><span class="sxs-lookup"><span data-stu-id="42c3d-105">WOW64 uses native x64, ia64, or ARM64 exceptions as a transport for x86 exceptions.</span></span> <span data-ttu-id="42c3d-106">Par conséquent, dans une application 32 bits s’exécutant sous WOW64, les exceptions non interceptées se comportent comme des exceptions 64 bits natives.</span><span class="sxs-lookup"><span data-stu-id="42c3d-106">Therefore, in a 32-bit application running under WOW64, uncaught exceptions behave like native 64-bit exceptions.</span></span>

<span data-ttu-id="42c3d-107">Dans une application qui s’exécute sur une version 32 bits de Windows, les exceptions non interceptées sont transmises aux gestionnaires d’exceptions de niveau supérieur de l’application, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="42c3d-107">In an application running on a 32-bit version of Windows, uncaught exceptions are passed on to higher-level exception handlers of the application, when available.</span></span> <span data-ttu-id="42c3d-108">Dans la même application 32 bits qui s’exécute sous WOW64, le système peut supprimer les exceptions non interceptées.</span><span class="sxs-lookup"><span data-stu-id="42c3d-108">In the same 32-bit application running under WOW64, the system may suppress uncaught exceptions.</span></span>

<span data-ttu-id="42c3d-109">**Windows Vista, Windows Server 2003 et Windows XP :** Dans la même application 32 bits qui s’exécute sous WOW64, le système appelle les filtres d’exception, mais peut supprimer les exceptions non interceptées sans appeler les gestionnaires associés.</span><span class="sxs-lookup"><span data-stu-id="42c3d-109">**Windows Vista, Windows Server 2003 and Windows XP:** In the same 32-bit application running under WOW64, the system calls the exception filters but may suppress uncaught exceptions without invoking the associated handlers.</span></span> <span data-ttu-id="42c3d-110">Ce comportement a été modifié à partir de Windows Vista avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="42c3d-110">This behavior changed starting with Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="42c3d-111">Pour plus d’informations sur les exceptions non interceptées dans les procédures de fenêtre, consultez la fonction [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="42c3d-111">For more information about uncaught exceptions in window procedures, see the [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

 

 