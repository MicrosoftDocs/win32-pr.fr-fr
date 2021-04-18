---
title: À propos des e/s de fichier multimédia
description: À propos des e/s de fichier multimédia
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Multimédia Windows, e/s de fichier
- multimédia, e/s de fichier
- entrée multimédia, e/s de fichier
- e/s de fichier multimédia, à propos de
- e/s de fichier, à propos de
- entrée et sortie (e/s), à propos de
- E/s (entrée et sortie), à propos de
- e/s de base
- RIFF (Resource Interchange File Format)
- RIFF (Resource Interchange File Format)
- E/S RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512251"
---
# <a name="about-multimedia-file-io"></a><span data-ttu-id="1bde2-114">À propos des e/s de fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="1bde2-114">About Multimedia File I/O</span></span>

<span data-ttu-id="1bde2-115">La plupart des applications multimédias nécessitent une entrée et une sortie de fichier (e/s), c’est-à-dire la possibilité de créer, de lire et d’écrire des fichiers sur disque.</span><span class="sxs-lookup"><span data-stu-id="1bde2-115">Most multimedia applications require file input and output (I/O) — that is, the ability to create, read, and write disk files.</span></span> <span data-ttu-id="1bde2-116">Les services d’e/s de fichier multimédia fournissent des e/s de fichier mises en mémoire tampon et non mises en mémoire tampon et prennent en charge les fichiers RIFF.</span><span class="sxs-lookup"><span data-stu-id="1bde2-116">Multimedia file I/O services provide buffered and unbuffered file I/O and support for RIFF files.</span></span> <span data-ttu-id="1bde2-117">Les services sont extensibles avec des procédures d’e/s personnalisées qui peuvent être partagées entre les applications.</span><span class="sxs-lookup"><span data-stu-id="1bde2-117">The services are extensible with custom I/O procedures that can be shared among applications.</span></span>

<span data-ttu-id="1bde2-118">La plupart des applications ont uniquement besoin des services d’e/s de base et des services d’e/s de fichier RIFF.</span><span class="sxs-lookup"><span data-stu-id="1bde2-118">Most applications need only the basic file I/O services and the RIFF file I/O services.</span></span> <span data-ttu-id="1bde2-119">Les applications sensibles aux performances d’e/s de fichier, telles que les applications qui diffusent des données à partir d’un CD-ROM en temps réel, peuvent optimiser les performances en utilisant des services pour accéder directement au tampon d’e/s de fichier.</span><span class="sxs-lookup"><span data-stu-id="1bde2-119">Applications sensitive to file I/O performance, such as applications that stream data from compact disc in real time, can optimize performance by using services to directly access the file I/O buffer.</span></span> <span data-ttu-id="1bde2-120">Les applications qui accèdent à des systèmes de stockage personnalisés, tels que des Archives de fichiers et des bases de données, peuvent fournir leur propre procédure d’e/s qui lit et écrit des éléments du système de stockage.</span><span class="sxs-lookup"><span data-stu-id="1bde2-120">Applications that access custom storage systems, such as file archives and databases, can provide their own I/O procedure that reads and writes elements of the storage system.</span></span>

 

 




