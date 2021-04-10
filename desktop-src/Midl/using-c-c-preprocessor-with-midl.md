---
title: Utilisation du préprocesseur C/C++ avec MIDL
description: Le compilateur MIDL ne prétraite pas les fichiers sources.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL du compilateur MIDL, C-preprocesseur
- MIDL de préprocesseur C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309822"
---
# <a name="using-cc-preprocessor-with-midl"></a><span data-ttu-id="035aa-105">Utilisation du préprocesseur C/C++ avec MIDL</span><span class="sxs-lookup"><span data-stu-id="035aa-105">Using C/C++-Preprocessor with MIDL</span></span>

<span data-ttu-id="035aa-106">Le compilateur MIDL ne prétraite pas les fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="035aa-106">The MIDL compiler does not preprocess source files.</span></span> <span data-ttu-id="035aa-107">Au lieu de cela, le compilateur MIDL utilise un préprocesseur disponible pour préparer le flux d’entrée pour l’analyse.</span><span class="sxs-lookup"><span data-stu-id="035aa-107">Rather, the MIDL compiler uses an available preprocessor to prepare the input stream for parsing.</span></span> <span data-ttu-id="035aa-108">Par défaut, MIDL utilise le préprocesseur pour le compilateur Microsoft C/C++ du même environnement de construction que MIDL.</span><span class="sxs-lookup"><span data-stu-id="035aa-108">By default, MIDL uses the preprocessor for the Microsoft C/C++ compiler from the same building environment as MIDL.</span></span> <span data-ttu-id="035aa-109">L’utilisateur peut indiquer un préprocesseur différent à utiliser par MIDL, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="035aa-109">The user can indicate a different preprocessor to be used by MIDL, if needed.</span></span>

<span data-ttu-id="035aa-110">MIDL génère des exécutions distinctes de préprocesseur pour les fichiers IDL et ACF de niveau supérieur, et pour chaque fichier importé avec la directive d’importation MIDL.</span><span class="sxs-lookup"><span data-stu-id="035aa-110">MIDL spawns separate preprocessor runs for top-level IDL and ACF files, and for each file imported with the MIDL import directive.</span></span> <span data-ttu-id="035aa-111">Les fichiers inclus avec la directive **\# include** sont gérés directement par le préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="035aa-111">Files included with the **\#include** directive are handled by the preprocessor directly.</span></span>

<span data-ttu-id="035aa-112">Les rubriques suivantes décrivent les différents aspects de MIDL-interactions du préprocesseur :</span><span class="sxs-lookup"><span data-stu-id="035aa-112">The following topics describe various aspects of MIDL-preprocessor interactions:</span></span>

-   [<span data-ttu-id="035aa-113">C-Configuration requise pour le préprocesseur pour MIDL</span><span class="sxs-lookup"><span data-stu-id="035aa-113">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
-   [<span data-ttu-id="035aa-114">Vérification des options de préprocesseur</span><span class="sxs-lookup"><span data-stu-id="035aa-114">Verifying Preprocessor Options</span></span>](verifying-preprocessor-options.md)
-   [<span data-ttu-id="035aa-115">Enregistrement de la sortie du préprocesseur</span><span class="sxs-lookup"><span data-stu-id="035aa-115">Saving Preprocessor Output</span></span>](saving-preprocessor-output.md)
-   [<span data-ttu-id="035aa-116">Gestion des \# définitions dans les fichiers IDL</span><span class="sxs-lookup"><span data-stu-id="035aa-116">Dealing with \#defines in IDL Files</span></span>](dealing-with-defines-in-idl-files-2.md)

 

 




