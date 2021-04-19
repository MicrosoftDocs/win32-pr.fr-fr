---
description: Une application lit et écrit dans un fichier à l’aide des fonctions ReadFile, ReadFileEx, WriteFile et WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Lecture et écriture dans des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529350"
---
# <a name="reading-from-and-writing-to-files"></a><span data-ttu-id="40c45-103">Lecture et écriture dans des fichiers</span><span class="sxs-lookup"><span data-stu-id="40c45-103">Reading From and Writing to Files</span></span>

<span data-ttu-id="40c45-104">Une application lit et écrit dans un fichier à l’aide des fonctions [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .</span><span class="sxs-lookup"><span data-stu-id="40c45-104">An application reads from and writes to a file by using the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) functions.</span></span> <span data-ttu-id="40c45-105">Ces fonctions requièrent un handle vers un fichier à ouvrir pour la lecture et l’écriture, respectivement.</span><span class="sxs-lookup"><span data-stu-id="40c45-105">These functions require a handle to a file to be opened for reading and writing, respectively.</span></span> <span data-ttu-id="40c45-106">Ils lisent et écrivent un nombre spécifié d’octets à l’emplacement indiqué par le pointeur de fichier.</span><span class="sxs-lookup"><span data-stu-id="40c45-106">They read and write a specified number of bytes at the location indicated by the file pointer.</span></span> <span data-ttu-id="40c45-107">Les données sont lues et écrites exactement comme spécifié ; les fonctions ne mettent pas en forme les données.</span><span class="sxs-lookup"><span data-stu-id="40c45-107">The data is read and written exactly as specified; the functions do not format the data.</span></span>

<span data-ttu-id="40c45-108">Quand le pointeur de fichier atteint la fin d’un fichier et que l’application tente de lire à partir du fichier, aucune erreur ne se produit, mais aucun octet n’est lu.</span><span class="sxs-lookup"><span data-stu-id="40c45-108">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="40c45-109">Par conséquent, la lecture de zéro octet sans erreur signifie que l’application a atteint la fin du fichier.</span><span class="sxs-lookup"><span data-stu-id="40c45-109">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="40c45-110">L’écriture de zéro octet ne fait rien.</span><span class="sxs-lookup"><span data-stu-id="40c45-110">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="40c45-111">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="40c45-111">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="40c45-112">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="40c45-112">In this section</span></span>



| <span data-ttu-id="40c45-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="40c45-113">Topic</span></span>                                                                                                                                           | <span data-ttu-id="40c45-114">Description</span><span class="sxs-lookup"><span data-stu-id="40c45-114">Description</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40c45-115">Positionnement d’un pointeur de fichier</span><span class="sxs-lookup"><span data-stu-id="40c45-115">Positioning a File Pointer</span></span>](positioning-a-file-pointer.md)<br/>                                                                         | <span data-ttu-id="40c45-116">Windows utilise un pointeur de fichier pour effectuer le suivi des octets lus ou écrits.</span><span class="sxs-lookup"><span data-stu-id="40c45-116">Windows uses a file pointer to keep track of bytes read or written.</span></span><br/>                                                       |
| [<span data-ttu-id="40c45-117">Lecture ou écriture dans des fichiers à l’aide d’un schéma de Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="40c45-117">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | <span data-ttu-id="40c45-118">Décrit un schéma de ventilation-regroupement pour la lecture ou l’écriture de segments non contigus de données en une seule opération.</span><span class="sxs-lookup"><span data-stu-id="40c45-118">Describes a scatter-gather scheme for reading or writing noncontiguous chunks of data in one operation.</span></span><br/>                   |
| [<span data-ttu-id="40c45-119">Vidage du System-Buffered des données d’e/s sur le disque</span><span class="sxs-lookup"><span data-stu-id="40c45-119">Flushing System-Buffered I/O Data to Disk</span></span>](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | <span data-ttu-id="40c45-120">Windows stocke les données dans des opérations de lecture et d’écriture de fichiers dans des mémoires tampons de données gérées par le système pour optimiser les performances du disque.</span><span class="sxs-lookup"><span data-stu-id="40c45-120">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span><br/> |
| [<span data-ttu-id="40c45-121">Troncation ou extension des fichiers</span><span class="sxs-lookup"><span data-stu-id="40c45-121">Truncating or Extending Files</span></span>](truncating-or-extending-files.md)<br/>                                                                   | <span data-ttu-id="40c45-122">Une application peut tronquer ou étendre un fichier en appelant [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="40c45-122">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span><br/>                             |



 

 

 




