---
description: Toutes les fonctions, prototypes, structures et constantes sont définis dans le fichier d’en-tête Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Génération et test d’une DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104321794"
---
# <a name="building-and-testing-a-gina-dll"></a><span data-ttu-id="ed6ab-103">Génération et test d’une DLL GINA</span><span class="sxs-lookup"><span data-stu-id="ed6ab-103">Building and Testing a GINA DLL</span></span>

<span data-ttu-id="ed6ab-104">Toutes les fonctions, prototypes, structures et constantes sont définis dans le fichier d’en-tête Winwlx. h.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-104">All functions, prototypes, structures, and constants are defined in the Winwlx.h header file.</span></span>

> [!Note]  
> <span data-ttu-id="ed6ab-105">Les DLL GINA sont ignorées dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="ed6ab-106">Pour tester une dll [*Gina*](/windows/desktop/SecGloss/g-gly) , utilisez le Winlogon.exe à partir d’une version vérifiée du système d’exploitation, qui est disponible avec le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-106">To test a [*GINA*](/windows/desktop/SecGloss/g-gly) DLL, use the Winlogon.exe from a checked version of the operating system, which is available with the Microsoft Windows Driver Development Kit (DDK).</span></span> <span data-ttu-id="ed6ab-107">La version vérifiée de [*Winlogon*](/windows/desktop/SecGloss/w-gly) prend en charge le débogage de Ginas comme suit :</span><span class="sxs-lookup"><span data-stu-id="ed6ab-107">The checked version of [*Winlogon*](/windows/desktop/SecGloss/w-gly) supports debugging GINAs as follows:</span></span>

-   <span data-ttu-id="ed6ab-108">Vous pouvez utiliser la syntaxe suivante pour créer une section dans Win.ini pour spécifier les options de débogage Winlogon.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-108">You can use the following syntax to create a section in Win.ini to specify Winlogon debugging options.</span></span>

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    <span data-ttu-id="ed6ab-109">S’il est spécifié, **logfile** doit contenir le nom complet du fichier qui sera utilisé pour enregistrer les informations de débogage.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-109">If specified, **LogFile** should contain the fully qualified name of the file that will be used to log debugging information.</span></span> <span data-ttu-id="ed6ab-110">Si le fichier n'existe pas, il est créé.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-110">If the file does not exist, it will be created.</span></span>

    <span data-ttu-id="ed6ab-111">Les options **DebugFlags** spécifient les genres d’informations de débogage à écrire dans le fichier journal ou le débogueur.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-111">The **DebugFlags** options specify which kinds of debugging information to write to the log file, or debugger.</span></span> <span data-ttu-id="ed6ab-112">**DebugFlags** peut contenir un ou plusieurs des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-112">**DebugFlags** can contain one or more of the following flags.</span></span>

    

    | <span data-ttu-id="ed6ab-113">Indicateur de débogage</span><span class="sxs-lookup"><span data-stu-id="ed6ab-113">Debugging flag</span></span> | <span data-ttu-id="ed6ab-114">Description</span><span class="sxs-lookup"><span data-stu-id="ed6ab-114">Description</span></span>                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="ed6ab-115">CoolSwitch</span><span class="sxs-lookup"><span data-stu-id="ed6ab-115">CoolSwitch</span></span>     | <span data-ttu-id="ed6ab-116">La combinaison de touches CTRL + ALT + MAJ + TAB entraîne une interruption de débogage dans Winlogon.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-116">The CTRL+ALT+SHIFT+TAB key combination will cause a debug break in Winlogon.</span></span>                                                                                               |
    | <span data-ttu-id="ed6ab-117">Error</span><span class="sxs-lookup"><span data-stu-id="ed6ab-117">Error</span></span>          | <span data-ttu-id="ed6ab-118">Erreurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-118">Print errors.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="ed6ab-119">Init</span><span class="sxs-lookup"><span data-stu-id="ed6ab-119">Init</span></span>           | <span data-ttu-id="ed6ab-120">Affichez les messages d’initialisation et de progression.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-120">Print initialization and progress messages.</span></span>                                                                                                                                |
    | <span data-ttu-id="ed6ab-121">Notifier</span><span class="sxs-lookup"><span data-stu-id="ed6ab-121">Notify</span></span>         | <span data-ttu-id="ed6ab-122">Imprimer les messages du package de notification.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-122">Print notification package messages.</span></span>                                                                                                                                       |
    | <span data-ttu-id="ed6ab-123">SAS</span><span class="sxs-lookup"><span data-stu-id="ed6ab-123">SAS</span></span>            | <span data-ttu-id="ed6ab-124">Imprimer des informations sur les notifications de [*séquence de touches de sécurité*](/windows/desktop/SecGloss/s-gly) (SAS).</span><span class="sxs-lookup"><span data-stu-id="ed6ab-124">Print information about [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) notifications.</span></span> |
    | <span data-ttu-id="ed6ab-125">State</span><span class="sxs-lookup"><span data-stu-id="ed6ab-125">State</span></span>          | <span data-ttu-id="ed6ab-126">Imprimer des messages lorsque Winlogon change d’État.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-126">Print messages when Winlogon changes state.</span></span>                                                                                                                                |
    | <span data-ttu-id="ed6ab-127">Délai d'expiration</span><span class="sxs-lookup"><span data-stu-id="ed6ab-127">Timeout</span></span>        | <span data-ttu-id="ed6ab-128">Imprimer des messages quand une limite de temps est définie ou si une limite de temps est atteinte.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-128">Print messages when a time limit is set or a time limit is reached.</span></span>                                                                                                        |
    | <span data-ttu-id="ed6ab-129">Trace</span><span class="sxs-lookup"><span data-stu-id="ed6ab-129">Trace</span></span>          | <span data-ttu-id="ed6ab-130">Imprimer les informations de trace détaillées.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-130">Print verbose trace information.</span></span>                                                                                                                                           |
    | <span data-ttu-id="ed6ab-131">Avertir</span><span class="sxs-lookup"><span data-stu-id="ed6ab-131">Warn</span></span>           | <span data-ttu-id="ed6ab-132">Afficher les avertissements.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-132">Print warnings.</span></span>                                                                                                                                                            |

    

     

-   <span data-ttu-id="ed6ab-133">Pour démarrer la version vérifiée de Winlogon dans un débogueur, ajoutez l’entrée suivante au registre :</span><span class="sxs-lookup"><span data-stu-id="ed6ab-133">To start the checked version of Winlogon in a debugger, add the following entry to the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> <span data-ttu-id="ed6ab-134">Vous devez utiliser le débogueur symbolique Windows (NTSD) pour déboguer Winlogon.</span><span class="sxs-lookup"><span data-stu-id="ed6ab-134">You must use the Windows symbolic debugger (NTSD) to debug Winlogon.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed6ab-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed6ab-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed6ab-136">Chargement et exécution d’une DLL GINA</span><span class="sxs-lookup"><span data-stu-id="ed6ab-136">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)
</dt> <dt>

[<span data-ttu-id="ed6ab-137">Fonctions d’exportation GINA</span><span class="sxs-lookup"><span data-stu-id="ed6ab-137">GINA Export Functions</span></span>](authentication-functions.md)
</dt> <dt>

[<span data-ttu-id="ed6ab-138">Structures GINA</span><span class="sxs-lookup"><span data-stu-id="ed6ab-138">GINA Structures</span></span>](authentication-structures.md)
</dt> <dt>

[<span data-ttu-id="ed6ab-139">Fonctions GINA des services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="ed6ab-139">Terminal Services GINA Functions</span></span>](terminal-services-gina-functions.md)
</dt> </dl>

 

 
