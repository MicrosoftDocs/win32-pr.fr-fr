---
description: 'Cette rubrique décrit les fonctions de gestion de la mémoire :'
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Fonctions de gestion de la mémoire
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: a203583016a127a550f609068df8e86da384fa34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094114"
---
# <a name="memory-management-functions"></a>Fonctions de gestion de la mémoire

- [Fonctions de mémoire générales](#general-memory-functions)
- [Fonctions de prévention de l’exécution des données](#data-execution-prevention-functions)
- [Fonctions de mappage de fichiers](#file-mapping-functions)
- [Fonctions AWE](#awe-functions)
- [Fonctions de segment de mémoire](#heap-functions)
- [Fonctions de mémoire virtuelle](#virtual-memory-functions)
- [Fonctions globales et locales](#global-and-local-functions)
- [Fonctions de mémoire incorrectes](#bad-memory-functions)
- [Enclave, fonctions](#enclave-functions)
- [Fonctions thunk ATL](#atl-thunk-functions)
- [Fonctions obsolètes](#obsolete-functions)

## <a name="general-memory-functions"></a>Fonctions de mémoire générales

| Fonction | Description |
|-|-|
| [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Inscrit une fonction de rappel à appeler quand une plage de mémoire sécurisée est libérée ou si ses protections sont modifiées. |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Copie un bloc de mémoire d’un emplacement à un autre. |
| [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Crée un objet de notification de ressource mémoire. |
| [**FillMemory**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Remplit un bloc de mémoire avec une valeur spécifiée. |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Récupère la taille minimale d’une grande page. |
| [**GetPhysicallyInstalledSystemMemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Récupère la quantité de mémoire vive qui est physiquement installée sur l’ordinateur. |
| [**GetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Récupère les limites de taille actuelles pour la plage de travail du cache système. |
| [**GetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Récupère les adresses des pages qui ont été écrites dans une région de la mémoire virtuelle. |
| [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Obtient des informations sur l’utilisation actuelle du système de la mémoire physique et de la mémoire virtuelle. |
| [**MoveMemory**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Déplace un bloc de mémoire d’un emplacement à un autre. |
| [**QueryMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Récupère l’état de l’objet de ressource de mémoire spécifié. |
| [**RemoveSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Annule l’inscription d’une fonction de rappel précédemment enregistrée avec la fonction [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) . |
| [**ResetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Réinitialise l’état de suivi d’écriture pour une région de mémoire virtuelle. |
| [**SecureMemoryCacheCallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Fonction définie par l’application qui est appelée lorsqu’une plage de mémoire sécurisée est libérée ou que ses protections sont modifiées. |
| [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Remplit un bloc de mémoire avec des zéros. |
| [**SetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Limite la taille de la plage de travail pour le cache du système de fichiers. |
| [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Remplit un bloc de mémoire avec des zéros. |

## <a name="data-execution-prevention-functions"></a>Fonctions de prévention de l’exécution des données

Ces fonctions sont utilisées avec la [prévention de l’exécution des données](data-execution-prevention.md) (DEP).

| Fonction | Description |
|-|-|
| [**GetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Récupère les paramètres DEP d’un processus. |
| [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Récupère les paramètres DEP pour le système. |
| [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Modifie les paramètres DEP d’un processus. |

## <a name="file-mapping-functions"></a>Fonctions de mappage de fichiers

Ces fonctions sont utilisées dans le [mappage de fichiers](file-mapping.md).

| Fonction | Description |
|-|-|
| [**CreateFileMappingA**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Crée ou ouvre un objet de mappage de fichier nommé ou sans nom pour un fichier spécifié. |
| [**CreateFileMappingW**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Crée ou ouvre un objet de mappage de fichier nommé ou sans nom pour un fichier spécifié. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Crée ou ouvre un objet de mappage de fichier nommé ou sans nom pour un fichier spécifié. Vous pouvez spécifier un nœud NUMA préféré pour la mémoire physique en tant que paramètre étendu. consultez le paramètre *ExtendedParameters* . |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | crée ou ouvre un objet de mappage de fichier nommé ou sans nom pour un fichier spécifié à partir d’une application Windows Store. |
| [**CreateFileMappingNuma**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Crée ou ouvre un objet de mappage de fichier nommé ou sans nom pour un fichier spécifié et spécifie le nœud NUMA pour la mémoire physique. |
| [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Écrit sur le disque une plage d’octets dans une vue mappée d’un fichier. |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Vérifie si l’adresse spécifiée se trouve dans un fichier mappé en mémoire dans l’espace d’adressage du processus spécifié. Si c’est le cas, la fonction retourne le nom du fichier mappé en mémoire. |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Cartes une vue d’un mappage de fichier dans l’espace d’adressage d’un processus appelant. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Cartes une vue d’un fichier ou d’une section de fichier de pagination dans l’espace d’adressage du processus spécifié. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Cartes une vue d’un fichier ou d’une section de fichier de pagination dans l’espace d’adressage du processus spécifié. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Cartes une vue d’un mappage de fichier dans l’espace d’adressage d’un processus appelant à partir d’une application Windows Store. |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Cartes une vue d’un mappage de fichier dans l’espace d’adressage d’un processus appelant. Un appelant peut éventuellement spécifier une adresse mémoire suggérée pour la vue. |
| [**MapViewOfFileExNuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Cartes une vue d’un mappage de fichier dans l’espace d’adressage d’un processus appelant, et spécifie le nœud NUMA pour la mémoire physique. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Cartes une vue d’un mappage de fichier dans l’espace d’adressage d’un processus appelant à partir d’une application Windows Store. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Cartes une vue d’un fichier ou d’une section de fichier de pagination dans l’espace d’adressage du processus spécifié. |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Ouvre un objet de mappage de fichier nommé. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Ouvre un objet de mappage de fichier nommé. |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Démappe une vue mappée d’un fichier à partir de l’espace d’adressage du processus appelant. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Annule le mappage d’une vue précédemment mappée d’un fichier ou d’une section de fichier de pagination. |
| [**UnmapViewOfFileEx**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Annule le mappage d’une vue précédemment mappée d’un fichier ou d’une section de fichier de pagination. |

## <a name="awe-functions"></a>Fonctions AWE

Il s’agit des [fonctions AWE](address-windowing-extensions.md).

| Fonction | Description |
|-|-|
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Alloue des pages de mémoire physique à mapper et à démapper dans une région AWE du processus. |
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Alloue des pages de mémoire physique à mapper et à démapper au sein d’une région AWE du processus, et spécifie le nœud NUMA pour la mémoire physique. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Libère les pages de mémoire physique allouées précédemment avec [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages). |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Cartes pages mémoire physique allouées précédemment à l’adresse spécifiée au sein d’une région AWE. |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Cartes pages mémoire physique allouées précédemment à l’adresse spécifiée au sein d’une région AWE. |

## <a name="heap-functions"></a>Fonctions de segment de mémoire

Il s’agit des [fonctions du tas](heap-functions.md).

| Fonction | Description |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Obtient un handle vers le tas du processus appelant. |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Obtient des handles de tous les tas qui sont valides pour le processus appelant. |
| [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Alloue un bloc de mémoire à partir d’un segment de mémoire. |
| [**HeapCompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Fusionne les blocs libres adjacents de la mémoire sur un segment de mémoire. |
| [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Crée un objet segment de mémoire. |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Détruit l’objet de tas spécifié. |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Libère un bloc de mémoire alloué à partir d’un segment de mémoire. |
| [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Tente d’acquérir le verrou associé à un segment de mémoire spécifié. |
| [**HeapQueryInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Récupère des informations sur le tas spécifié. |
| [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Réalloue un bloc de mémoire à partir d’un segment de mémoire. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Définit des informations de tas pour le tas spécifié. |
| [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Récupère la taille d’un bloc de mémoire alloué à partir d’un segment de mémoire. |
| [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Libère la propriété du verrou associé à un segment de mémoire spécifié. |
| [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Tente de valider un segment de mémoire spécifié. |
| [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Énumère les blocs de mémoire dans un tas spécifié. |

## <a name="virtual-memory-functions"></a>Fonctions de mémoire virtuelle

Il s’agit des [fonctions de mémoire virtuelle](virtual-memory-functions.md).

| Fonction | Description |
|-|-|
| [**DiscardVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Ignore le contenu de la mémoire d’une plage de pages de mémoire, sans la désengagement de la mémoire. Le contenu de la mémoire ignorée n’est pas défini et doit être réécrit par l’application. |
| [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Indique que les données contenues dans une plage de pages mémoire ne sont plus nécessaires à l’application et peuvent être ignorées par le système si nécessaire. |
| [**PrefetchVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Prérécupère les plages d’adresses virtuelles dans la mémoire physique. |
| [**QueryVirtualMemoryInformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Retourne des informations sur une page ou un ensemble de pages dans l’espace d’adressage virtuel du processus spécifié. |
| [**ReclaimVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Récupère une plage de pages mémoire qui ont été proposées au système avec [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory). |
| [**SetProcessValidCallTargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Fournit à CFG une liste de cibles d’appel indirect valides et spécifie si elles doivent être marquées comme valides ou non. |
| [**VirtualAlloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Réserve ou valide une zone de pages dans l’espace d’adressage virtuel du processus appelant. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Réserve, valide ou modifie l’état d’une région de mémoire dans l’espace d’adressage virtuel d’un processus spécifié. La fonction initialise la mémoire qu’elle alloue à zéro. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Réserve, valide ou modifie l’état d’une région de pages dans l’espace d’adressage virtuel du processus appelant. La mémoire allouée par cette fonction est automatiquement initialisée à zéro. |
| [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Réserve ou valide une zone de pages dans l’espace d’adressage virtuel du processus spécifié. |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Réserve ou valide une zone de mémoire dans l’espace d’adressage virtuel du processus spécifié et spécifie le nœud NUMA pour la mémoire physique. |
| [**VirtualAllocFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Réserve, valide ou modifie l’état d’une région de pages dans l’espace d’adressage virtuel du processus appelant. La mémoire allouée par cette fonction est automatiquement initialisée à zéro. |
| [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Libère ou annule la validation d’une région de pages dans l’espace d’adressage virtuel du processus appelant. |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Libère ou annule la validation d’une zone de mémoire dans l’espace d’adressage virtuel d’un processus spécifié. |
| [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Verrouille la région spécifiée de l’espace d’adressage virtuel du processus dans la mémoire physique. |
| [**VirtualProtect,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Modifie la protection d’accès sur une région de pages validées dans l’espace d’adressage virtuel du processus appelant. |
| [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Modifie la protection d’accès sur une région de pages validées dans l’espace d’adressage virtuel du processus appelant. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Modifie la protection sur une région de pages validées dans l’espace d’adressage virtuel du processus appelant. |
| [**VirtualQuery,**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Fournit des informations sur une plage de pages dans l’espace d’adressage virtuel du processus appelant. |
| [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Fournit des informations sur une plage de pages dans l’espace d’adressage virtuel du processus appelant. |
| [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Déverrouille une plage spécifiée de pages dans l’espace d’adressage virtuel d’un processus. |

## <a name="global-and-local-functions"></a>Fonctions globales et locales

Consultez également [fonctions globales et locales](global-and-local-functions.md). ces fonctions sont fournies à des fins de compatibilité avec les Windows 16 bits et sont utilisées avec échange dynamique de données (DDE), les fonctions du presse-papiers et les objets de données OLE. À moins que la documentation stipule spécifiquement qu’une fonction globale ou locale doit être utilisée, les nouvelles applications doivent utiliser la [fonction de tas](heap-functions.md) correspondante avec le handle retourné par [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap). Pour obtenir des fonctionnalités équivalentes à la fonction globale ou locale, affectez la valeur 0 au paramètre *dwFlags* de la fonction Heap.

| Fonction | Description | Fonction Heap correspondante |
|-|-|-|
| [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [ **LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Alloue le nombre d’octets spécifié à partir du tas. | [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**GlobalDiscard**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard), [ **LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Ignore le bloc de mémoire globale spécifié. | Non applicable. |
| [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags), [ **LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Retourne des informations sur l’objet de mémoire globale spécifié. | Non applicable. Utilisez [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) pour valider le tas. |
| [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree), [ **LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Libère l’objet de mémoire globale spécifié. | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle), [ **LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Récupère le handle associé au pointeur spécifié vers un bloc de mémoire globale. Cette fonction doit être utilisée uniquement avec les fonctions OLE et Clipboard qui l’exigent. | Non applicable. |
| [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock), [ **LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Verrouille un objet mémoire global et retourne un pointeur vers le premier octet du bloc de mémoire de l’objet. | Non applicable. |
| [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc), [ **LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Modifie la taille ou les attributs d’un objet de mémoire globale spécifié. | [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Récupère la taille actuelle de l’objet de mémoire globale spécifié. | [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**GlobalUnlock**](/windows/desktop/api/WinBase/nf-winbase-globalunlock), [ **LocalUnlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Décrémente le nombre de verrous associé à un objet mémoire. Cette fonction doit être utilisée uniquement avec les fonctions OLE et Clipboard qui l’exigent. | Non applicable. |

## <a name="bad-memory-functions"></a>Fonctions de mémoire incorrectes

| Fonction | Description |
|-|-|
| [**BadMemoryCallbackRoutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Fonction définie par l’application inscrite avec la fonction [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) qui est appelée lorsqu’une ou plusieurs pages mémoire incorrectes sont détectées. |
| [**GetMemoryErrorHandlingCapabilities**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Obtient les fonctionnalités de gestion des erreurs de mémoire du système. |
| [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Inscrit une notification de mémoire incorrecte qui est appelée lorsqu’une ou plusieurs pages mémoire incorrectes sont détectées. |
| [**UnregisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Ferme le handle de notification de mémoire incorrect spécifié. |

## <a name="enclave-functions"></a>Enclave, fonctions

| Fonction | Description |
|-|-|
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Crée une enclave non initialisée. Une enclave est une région isolée de code et des données dans l’espace d’adressage d’une application. Seul le code qui s’exécute dans l’enclave peut accéder aux données dans la même enclave. |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Initialise une enclave que vous avez créée et chargée avec des données. |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Récupère une valeur indiquant si le type spécifié d’enclave est pris en charge. |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Charge des données dans une enclave non initialisée que vous avez créée en appelant [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave). |

## <a name="atl-thunk-functions"></a>Fonctions thunk ATL

| Fonction | Description |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Alloue de l’espace en mémoire pour un thunk ATL. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Retourne une fonction exécutable correspondant au paramètre AtlThunkData_t. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Libère la mémoire associée à un thunk ATL. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Initialise un thunk ATL. |

## <a name="obsolete-functions"></a>Fonctions obsolètes

Ces fonctions sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Windows :

- [**IsBadCodePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**IsBadReadPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**IsBadStringPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**IsBadWritePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

La fonction ci-dessous peut retourner des informations incorrectes et ne doit pas être utilisée. Utilisez plutôt la fonction [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) .

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)