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
# <a name="building-directshow-filters"></a>Génération de filtres DirectShow

Les classes de base DirectShow sont recommandées pour l’implémentation des filtres DirectShow. Pour générer avec les classes de base, procédez comme suit, en plus des étapes indiquées dans [configuration de l’environnement de génération](setting-up-the-build-environment.md):

-   Générez la bibliothèque de classes de base, située dans le répertoire Samples \\ Multimedia \\ DirectShow \\ BaseClasses, sous le répertoire racine du kit de développement logiciel (SDK). Il existe deux versions de la bibliothèque : une version commerciale (Strmbase. lib) et une version de débogage (Strmbasd. lib).
-   Incluez le fichier d’en-tête streams. h.
-   Utilisez la \_ \_ Convention d’appel StdCall.
-   Utilisez la bibliothèque Runtime C multithread (Debug ou Retail, le cas échéant).
-   Incluez un fichier de définition (. def) qui exporte les fonctions DLL. Voici un exemple de fichier de définition. Il part du principe que le fichier de sortie est nommé MyFilter.dll.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Lien vers les fichiers lib suivants.

    |              |                                      |
    |--------------|--------------------------------------|
    | Version Debug  | Strmbasd. lib, msvcrtd. lib, winmm. lib |
    | Version commerciale | Strmbase. lib, msvcrt. lib, winmm. lib  |

    

     

-   Choisissez l’option « Ignorer les bibliothèques par défaut » dans les paramètres de l’éditeur de liens.
-   Déclarez le point d’entrée de la DLL dans votre code source, comme suit :
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Versions antérieures

Pour les versions de la bibliothèque de classes de base antérieures à DirectShow 9,0, vous devez également effectuer les opérations suivantes :

-   Pour les builds de débogage, définissez l’indicateur de préprocesseur DEBUG.

Cette étape n’est pas requise pour la version de la bibliothèque de classes de base qui est disponible dans DirectShow 9,0 et versions ultérieures.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Classes de base DirectShow](directshow-base-classes.md)
</dt> <dt>

[Écriture de filtres DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



