---
description: Les termes suivants sont utilisés lors de la description du débogage.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminologie du débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950385"
---
# <a name="debugging-terminology"></a><span data-ttu-id="40359-103">Terminologie du débogage</span><span class="sxs-lookup"><span data-stu-id="40359-103">Debugging Terminology</span></span>

<span data-ttu-id="40359-104">Les termes suivants sont utilisés lors de la description du débogage.</span><span class="sxs-lookup"><span data-stu-id="40359-104">The following terms are used when describing debugging.</span></span>

<dl> <dt>

<span data-ttu-id="40359-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Écran bleu</span><span class="sxs-lookup"><span data-stu-id="40359-105"><span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blue screen</span></span>
</dt> <dd>

<span data-ttu-id="40359-106">Lorsque le système rencontre un problème matériel, une incohérence des données ou une erreur similaire, il peut afficher un écran bleu contenant des informations qui peuvent être utilisées pour déterminer la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="40359-106">When the system encounters a hardware problem, data inconsistency, or similar error, it may display a blue screen containing information that can be used to determine the cause of the error.</span></span> <span data-ttu-id="40359-107">Ces informations incluent le code d’arrêt et indiquent si un fichier de vidage sur incident a été créé.</span><span class="sxs-lookup"><span data-stu-id="40359-107">This information includes the STOP code and whether a crash dump file was created.</span></span> <span data-ttu-id="40359-108">Elle peut également inclure une liste des pilotes chargés et une trace de la pile.</span><span class="sxs-lookup"><span data-stu-id="40359-108">It may also include a list of loaded drivers and a stack trace.</span></span>

</dd> <dt>

<span data-ttu-id="40359-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Fichier de vidage sur incident</span><span class="sxs-lookup"><span data-stu-id="40359-109"><span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Crash dump file</span></span>
</dt> <dd>

<span data-ttu-id="40359-110">Vous pouvez configurer le système pour écrire des informations dans un fichier de vidage sur incident sur votre disque dur à chaque fois qu’un code d’arrêt est généré.</span><span class="sxs-lookup"><span data-stu-id="40359-110">You can configure the system to write information to a crash dump file on your hard disk whenever a STOP code is generated.</span></span> <span data-ttu-id="40359-111">Le fichier contient des informations que le débogueur peut utiliser pour analyser l’erreur.</span><span class="sxs-lookup"><span data-stu-id="40359-111">The file contains information the debugger can use to analyze the error.</span></span> <span data-ttu-id="40359-112">Ce fichier peut être aussi volumineux que la mémoire physique contenue dans l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="40359-112">This file can be as big as the physical memory contained in the computer.</span></span>

</dd> <dt>

<span data-ttu-id="40359-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Débogueur</span><span class="sxs-lookup"><span data-stu-id="40359-113"><span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger</span></span>
</dt> <dd>

<span data-ttu-id="40359-114">Programme conçu pour aider à détecter, localiser et corriger les erreurs dans un autre programme.</span><span class="sxs-lookup"><span data-stu-id="40359-114">A program designed to help detect, locate, and correct errors in another program.</span></span> <span data-ttu-id="40359-115">Elle permet au développeur de parcourir l’exécution du processus et de ses threads, d’analyser la mémoire, les variables et d’autres éléments de processus et de contexte de thread.</span><span class="sxs-lookup"><span data-stu-id="40359-115">It allows the developer to step through the execution of the process and its threads, monitoring memory, variables, and other elements of process and thread context.</span></span>

</dd> <dt>

<span data-ttu-id="40359-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Mode noyau</span><span class="sxs-lookup"><span data-stu-id="40359-116"><span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel mode</span></span>
</dt> <dd>

<span data-ttu-id="40359-117">Mode de processeur dans lequel s’exécutent les services système et les pilotes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="40359-117">The processor mode in which system services and device drivers run.</span></span> <span data-ttu-id="40359-118">Toutes les interfaces et instructions de l’UC sont disponibles, et toute la mémoire est accessible.</span><span class="sxs-lookup"><span data-stu-id="40359-118">All interfaces and CPU instructions are available, and all memory is accessible.</span></span>

</dd> <dt>

<span data-ttu-id="40359-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Fichier minidump</span><span class="sxs-lookup"><span data-stu-id="40359-119"><span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump file</span></span>
</dt> <dd>

<span data-ttu-id="40359-120">Les applications peuvent produire des fichiers Minidump en mode utilisateur, qui contiennent un sous-ensemble utile des informations contenues dans un fichier de vidage sur incident.</span><span class="sxs-lookup"><span data-stu-id="40359-120">Applications can produce user-mode minidump files, which contain a useful subset of the information contained in a crash dump file.</span></span> <span data-ttu-id="40359-121">Pour plus d’informations, consultez [fichiers Minidump](minidump-files.md).</span><span class="sxs-lookup"><span data-stu-id="40359-121">For more information, see [Minidump Files](minidump-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="40359-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>ARRÊTER le code</span><span class="sxs-lookup"><span data-stu-id="40359-122"><span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP code</span></span>
</dt> <dd>

<span data-ttu-id="40359-123">Code d’erreur qui identifie l’erreur qui a empêché le noyau du système de continuer à s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="40359-123">The error code that identifies the error that stopped the system kernel from continuing to run.</span></span>

</dd> <dt>

<span data-ttu-id="40359-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Fichiers de symboles</span><span class="sxs-lookup"><span data-stu-id="40359-124"><span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol files</span></span>
</dt> <dd>

<span data-ttu-id="40359-125">Toutes les applications système, tous les pilotes et toutes les dll sont générés de sorte que leurs informations de débogage se trouvent dans des fichiers distincts appelés fichiers de symboles.</span><span class="sxs-lookup"><span data-stu-id="40359-125">All system applications, drivers, and DLLs are built such that their debugging information resides in separate files known as symbol files.</span></span> <span data-ttu-id="40359-126">Par conséquent, le système est plus petit et plus rapide, mais il peut toujours être débogué si les fichiers de symboles sont installés.</span><span class="sxs-lookup"><span data-stu-id="40359-126">Therefore, the system is smaller and faster, yet it can still be debugged if the symbol files are installed.</span></span> <span data-ttu-id="40359-127">Pour plus d’informations, consultez [fichiers de symboles](symbol-files.md).</span><span class="sxs-lookup"><span data-stu-id="40359-127">For more information, see [Symbol Files](symbol-files.md).</span></span>

</dd> <dt>

<span data-ttu-id="40359-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Mode utilisateur</span><span class="sxs-lookup"><span data-stu-id="40359-128"><span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>User mode</span></span>
</dt> <dd>

<span data-ttu-id="40359-129">Mode de processeur dans lequel les applications s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="40359-129">The processor mode in which applications run.</span></span> <span data-ttu-id="40359-130">Un ensemble limité d’interfaces est disponible dans ce mode, et l’accès aux données système est limité.</span><span class="sxs-lookup"><span data-stu-id="40359-130">A limited set of interfaces are available in this mode, and access to system data is limited.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="40359-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40359-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40359-132">Configuration du débogage automatique</span><span class="sxs-lookup"><span data-stu-id="40359-132">Configuring Automatic Debugging</span></span>](configuring-automatic-debugging.md)
</dt> </dl>

 

 



