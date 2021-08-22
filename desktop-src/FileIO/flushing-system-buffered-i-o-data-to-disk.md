---
description: Windows stocke les données dans des opérations de lecture et d’écriture de fichiers dans des mémoires tampons de données gérées par le système pour optimiser les performances du disque.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Vidage du System-Buffered des données d’e/s sur le disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44740158ce1a5a2c3449a0fc5b90bc04bb0da525709cf7ee05c8768d10c39460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068699"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Vidage du System-Buffered des données d’e/s sur le disque

Windows stocke les données dans des opérations de lecture et d’écriture de fichiers dans des mémoires tampons de données gérées par le système pour optimiser les performances du disque. Quand une application écrit dans un fichier, le système met généralement en mémoire tampon les données et écrit les données sur le disque régulièrement. Une application peut forcer le système d’exploitation à écrire le contenu de ces mémoires tampons de données sur le disque à l’aide de la fonction [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) . Une application peut également spécifier que les opérations d’écriture doivent contourner la mémoire tampon de données et écrire directement sur le disque en définissant l’indicateur de **fichier sans indicateur de \_ mise en \_ \_ mémoire tampon** lors de la création ou de l’ouverture du fichier à l’aide de la fonction [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

S’il y a des données dans la mémoire tampon interne lorsque le fichier est fermé, le système d’exploitation n’écrit pas automatiquement le contenu de la mémoire tampon sur le disque avant de fermer le fichier. Si l’application ne force pas le système d’exploitation à écrire le tampon sur le disque avant de fermer le fichier, l’algorithme de mise en cache détermine le moment où la mémoire tampon est écrite.

> [!Note]  
> L’accès à une mémoire tampon de données pendant qu’une opération de lecture ou d’écriture l’utilise peut corrompre la mémoire tampon. Les applications ne doivent pas lire, écrire, réallouer ou libérer la mémoire tampon de données utilisée par une opération de lecture ou d’écriture jusqu’à la fin de l’opération.

 

 

 



