---
title: Informations sur le fichier Memory-Mapped
description: Un fichier mappé en mémoire (ou mappage de fichiers) est le résultat de l’Association du contenu d’un fichier à une partie de l’espace d’adressage virtuel d’un processus. Il peut être utilisé pour partager un fichier ou une mémoire entre deux ou plusieurs processus.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102161"
---
# <a name="memory-mapped-file-information"></a>Informations sur le fichier Memory-Mapped

Un *fichier mappé en mémoire* (ou *mappage de fichiers*) est le résultat de l’Association du contenu d’un fichier à une partie de l’espace d’adressage virtuel d’un processus. Il peut être utilisé pour partager un fichier ou une mémoire entre deux ou plusieurs processus.

La fonction [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) reçoit un handle de processus et un pointeur vers une adresse comme entrée. Si l’adresse se trouve dans un fichier mappé en mémoire dans l’espace d’adressage virtuel du processus, la fonction retourne le nom du fichier mappé en mémoire. Les noms de fichiers retournés par **GetMappedFileName** utilisent le format de l’appareil, plutôt que les lettres de lecteur. Par exemple, le nom de fichier c : \\ winnt \\ system32 \\ CType. nls ressemble à ce qui suit sous forme de périphérique :

\\Appareil \\ Harddisk0 \\ Partition1 \\ winnt \\ system32 \\ CType. nls

Pour plus d’informations sur les fichiers mappés en mémoire, consultez [mappage de fichiers](/windows/desktop/Memory/file-mapping). Pour obtenir un exemple qui convertit les noms de fichiers sous forme de périphérique en lettres de lecteur, consultez [obtention d’un nom de fichier à partir d’un handle de fichier](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).

 

 