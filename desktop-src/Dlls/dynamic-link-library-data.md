---
description: Une bibliothèque de Dynamic-Link (DLL) peut contenir des données globales ou des données locales.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link des données de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83280d3bfc449061c44f9e8bfd9b47833e7eca19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123686"
---
# <a name="dynamic-link-library-data"></a>Dynamic-Link des données de bibliothèque

Une bibliothèque de Dynamic-Link (DLL) peut contenir des données globales ou des données locales.

## <a name="variable-scope"></a>Portée des variables

Les variables déclarées comme globales dans un fichier de code source DLL sont traitées comme des variables globales par le compilateur et l’éditeur de liens, mais chaque processus qui charge une DLL donnée obtient sa propre copie des variables globales de cette DLL. La portée des variables statiques est limitée au bloc dans lequel les variables statiques sont déclarées. Par conséquent, chaque processus possède sa propre instance des variables globales et statiques de la DLL par défaut.

> [!Note]  
> Vos outils de développement peuvent vous permettre de remplacer le comportement par défaut. Par exemple, le compilateur Visual C++ prend en charge la **\# section pragma** et l’éditeur de liens prend en charge l’option/section. Pour plus d’informations, consultez la documentation fournie avec vos outils de développement.

 

## <a name="dynamic-memory-allocation"></a>Allocation de Mémoire dynamique

Lorsqu’une DLL alloue de la mémoire à l’aide de l’une des fonctions d’allocation de mémoire ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)et [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)), la mémoire est allouée dans l’espace d’adressage virtuel du processus appelant et est accessible uniquement aux threads de ce processus.

Une DLL peut utiliser le mappage de fichiers pour allouer de la mémoire qui peut être partagée entre les processus. Pour une présentation générale de l’utilisation du mappage de fichiers pour créer une mémoire partagée nommée, consultez [mappage de fichiers](/windows/desktop/Memory/file-mapping). Pour obtenir un exemple qui utilise la fonction [**DllMain**](dllmain.md) pour configurer la mémoire partagée à l’aide du mappage de fichiers, consultez [utilisation de la mémoire partagée dans une bibliothèque de Dynamic-Link](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>stockage local des threads

Les fonctions de stockage local des threads (TLS) permettent à une DLL d’allouer un index pour le stockage et la récupération d’une valeur différente pour chaque thread d’un processus multithread. Par exemple, une application de feuille de calcul peut créer une nouvelle instance du même thread chaque fois que l’utilisateur ouvre une nouvelle feuille de calcul. Une DLL qui fournit les fonctions pour diverses opérations de feuille de calcul peut utiliser TLS pour enregistrer les informations sur l’état actuel de chaque feuille de calcul (ligne, colonne, etc.). pour une présentation générale du stockage local des threads, consultez [thread local Stockage](/windows/desktop/ProcThread/thread-local-storage). pour obtenir un exemple qui utilise la fonction [**DllMain**](dllmain.md) pour configurer le stockage local des threads, consultez [utilisation de threads locaux Stockage dans une bibliothèque de Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

**Windows Server 2003 et Windows XP :** Le compilateur Visual C++ prend en charge une syntaxe qui vous permet de déclarer des variables de thread local : **\_ declspec (thread)**. si vous utilisez cette syntaxe dans une dll, vous ne pourrez pas charger la dll explicitement à l’aide de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) sur les versions de Windows antérieures à Windows Vista. Si votre DLL sera chargée de manière explicite, vous devez utiliser les fonctions de stockage local des threads au lieu de **\_ declspec (thread)**.

 

 
