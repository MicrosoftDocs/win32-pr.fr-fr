---
title: Erreurs d’alignement
description: Erreurs d’alignement
ms.assetid: 16e69aec-3aec-4684-bf37-b3e5db6e4f87
keywords:
- Erreurs d’alignement 64-programmation Windows bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318a7a55010ac148354d000ece32c91a8652f821
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510698"
---
# <a name="alignment-faults"></a><span data-ttu-id="87040-104">Erreurs d’alignement</span><span class="sxs-lookup"><span data-stu-id="87040-104">Alignment Faults</span></span>

<span data-ttu-id="87040-105">Le gestionnaire d’erreurs d’alignement système est désactivé par défaut sur les systèmes basés sur Itanium.</span><span class="sxs-lookup"><span data-stu-id="87040-105">The system alignment-fault handler is turned off by default on Itanium-based systems.</span></span> <span data-ttu-id="87040-106">Par conséquent, tout accès aux données non alignées génère une exception qui ne sera pas automatiquement corrigée par le système, à moins que l’application n’intercepte l’exception dans un [Gestionnaire d’exceptions basé sur des frames](/windows/desktop/Debug/frame-based-exception-handling).</span><span class="sxs-lookup"><span data-stu-id="87040-106">Therefore, any unaligned data access generates an exception that will not automatically be fixed by the system unless the application catches the exception in a [frame-based exception handler](/windows/desktop/Debug/frame-based-exception-handling).</span></span> <span data-ttu-id="87040-107">Pour activer le gestionnaire d’erreurs d’alignement du système, appelez la fonction [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) avec **SEM \_ NOALIGNMENTFAULTEXCEPT**.</span><span class="sxs-lookup"><span data-stu-id="87040-107">To enable the system alignment-fault hander, call the [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) function with **SEM\_NOALIGNMENTFAULTEXCEPT**.</span></span> <span data-ttu-id="87040-108">Toutefois, Notez que les processus peuvent subir une dégradation importante des performances si le gestionnaire d’erreurs d’alignement du système est activé et que le processus génère des erreurs d’alignement.</span><span class="sxs-lookup"><span data-stu-id="87040-108">However, note that processes may experience severe performance degradation if the system alignment-fault handler is enabled and the process generates alignment faults.</span></span>

<span data-ttu-id="87040-109">Si le débogueur WinDbg a été installé en tant que débogueur système, WinDbg est lancé automatiquement si un processus sur le système génère une exception non gérée.</span><span class="sxs-lookup"><span data-stu-id="87040-109">If the WinDbg debugger has been installed as the system debugger, WinDbg will automatically be launched if any process on the system generates an unhandled exception.</span></span> <span data-ttu-id="87040-110">Si un débogueur n’est pas installé en tant que débogueur système, le système affiche une boîte de dialogue indiquant que votre application a rencontré une erreur et a fourni la possibilité de signaler le problème à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="87040-110">If you do not have a debugger installed as your system debugger, the system displays a dialog box stating that your application has encountered an error and providing the opportunity to report the problem to Microsoft.</span></span>

<span data-ttu-id="87040-111">Sur les systèmes x64 et ARM64, les erreurs d’alignement sont gérées par une combinaison de matériel et de logiciels.</span><span class="sxs-lookup"><span data-stu-id="87040-111">On x64 and ARM64 systems, any alignment faults are handled by a combination of hardware and software.</span></span> <span data-ttu-id="87040-112">Pour des performances optimales, tout accès à la mémoire doit être correctement aligné.</span><span class="sxs-lookup"><span data-stu-id="87040-112">For best performance, all access to memory should be properly aligned.</span></span> <span data-ttu-id="87040-113">En outre, [l’accès aux variables bloquées](/windows/desktop/Sync/interlocked-variable-access) non alignées doit être évité sur ARM64, car ces opérations ne sont pas atomiques.</span><span class="sxs-lookup"><span data-stu-id="87040-113">In addition, unaligned [interlocked variable access](/windows/desktop/Sync/interlocked-variable-access) should be avoided on ARM64, as these operations are not atomic-safe.</span></span>

 

 