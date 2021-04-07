---
description: Génération de filtres DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Génération de filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5553c4358f97809214ebbdea23c129aa7c214e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747069"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="1b113-103">Génération de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b113-103">Building DirectShow Filters</span></span>

<span data-ttu-id="1b113-104">Les classes de base DirectShow sont recommandées pour l’implémentation des filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1b113-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="1b113-105">Pour générer avec les classes de base, procédez comme suit, en plus des étapes indiquées dans [configuration de l’environnement de génération](setting-up-the-build-environment.md):</span><span class="sxs-lookup"><span data-stu-id="1b113-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="1b113-106">Générez la bibliothèque de classes de base, située dans le répertoire Samples \\ Multimedia \\ DirectShow \\ BaseClasses, sous le répertoire racine du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="1b113-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="1b113-107">Il existe deux versions de la bibliothèque : une version commerciale (Strmbase. lib) et une version de débogage (Strmbasd. lib).</span><span class="sxs-lookup"><span data-stu-id="1b113-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="1b113-108">Incluez le fichier d’en-tête streams. h.</span><span class="sxs-lookup"><span data-stu-id="1b113-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="1b113-109">Utilisez la \_ \_ Convention d’appel StdCall.</span><span class="sxs-lookup"><span data-stu-id="1b113-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="1b113-110">Utilisez la bibliothèque Runtime C multithread (Debug ou Retail, le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="1b113-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="1b113-111">Incluez un fichier de définition (. def) qui exporte les fonctions DLL.</span><span class="sxs-lookup"><span data-stu-id="1b113-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="1b113-112">Voici un exemple de fichier de définition.</span><span class="sxs-lookup"><span data-stu-id="1b113-112">The following is an example of a definition file.</span></span> <span data-ttu-id="1b113-113">Il part du principe que le fichier de sortie est nommé MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="1b113-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="1b113-114">Lien vers les fichiers lib suivants.</span><span class="sxs-lookup"><span data-stu-id="1b113-114">Link to the following lib files.</span></span>

    |              |                                      |
    |--------------|--------------------------------------|
    | <span data-ttu-id="1b113-115">Version Debug</span><span class="sxs-lookup"><span data-stu-id="1b113-115">Debug Build</span></span>  | <span data-ttu-id="1b113-116">Strmbasd. lib, msvcrtd. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="1b113-116">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="1b113-117">Version commerciale</span><span class="sxs-lookup"><span data-stu-id="1b113-117">Retail Build</span></span> | <span data-ttu-id="1b113-118">Strmbase. lib, msvcrt. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="1b113-118">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="1b113-119">Choisissez l’option « Ignorer les bibliothèques par défaut » dans les paramètres de l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="1b113-119">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="1b113-120">Déclarez le point d’entrée de la DLL dans votre code source, comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b113-120">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="1b113-121">Versions antérieures</span><span class="sxs-lookup"><span data-stu-id="1b113-121">Previous Versions</span></span>

<span data-ttu-id="1b113-122">Pour les versions de la bibliothèque de classes de base antérieures à DirectShow 9,0, vous devez également effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="1b113-122">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="1b113-123">Pour les builds de débogage, définissez l’indicateur de préprocesseur DEBUG.</span><span class="sxs-lookup"><span data-stu-id="1b113-123">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="1b113-124">Cette étape n’est pas requise pour la version de la bibliothèque de classes de base qui est disponible dans DirectShow 9,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1b113-124">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b113-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b113-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b113-126">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b113-126">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="1b113-127">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="1b113-127">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



