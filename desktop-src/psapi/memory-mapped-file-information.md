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
# <a name="memory-mapped-file-information"></a><span data-ttu-id="38014-104">Informations sur le fichier Memory-Mapped</span><span class="sxs-lookup"><span data-stu-id="38014-104">Memory-Mapped File Information</span></span>

<span data-ttu-id="38014-105">Un *fichier mappé en mémoire* (ou *mappage de fichiers*) est le résultat de l’Association du contenu d’un fichier à une partie de l’espace d’adressage virtuel d’un processus.</span><span class="sxs-lookup"><span data-stu-id="38014-105">A *memory-mapped file* (or *file mapping*) is the result of associating a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="38014-106">Il peut être utilisé pour partager un fichier ou une mémoire entre deux ou plusieurs processus.</span><span class="sxs-lookup"><span data-stu-id="38014-106">It can be used to share a file or memory between two or more processes.</span></span>

<span data-ttu-id="38014-107">La fonction [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) reçoit un handle de processus et un pointeur vers une adresse comme entrée.</span><span class="sxs-lookup"><span data-stu-id="38014-107">The [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) function receives a process handle and a pointer to an address as input.</span></span> <span data-ttu-id="38014-108">Si l’adresse se trouve dans un fichier mappé en mémoire dans l’espace d’adressage virtuel du processus, la fonction retourne le nom du fichier mappé en mémoire.</span><span class="sxs-lookup"><span data-stu-id="38014-108">If the address is within a memory-mapped file in the virtual address space of the process, the function returns the name of the memory-mapped file.</span></span> <span data-ttu-id="38014-109">Les noms de fichiers retournés par **GetMappedFileName** utilisent le format de l’appareil, plutôt que les lettres de lecteur.</span><span class="sxs-lookup"><span data-stu-id="38014-109">The file names returned by **GetMappedFileName** use device form, rather than drive letters.</span></span> <span data-ttu-id="38014-110">Par exemple, le nom de fichier c : \\ winnt \\ system32 \\ CType. nls ressemble à ce qui suit sous forme de périphérique :</span><span class="sxs-lookup"><span data-stu-id="38014-110">For example, the file name c:\\winnt\\system32\\ctype.nls would look like this in device form:</span></span>

<span data-ttu-id="38014-111">\\Appareil \\ Harddisk0 \\ Partition1 \\ winnt \\ system32 \\ CType. nls</span><span class="sxs-lookup"><span data-stu-id="38014-111">\\Device\\Harddisk0\\Partition1\\WINNT\\System32\\ctype.nls</span></span>

<span data-ttu-id="38014-112">Pour plus d’informations sur les fichiers mappés en mémoire, consultez [mappage de fichiers](/windows/desktop/Memory/file-mapping).</span><span class="sxs-lookup"><span data-stu-id="38014-112">For more information about memory-mapped files, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="38014-113">Pour obtenir un exemple qui convertit les noms de fichiers sous forme de périphérique en lettres de lecteur, consultez [obtention d’un nom de fichier à partir d’un handle de fichier](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span><span class="sxs-lookup"><span data-stu-id="38014-113">For an example that converts file names in device form to drive letters, see [Obtaining a File Name From a File Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span></span>

 

 