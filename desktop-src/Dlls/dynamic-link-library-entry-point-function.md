---
description: Une DLL peut éventuellement spécifier une fonction de point d’entrée.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Entry-Point fonction de la bibliothèque de Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6289f705a11dad58eca8b047ba469ee07320dedef762024cbfa04046a0677f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815837"
---
# <a name="dynamic-link-library-entry-point-function"></a>Entry-Point fonction de la bibliothèque de Dynamic-Link

Une DLL peut éventuellement spécifier une fonction de point d’entrée. Si elle est présente, le système appelle la fonction de point d’entrée chaque fois qu’un processus ou un thread charge ou décharge la DLL. Il peut être utilisé pour effectuer des tâches d’initialisation et de nettoyage simples. Par exemple, il peut configurer le stockage local des threads lorsqu’un nouveau thread est créé, et le nettoyer lorsque le thread est arrêté.

Si vous liez votre DLL à la bibliothèque Runtime C, elle peut fournir une fonction de point d’entrée pour vous, et vous permettre de fournir une fonction d’initialisation distincte. Pour plus d’informations, consultez la documentation de votre bibliothèque Runtime.

Si vous fournissez votre propre point d’entrée, consultez la fonction [**DllMain**](dllmain.md) . Le nom **DllMain** est un espace réservé pour une fonction définie par l’utilisateur. Vous devez spécifier le nom réel que vous utilisez lorsque vous générez votre DLL. Pour plus d’informations, consultez la documentation fournie avec vos outils de développement.

## <a name="calling-the-entry-point-function"></a>Appel de la fonction Entry-Point

Le système appelle la fonction de point d’entrée chaque fois que l’un des événements suivants se produit :

-   Un processus charge la DLL. Pour les processus utilisant la liaison dynamique au moment du chargement, la DLL est chargée pendant l’initialisation du processus. Pour les processus utilisant la liaison au moment de l’exécution, la DLL est chargée avant le retour de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) .
-   Un processus décharge la DLL. La DLL est déchargée lorsque le processus se termine ou appelle la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) et que le nombre de références est égal à zéro. Si le processus se termine à la suite de la fonction [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) ou [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) , le système n’appelle pas la fonction de point d’entrée dll.
-   Un nouveau thread est créé dans un processus qui a chargé la DLL. Vous pouvez utiliser la fonction [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) pour désactiver la notification lors de la création de threads.
-   Un thread d’un processus qui a chargé la DLL s’arrête normalement, sans utiliser [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) ou [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Lorsqu’un processus décharge la DLL, la fonction de point d’entrée est appelée une seule fois pour l’ensemble du processus, plutôt qu’une fois pour chaque thread existant du processus. Vous pouvez utiliser [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) pour désactiver la notification lorsque les threads sont terminés.

Un seul thread à la fois peut appeler la fonction de point d’entrée.

Le système appelle la fonction de point d’entrée dans le contexte du processus ou du thread qui a provoqué l’appel de la fonction. Cela permet à une DLL d’utiliser sa fonction de point d’entrée pour allouer de la mémoire dans l’espace d’adressage virtuel du processus appelant ou pour ouvrir des handles accessibles au processus. La fonction de point d’entrée peut également allouer de la mémoire qui est privée à un nouveau thread à l’aide du stockage local des threads (TLS). pour plus d’informations sur le stockage local des threads, consultez [thread local Stockage](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Définition de la fonction Entry-Point

La fonction de point d’entrée de DLL doit être déclarée avec la Convention d’appel d’appel standard. Si le point d’entrée de la DLL n’est pas déclaré correctement, la DLL n’est pas chargée et le système affiche un message indiquant que le point d’entrée de la DLL doit être déclaré avec WINAPI.

Dans le corps de la fonction, vous pouvez gérer n’importe quelle combinaison des scénarios suivants dans lesquels le point d’entrée de la DLL a été appelé :

-   Un processus charge la DLL (**\_ \_ attachement du processus dll**).
-   Le processus en cours crée un thread (**\_ \_ attachement de thread dll**).
-   Un thread s’arrête normalement (**\_ \_ détachement de thread dll**).
-   Un processus décharge la DLL (**\_ \_ détachement de processus dll**).

La fonction de point d’entrée doit effectuer uniquement des tâches d’initialisation simples. Elle ne doit pas appeler la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (ou une fonction qui appelle ces fonctions), car cela peut créer des boucles de dépendance dans l’ordre de chargement de la dll. Cela peut entraîner l’utilisation d’une DLL avant l’exécution du code d’initialisation du système. De même, la fonction de point d’entrée ne doit pas appeler la fonction [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (ou une fonction qui appelle **FreeLibrary**) pendant l’arrêt du processus, car cela peut entraîner l’utilisation d’une dll après l’exécution du code d’arrêt du système.

Étant donné que le chargement de Kernel32.dll est garanti dans l’espace d’adressage de processus lorsque la fonction de point d’entrée est appelée, l’appel de fonctions dans Kernel32.dll n’entraîne pas l’utilisation de la DLL avant l’exécution de son code d’initialisation. Par conséquent, la fonction de point d’entrée peut créer des [objets de synchronisation](/windows/desktop/Sync/synchronization-objects) , tels que des sections critiques et des mutex, et utiliser TLS, car ces fonctions se trouvent dans Kernel32.dll. Il n’est pas recommandé d’appeler les fonctions de Registre, par exemple, car elles se trouvent dans Advapi32.dll.

L’appel d’autres fonctions peut entraîner des problèmes difficiles à diagnostiquer. Par exemple, l’appel de fonctions utilisateur, Shell et COM peut provoquer des erreurs de violation d’accès, car certaines fonctions dans leurs dll appellent [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger d’autres composants système. Inversement, l’appel de ces fonctions pendant l’arrêt peut entraîner des erreurs de violation d’accès, car le composant correspondant a peut-être déjà été déchargé ou non initialisé.

L’exemple suivant montre comment structurer la fonction de point d’entrée DLL.

``` syntax
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

## <a name="entry-point-function-return-value"></a>Valeur de retour de la fonction Entry-Point

Quand une fonction de point d’entrée DLL est appelée car un processus est en cours de chargement, la fonction retourne la **valeur true** pour indiquer la réussite. Pour les processus utilisant la liaison au moment du chargement, la valeur de retour **false** entraîne l’échec de l’initialisation du processus et le processus se termine. Pour les processus utilisant la liaison au moment de l’exécution, la valeur de retour FALSe fait que la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) retourne la valeur **null**, ce qui indique un échec. (Le système appelle immédiatement votre fonction de point d’entrée avec le **\_ \_ détachement de processus dll** et décharge la dll.) La valeur de retour de la fonction de point d’entrée est ignorée lorsque la fonction est appelée pour une autre raison.

 

 
