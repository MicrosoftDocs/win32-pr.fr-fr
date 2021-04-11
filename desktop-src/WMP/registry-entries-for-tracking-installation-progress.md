---
title: Entrées de Registre pour le suivi de la progression de l’installation
description: Entrées de Registre pour le suivi de la progression de l’installation
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player, suivi de la progression de l’installation
- Windows Media Player, suivi de la progression de l’installation
- Lecteur Windows Media, suivi de la progression des installations
- Lecteur Windows Media, registre
- Registre, suivi de la progression de l’installation
- Registre, suivi de la progression de l’installation
- Registre, suivi de la progression des installations
- Registre, paramètres pour le lecteur Windows Media
- suivi de la progression de l’installation
- installation du suivi de la progression
- suivi de la progression des installations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3add1d2feb668ee90418704b9a11b0072530f120
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029842"
---
# <a name="registry-entries-for-tracking-installation-progress"></a><span data-ttu-id="e7eec-114">Entrées de Registre pour le suivi de la progression de l’installation</span><span class="sxs-lookup"><span data-stu-id="e7eec-114">Registry Entries for Tracking Installation Progress</span></span>

<span data-ttu-id="e7eec-115">Le programme d’installation de Windows Media Player 11, Setup \_wm.exe, écrit les entrées suivantes dans le registre afin que les programmes d’installation puissent suivre la progression du programme d’installation du lecteur Windows Media lors de son exécution.</span><span class="sxs-lookup"><span data-stu-id="e7eec-115">The Windows Media Player 11 setup program, setup\_wm.exe, writes the following entries in the registry so that installation programs can track the progress of the Windows Media Player setup program as it runs.</span></span>


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



<span data-ttu-id="e7eec-116">Dans la syntaxe précédente du Registre, la *valeur* est un espace réservé pour une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="e7eec-116">In the preceding registry syntax, *value* is a placeholder for an integer value.</span></span>

<span data-ttu-id="e7eec-117">Progress \_ CurrentDialog indique la boîte de dialogue que le programme d’installation du lecteur Windows Media affiche actuellement.</span><span class="sxs-lookup"><span data-stu-id="e7eec-117">Progress\_CurrentDialog indicates which dialog box Windows Media Player setup is currently displaying.</span></span> <span data-ttu-id="e7eec-118">Progress \_ MaxDialog indique le nombre total de boîtes de dialogue affichées par Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e7eec-118">Progress\_MaxDialog indicates the total number of dialog boxes that Windows Media will display.</span></span> <span data-ttu-id="e7eec-119">Par exemple, si Progress \_ CurrentDialog = 2 et Progress \_ MaxDialog = 5, le lecteur Windows Media affiche actuellement la deuxième boîte de dialogue dans une séquence de cinq.</span><span class="sxs-lookup"><span data-stu-id="e7eec-119">For example, if Progress\_CurrentDialog = 2 and Progress\_MaxDialog = 5, Windows Media Player is currently displaying the second dialog box in a sequence of five.</span></span>

<span data-ttu-id="e7eec-120">Progress \_ CurrentInstall et Progress \_ MaxInstall, pris ensemble, indiquent le pourcentage d’achèvement de la boîte de dialogue active.</span><span class="sxs-lookup"><span data-stu-id="e7eec-120">Progress\_CurrentInstall and Progress\_MaxInstall, taken together, indicate the percent of completion of the current dialog.</span></span> <span data-ttu-id="e7eec-121">Par exemple, si Progress \_ CurrentInstall = 6 et Progress \_ MaxInstall = 25, la boîte de dialogue actuelle est 6/25 (c’est-à-dire 24%) Remplissez.</span><span class="sxs-lookup"><span data-stu-id="e7eec-121">For example, if Progress\_CurrentInstall = 6 and Progress\_MaxInstall = 25, the current dialog is 6/25 (that is, 24%) complete.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7eec-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e7eec-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7eec-123">**Paramètres du Registre**</span><span class="sxs-lookup"><span data-stu-id="e7eec-123">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




