---
description: Génération de filtres DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Génération de filtres DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7090eed702b1abe8ee863d5fa3ac9c1fd413690e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908617"
---
# <a name="building-directshow-filters"></a><span data-ttu-id="52a7f-103">Génération de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="52a7f-103">Building DirectShow Filters</span></span>

<span data-ttu-id="52a7f-104">Les classes de base DirectShow sont recommandées pour l’implémentation des filtres DirectShow.</span><span class="sxs-lookup"><span data-stu-id="52a7f-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="52a7f-105">Pour générer avec les classes de base, procédez comme suit, en plus des étapes indiquées dans [configuration de l’environnement de génération](setting-up-the-build-environment.md):</span><span class="sxs-lookup"><span data-stu-id="52a7f-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="52a7f-106">Générez la bibliothèque de classes de base, située dans le répertoire Samples \\ Multimedia \\ DirectShow \\ BaseClasses, sous le répertoire racine du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="52a7f-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="52a7f-107">Il existe deux versions de la bibliothèque : une version commerciale (Strmbase. lib) et une version de débogage (Strmbasd. lib).</span><span class="sxs-lookup"><span data-stu-id="52a7f-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="52a7f-108">Incluez le fichier d’en-tête streams. h.</span><span class="sxs-lookup"><span data-stu-id="52a7f-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="52a7f-109">Utilisez la \_ \_ Convention d’appel StdCall.</span><span class="sxs-lookup"><span data-stu-id="52a7f-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="52a7f-110">Utilisez la bibliothèque Runtime C multithread (Debug ou Retail, le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="52a7f-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="52a7f-111">Incluez un fichier de définition (. def) qui exporte les fonctions DLL.</span><span class="sxs-lookup"><span data-stu-id="52a7f-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="52a7f-112">Voici un exemple de fichier de définition.</span><span class="sxs-lookup"><span data-stu-id="52a7f-112">The following is an example of a definition file.</span></span> <span data-ttu-id="52a7f-113">Il part du principe que le fichier de sortie est nommé MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="52a7f-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="52a7f-114">Lien vers les fichiers lib suivants.</span><span class="sxs-lookup"><span data-stu-id="52a7f-114">Link to the following lib files.</span></span>

| <span data-ttu-id="52a7f-115">Étiquette</span><span class="sxs-lookup"><span data-stu-id="52a7f-115">Label</span></span> | <span data-ttu-id="52a7f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="52a7f-116">Value</span></span> |
    |--------------|--------------------------------------|
    | <span data-ttu-id="52a7f-117">Version Debug</span><span class="sxs-lookup"><span data-stu-id="52a7f-117">Debug Build</span></span>  | <span data-ttu-id="52a7f-118">Strmbasd. lib, msvcrtd. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="52a7f-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="52a7f-119">Version commerciale</span><span class="sxs-lookup"><span data-stu-id="52a7f-119">Retail Build</span></span> | <span data-ttu-id="52a7f-120">Strmbase. lib, msvcrt. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="52a7f-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="52a7f-121">Choisissez l’option « Ignorer les bibliothèques par défaut » dans les paramètres de l’éditeur de liens.</span><span class="sxs-lookup"><span data-stu-id="52a7f-121">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="52a7f-122">Déclarez le point d’entrée de la DLL dans votre code source, comme suit :</span><span class="sxs-lookup"><span data-stu-id="52a7f-122">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="52a7f-123">Versions antérieures</span><span class="sxs-lookup"><span data-stu-id="52a7f-123">Previous Versions</span></span>

<span data-ttu-id="52a7f-124">Pour les versions de la bibliothèque de classes de base antérieures à DirectShow 9,0, vous devez également effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="52a7f-124">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="52a7f-125">Pour les builds de débogage, définissez l’indicateur de préprocesseur DEBUG.</span><span class="sxs-lookup"><span data-stu-id="52a7f-125">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="52a7f-126">Cette étape n’est pas requise pour la version de la bibliothèque de classes de base qui est disponible dans DirectShow 9,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="52a7f-126">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52a7f-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52a7f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52a7f-128">Classes de base DirectShow</span><span class="sxs-lookup"><span data-stu-id="52a7f-128">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="52a7f-129">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="52a7f-129">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



