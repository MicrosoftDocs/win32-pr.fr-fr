---
description: Toute la mémoire allouée par un processus à l’aide des fonctions d’allocation de mémoire (HeapAlloc, VirtualAlloc, GlobalAlloc ou LocalAlloc) est accessible uniquement au processus.
ms.assetid: b47200dc-6824-4fd8-8d9f-2aaa439a74ff
title: Portée de la mémoire allouée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f06b0ee3f9446962bb508c23d4c5542fd16168027c5913b63438d16b6cea910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067669"
---
# <a name="scope-of-allocated-memory"></a>Portée de la mémoire allouée

Toute la mémoire allouée par un processus à l’aide des fonctions d’allocation de mémoire ( [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc), [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc)ou [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)) est accessible uniquement au processus. Toutefois, la mémoire allouée par une DLL est allouée dans l’espace d’adressage du processus qui a appelé la DLL et n’est pas accessible aux autres processus à l’aide de la même DLL. Pour créer de la mémoire partagée, vous devez utiliser le mappage de fichiers.

Le mappage de fichier nommé offre un moyen simple de créer un bloc de mémoire partagée. Un processus peut spécifier un nom lorsqu’il utilise la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) pour créer un objet de mappage de fichiers. D’autres processus peuvent spécifier le même nom pour la fonction **CreateFileMapping** ou [**OpenFileMapping**](/windows/desktop/api/WinBase/nf-winbase-openfilemappinga) pour obtenir un descripteur de l’objet de mappage.

Chaque processus spécifie son descripteur de l’objet de mappage de fichiers dans la fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pour mapper une vue du fichier dans son propre espace d’adressage. Les vues de tous les processus pour un objet de mappage de fichier unique sont mappées dans les mêmes pages partageables de stockage physique. Toutefois, les adresses virtuelles des vues mappées peuvent varier d’un processus à un autre, sauf si la fonction [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) est utilisée pour mapper la vue à une adresse spécifiée. Bien qu’elles soient partageables, les pages de stockage physique utilisées pour une vue de fichier mappée ne sont pas globales ; ils ne sont pas accessibles aux processus qui n’ont pas mappé une vue du fichier.

Toutes les pages validées par le mappage d’une vue d’un fichier sont libérées lorsque le dernier processus avec une vue de l’objet de mappage se termine ou annule la mise en correspondance de sa vue en appelant la fonction [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) . À ce stade, le fichier spécifié (le cas échéant) associé à l’objet de mappage est mis à jour. Un fichier spécifié peut également être forcé à être mis à jour en appelant la fonction [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) .

Pour plus d’informations, consultez [mappage de fichiers](file-mapping.md). Pour obtenir un exemple de mémoire partagée dans une DLL, consultez [utilisation de la mémoire partagée dans une bibliothèque de Dynamic-Link](../dlls/using-shared-memory-in-a-dynamic-link-library.md).

Si plusieurs processus ont accès en écriture à la mémoire partagée, vous devez synchroniser l’accès à la mémoire. Pour plus d’informations, consultez [Synchronization](../sync/synchronization.md).

 

 
