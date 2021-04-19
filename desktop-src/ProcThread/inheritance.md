---
description: Un processus enfant peut hériter de plusieurs propriétés et ressources de son processus parent.
ms.assetid: c530e723-2d40-4022-a259-dfc650604e44
title: Héritage (processus et threads)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4713fe398360b510fab3c66f5cf74dc07b642dac
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "106513563"
---
# <a name="inheritance"></a>Héritage

Un processus enfant peut hériter de plusieurs propriétés et ressources de son processus parent. Vous pouvez également empêcher un processus enfant d’hériter des propriétés de son processus parent. Les éléments suivants peuvent être hérités :

-   Handles ouverts retournés par la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) . Cela comprend les descripteurs des fichiers, les mémoires tampons d’entrée de la console, les mémoires tampons d’écran de la console, les canaux nommés, les périphériques de communication série et les mailslots.
-   Handles ouverts pour traiter, thread, mutex, événement, sémaphore, canal nommé, canal anonyme et objets de mappage de fichiers. Celles-ci sont retournées par les fonctions [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateMutex**](/windows/desktop/api/synchapi/nf-synchapi-createmutexa), [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), [**CreateNamedPipe**](/windows/desktop/api/winbase/nf-winbase-createnamedpipea), [**CreatePipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe)et [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) , respectivement.
-   Variables d'environnement.
-   Le répertoire actif.
-   La console, sauf si le processus est détaché ou si une nouvelle console est créée. Un processus de console enfant peut également hériter des handles standard du parent, ainsi qu’un accès à la mémoire tampon d’entrée et à la mémoire tampon d’écran active.
-   Le mode d’erreur, tel que défini par la fonction [**SetErrorMode**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-seterrormode) .
-   Masque d’affinité du processeur.
-   Association avec un travail.

Le processus enfant n’hérite pas des éléments suivants :

-   Classe de priorité.
-   Handles retournés par [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**HeapCreate**](/windows/desktop/api/heapapi/nf-heapapi-heapcreate)et [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc).
-   Les Pseudo-Handles, comme dans les descripteurs retournés par la fonction [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) ou [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) . Ces handles ne sont valides que pour le processus appelant.
-   Descripteurs de module DLL retournés par la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) .
-   Des handles GDI ou utilisateur, tels que **HBITMAP** ou **HMENU**.

## <a name="inheriting-handles"></a>Hériter des handles

Un processus enfant peut hériter de certains des handles de son parent, mais ne pas en hériter d’autres. Pour faire en sorte qu’un handle soit hérité, vous devez effectuer deux opérations :

-   Spécifie que le handle doit être hérité lorsque vous créez, ouvrez ou dupliquez le handle. Les fonctions de création utilisent généralement le membre **bInheritHandle** d’une structure d' [**\_ attributs de sécurité**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) à cet effet. [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) utilise le paramètre *bInheritHandles* .
-   Spécifiez que les handles pouvant être hérités doivent être hérités en définissant le paramètre *bInheritHandles* sur true lors de l’appel de la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . En outre, pour hériter des handles d’entrée standard, de sortie standard et d’erreur standard, le membre **dwFlags** de la structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) doit inclure STARTF \_ USESTDHANDLES.

Pour spécifier une liste des descripteurs qui doivent être hérités par un processus enfant spécifique, appelez la fonction [**UpdateProcThreadAttribute**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) avec l’indicateur *PROC_THREAD_ATTRIBUTE_HANDLE_LIST* .

Un handle hérité fait référence au même objet dans le processus enfant que dans le processus parent. Elle a également la même valeur et les mêmes privilèges d’accès. Par conséquent, lorsqu’un processus modifie l’état de l’objet, la modification affecte les deux processus. Pour utiliser un handle, le processus enfant doit récupérer la valeur du handle et « connaître » l’objet auquel il fait référence. En règle générale, le processus parent communique ces informations au processus enfant par le biais de sa ligne de commande, d’un bloc d’environnement ou d’une certaine forme de [communication entre processus](/windows/desktop/ipc/interprocess-communications).

Utilisez la fonction [**SetHandleInformation**](/windows/win32/api/handleapi/nf-handleapi-sethandleinformation) pour contrôler si un handle existant peut ou non être hérité.

## <a name="inheriting-environment-variables"></a>Héritage de variables d’environnement

Par défaut, un processus enfant hérite des variables d’environnement de son processus parent. Toutefois, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permet au processus parent de spécifier un autre bloc de variables d’environnement. Pour plus d’informations, consultez [variables d’environnement](environment-variables.md).

## <a name="inheriting-the-current-directory"></a>Héritage du répertoire actif

La fonction [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) récupère le répertoire actif du processus appelant. Par défaut, un processus enfant hérite le répertoire actuel de son processus parent. Toutefois, [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permet au processus parent de spécifier un répertoire actif différent pour le processus enfant. Pour modifier le répertoire actif du processus appelant, utilisez la fonction [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) .
