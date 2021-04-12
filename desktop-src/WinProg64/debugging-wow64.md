---
title: Débogage de WOW64
description: Les applications qui s’exécutent sous WOW64 peuvent être déboguées à l’aide d’un débogueur hébergé par x86 ou d’un débogueur natif.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64 bits, programmation Windows, débogage
- débogage de la programmation Windows WOW64 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382584"
---
# <a name="debugging-wow64"></a><span data-ttu-id="c7315-105">Débogage de WOW64</span><span class="sxs-lookup"><span data-stu-id="c7315-105">Debugging WOW64</span></span>

<span data-ttu-id="c7315-106">Les applications qui s’exécutent sous WOW64 peuvent être déboguées de deux manières :</span><span class="sxs-lookup"><span data-stu-id="c7315-106">Applications running under WOW64 can be debugged two ways:</span></span>

-   <span data-ttu-id="c7315-107">Utilisez un débogueur hébergé sur x86, tel que NTSD, WinDbg ou Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c7315-107">Use an x86-hosted debugger such as NTSD, WinDbg, or Visual Studio.</span></span> <span data-ttu-id="c7315-108">Le NTSD 32 bits est installé dans% SystemRoot% \\ SysWOW64 sur les installations de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="c7315-108">The 32-bit NTSD is installed to %systemroot%\\syswow64 on retail installations.</span></span> <span data-ttu-id="c7315-109">Notez que les débogueurs x86 peuvent être utilisés pour déboguer du code x86, mais ne peuvent pas être utilisés pour désassembler ou définir des points d’arrêt dans la couche du thunk WOW64, car il s’agit d’un code natif 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c7315-109">Note that x86 debuggers can be used to debug x86 code, but cannot be used to disassemble or set breakpoints within the WOW64 thunk layer because it is 64-bit native code.</span></span>
-   <span data-ttu-id="c7315-110">Utilisez un débogueur natif tel que CDB, NTSD ou WinDbg et l’extension de débogueur WOW64, Wow64exts.dll.</span><span class="sxs-lookup"><span data-stu-id="c7315-110">Use a native debugger such as CDB, NTSD, or WinDbg and the WOW64 debugger extension, Wow64exts.dll.</span></span> <span data-ttu-id="c7315-111">Si le débogueur natif s’arrête alors que le processeur est en mode x86, le débogueur présente le processus en tant que processus x86.</span><span class="sxs-lookup"><span data-stu-id="c7315-111">If the native debugger breaks while the processor is in x86 mode, the debugger presents the process as an x86 process.</span></span> <span data-ttu-id="c7315-112">Si le processeur est en mode natif, le débogueur présente le processus comme natif.</span><span class="sxs-lookup"><span data-stu-id="c7315-112">If the processor is in native mode, the debugger presents the process as native.</span></span>

<span data-ttu-id="c7315-113">CDB, NTSD et WinDbg sont inclus dans les outils de débogage pour Windows.</span><span class="sxs-lookup"><span data-stu-id="c7315-113">CDB, NTSD, and WinDbg are included in Debugging Tools for Windows.</span></span> <span data-ttu-id="c7315-114">Pour plus d’informations, consultez la documentation [sur les outils de débogage pour Windows](/windows-hardware/drivers/debugger/) .</span><span class="sxs-lookup"><span data-stu-id="c7315-114">For more information, see the [Debugging Tools for Windows](/windows-hardware/drivers/debugger/) documentation.</span></span>

<span data-ttu-id="c7315-115">L’extension du débogueur Wow64exts est installée avec WinDbg.</span><span class="sxs-lookup"><span data-stu-id="c7315-115">The Wow64exts debugger extension is installed with WinDbg.</span></span> <span data-ttu-id="c7315-116">Utilisez la commande ! Load wow64exts pour charger l’extension du débogueur.</span><span class="sxs-lookup"><span data-stu-id="c7315-116">Use the !load wow64exts command to load the debugger extension.</span></span> <span data-ttu-id="c7315-117">Le tableau suivant répertorie les commandes d’extension du débogueur ! wow64exts.</span><span class="sxs-lookup"><span data-stu-id="c7315-117">The following table lists the !wow64exts debugger extension commands.</span></span>



| <span data-ttu-id="c7315-118">Commande</span><span class="sxs-lookup"><span data-stu-id="c7315-118">Command</span></span>                | <span data-ttu-id="c7315-119">Description</span><span class="sxs-lookup"><span data-stu-id="c7315-119">Description</span></span>                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7315-120">! wow64exts. SW</span><span class="sxs-lookup"><span data-stu-id="c7315-120">!wow64exts.sw</span></span>          | <span data-ttu-id="c7315-121">Bascule entre le mode x86 et le mode natif.</span><span class="sxs-lookup"><span data-stu-id="c7315-121">Switches between x86 and native mode.</span></span>                                                                                                    |
| <span data-ttu-id="c7315-122">! wow64exts. k *Count*</span><span class="sxs-lookup"><span data-stu-id="c7315-122">!wow64exts.k *count*</span></span>   | <span data-ttu-id="c7315-123">Vide une trace de la pile 32 bits/64 bits combinée.</span><span class="sxs-lookup"><span data-stu-id="c7315-123">Dumps a combined 32-bit/64-bit stack trace.</span></span> <span data-ttu-id="c7315-124">Si *Count* est spécifié, la commande vide *les premières adresses* de chaque trace de la pile.</span><span class="sxs-lookup"><span data-stu-id="c7315-124">If *count* is specified, the command dumps the first *count* addresses in each stack trace.</span></span>  |
| <span data-ttu-id="c7315-125">! wow64exts.info</span><span class="sxs-lookup"><span data-stu-id="c7315-125">!wow64exts.info</span></span>        | <span data-ttu-id="c7315-126">Vide les informations de base sur le PEB du processus, le TEB du thread actuel et les emplacements de stockage local des threads (TLS) utilisés par WOW64.</span><span class="sxs-lookup"><span data-stu-id="c7315-126">Dumps basic information about the PEB of the process, the TEB of the current thread, and thread local storage (TLS) slots used by WOW64.</span></span> |
| <span data-ttu-id="c7315-127">! wow64exts. r *adresse*</span><span class="sxs-lookup"><span data-stu-id="c7315-127">!wow64exts.r *address*</span></span> | <span data-ttu-id="c7315-128">Fait un dump du contexte pour l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c7315-128">Dumps context for the specified address.</span></span> <span data-ttu-id="c7315-129">Si *Address* n’est pas spécifié, la commande vide le contexte pour le processeur.</span><span class="sxs-lookup"><span data-stu-id="c7315-129">If *address* is not specified, the command dumps context for the processor.</span></span>                     |



 

 

 