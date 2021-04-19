---
description: Lorsque l’application appelle les fonctions LoadLibrary ou LoadLibraryEx, le système tente de localiser la DLL (pour plus d’informations, consultez l’ordre de recherche de la bibliothèque Dynamic-Link).
ms.assetid: 81e237a9-3c32-46a5-88d3-c978f43dad54
title: Run-Time la liaison dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e215ac83ecdc0615b8030e2e215857c67fe6e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521418"
---
# <a name="run-time-dynamic-linking"></a>Run-Time la liaison dynamique

Lorsque l’application appelle les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , le système tente de localiser la dll (pour plus d’informations, consultez ordre de recherche dans la [bibliothèque de liens dynamiques](dynamic-link-library-search-order.md)). Si la recherche est réussie, le système mappe le module DLL dans l’espace d’adressage virtuel du processus et incrémente le décompte de références. Si l’appel à **LoadLibrary** ou **LoadLibraryEx** spécifie une dll dont le code est déjà mappé dans l’espace d’adressage virtuel du processus appelant, la fonction retourne simplement un handle à la dll et incrémente le nombre de références de dll. Notez que deux dll qui ont les mêmes nom et extension de fichier de base mais se trouvent dans des répertoires différents ne sont pas considérées comme étant la même DLL.

Le système appelle la fonction de point d’entrée dans le contexte du thread qui a appelé [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). La fonction de point d’entrée n’est pas appelée si la DLL a déjà été chargée par le processus par le biais d’un appel à **LoadLibrary** ou **LoadLibraryEx** sans appel correspondant à la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

Si le système ne peut pas trouver la DLL ou si la fonction de point d’entrée retourne FALSe, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) retourne null. Si **LoadLibrary** ou **LoadLibraryEx** parvient à fonctionner, il retourne un handle au module dll. Le processus peut utiliser ce handle pour identifier la DLL dans un appel à la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)ou [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) .

La fonction [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) retourne un handle utilisé dans [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)ou [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). La fonction **GetModuleHandle** ne fonctionne que si le module dll est déjà mappé dans l’espace d’adressage du processus par liaison au moment du chargement ou par un appel précédent à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Contrairement à **LoadLibrary** ou **LoadLibraryEx**, **GetModuleHandle** n’incrémente pas le nombre de références de module. La fonction [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) récupère le chemin d’accès complet du module associé à un handle retourné par **GetModuleHandle**, **LoadLibrary** ou **LoadLibraryEx**.

Le processus peut utiliser [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour obtenir l’adresse d’une fonction exportée dans la dll à l’aide d’un handle de module dll retourné par [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

Lorsque le module DLL n’est plus nécessaire, le processus peut appeler [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) ou [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). Ces fonctions décrémentent le nombre de références de module et annulent le démappage du Code DLL de l’espace d’adressage virtuel du processus si le nombre de références est égal à zéro.

La liaison dynamique au moment de l’exécution permet au processus de continuer à s’exécuter même si aucune DLL n’est disponible. Le processus peut ensuite utiliser une autre méthode pour atteindre son objectif. Par exemple, si un processus ne parvient pas à localiser une seule DLL, il peut essayer d’en utiliser un autre ou notifier l’utilisateur d’une erreur. Si l’utilisateur peut fournir le chemin d’accès complet de la DLL manquante, le processus peut utiliser ces informations pour charger la DLL même si elle ne se trouve pas dans le chemin de recherche normal. Cette situation contraste avec la liaison au moment du chargement, dans laquelle le système arrête simplement le processus s’il ne trouve pas la DLL.

La liaison dynamique au moment de l’exécution peut entraîner des problèmes si la DLL utilise la fonction [**DllMain**](dllmain.md) pour effectuer l’initialisation de chaque thread d’un processus, car le point d’entrée n’est pas appelé pour les threads qui existaient avant l’appel de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Pour obtenir un exemple illustrant la façon de résoudre ce problème, consultez [utilisation du stockage local des threads dans une bibliothèque de Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la liaison dynamique au moment de l’exécution](using-run-time-dynamic-linking.md)
</dt> </dl>

 

 
