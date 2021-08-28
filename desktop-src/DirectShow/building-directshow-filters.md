---
description: génération de filtres de DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: génération de filtres de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d1983d3bfd42d1a1582ef696b6793acdd0856dde2bd2d589e809acc614314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794320"
---
# <a name="building-directshow-filters"></a>génération de filtres de DirectShow

les classes de base DirectShow sont recommandées pour implémenter des filtres de DirectShow. Pour générer avec les classes de base, procédez comme suit, en plus des étapes indiquées dans [configuration de l’environnement de génération](setting-up-the-build-environment.md):

-   générez la bibliothèque de classes de base, située dans le répertoire samples \\ Multimedia \\ DirectShow \\ BaseClasses, sous le répertoire racine du kit de développement logiciel (SDK). Il existe deux versions de la bibliothèque : une version commerciale (Strmbase. lib) et une version de débogage (Strmbasd. lib).
-   incluez le fichier d’en-tête Flux. h.
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

| Étiquette | Valeur |
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

    

Versions précédentes

pour les versions de la bibliothèque de classes de base antérieures DirectShow 9,0, vous devez également effectuer les opérations suivantes :

-   Pour les builds de débogage, définissez l’indicateur de préprocesseur DEBUG.

cette étape n’est pas requise pour la version de la bibliothèque de classes de base disponible dans DirectShow 9,0 et versions ultérieures.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Classes de base](directshow-base-classes.md)
</dt> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



