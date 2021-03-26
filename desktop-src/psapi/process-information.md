---
title: Informations sur le processus
description: Le système gère une liste des processus en cours d’exécution. Vous pouvez récupérer les identificateurs de ces processus en appelant la fonction EnumProcesses. Cette fonction remplit un tableau de valeurs DWORD avec les identificateurs de tous les processus du système.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315552"
---
# <a name="process-information"></a><span data-ttu-id="63df3-105">Informations sur le processus</span><span class="sxs-lookup"><span data-stu-id="63df3-105">Process Information</span></span>

<span data-ttu-id="63df3-106">Le système gère une liste des processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="63df3-106">The system maintains a list of running processes.</span></span> <span data-ttu-id="63df3-107">Vous pouvez récupérer les identificateurs de ces processus en appelant la fonction [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="63df3-107">You can retrieve the identifiers for these processes by calling the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="63df3-108">Cette fonction remplit un tableau de valeurs **DWORD** avec les identificateurs de tous les processus du système.</span><span class="sxs-lookup"><span data-stu-id="63df3-108">This function fills an array of **DWORD** values with the identifiers of all processes in the system.</span></span>

<span data-ttu-id="63df3-109">De nombreuses fonctions dans PSAPIi requièrent un handle de processus.</span><span class="sxs-lookup"><span data-stu-id="63df3-109">Many functions in PSAPI require a process handle.</span></span> <span data-ttu-id="63df3-110">Pour obtenir un handle de processus pour un processus en cours d’exécution, transmettez son identificateur de processus (obtenu à partir de [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) à la fonction [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) .</span><span class="sxs-lookup"><span data-stu-id="63df3-110">To obtain a process handle for a running process, pass its process identifier (obtained from [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) to the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function.</span></span> <span data-ttu-id="63df3-111">N’oubliez pas d’appeler la fonction [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) lorsque vous avez terminé avec le handle de processus.</span><span class="sxs-lookup"><span data-stu-id="63df3-111">Remember to call the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function when you are finished with the process handle.</span></span>

 

 