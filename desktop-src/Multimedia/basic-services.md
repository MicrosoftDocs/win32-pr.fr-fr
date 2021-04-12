---
title: Services de base
description: Services de base
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- e/s de fichier multimédia, services de base
- e/s de fichier, services de base
- entrée et sortie (e/s), services de base
- E/s (entrée et sortie), services de base
- e/s de base
- mmioOpen fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381917"
---
# <a name="basic-services"></a><span data-ttu-id="e0d7b-109">Services de base</span><span class="sxs-lookup"><span data-stu-id="e0d7b-109">Basic Services</span></span>

<span data-ttu-id="e0d7b-110">L’utilisation des services d’e/s de base est semblable à l’utilisation des services d’e/s de fichier au moment de l’exécution de la bibliothèque Runtime C.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-110">Using the basic I/O services is similar to using the run-time file I/O services of the C run-time library.</span></span> <span data-ttu-id="e0d7b-111">Les fichiers doivent être ouverts pour pouvoir être lus ou écrits.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-111">Files must be opened before they can be read or written.</span></span> <span data-ttu-id="e0d7b-112">Après la lecture ou l’écriture, le fichier doit être fermé.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-112">After reading or writing, the file must be closed.</span></span> <span data-ttu-id="e0d7b-113">Vous pouvez également modifier l’emplacement actuel de lecture ou d’écriture dans un fichier ouvert.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-113">You can also change the current read or write location within an open file.</span></span>

<span data-ttu-id="e0d7b-114">Avant de commencer des opérations d’e/s dans un fichier, vous devez ouvrir le fichier à l’aide de la fonction [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="e0d7b-114">Before you begin any I/O operations to a file, you must open the file by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="e0d7b-115">Cette fonction retourne un handle de fichier de type **HMMIO**.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-115">This function returns a file handle of type **HMMIO**.</span></span> <span data-ttu-id="e0d7b-116">Vous pouvez utiliser ce descripteur de fichier pour identifier le fichier ouvert lors de l’appel d’autres fonctions d’e/s de fichier.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-116">You can use this file handle to identify the open file when calling other file I/O functions.</span></span>

> [!Note]  
> <span data-ttu-id="e0d7b-117">Un descripteur de fichier **HMMIO** n’est pas un descripteur de fichier standard.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-117">An **HMMIO** file handle is not a standard file handle.</span></span> <span data-ttu-id="e0d7b-118">N’utilisez pas de descripteurs de fichiers **HMMIO** avec des fonctions d’e/s de fichier Win32 ou C.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-118">Do not use **HMMIO** file handles with Win32 or C run-time file I/O functions.</span></span>

 

<span data-ttu-id="e0d7b-119">Quand vous utilisez [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) pour ouvrir un fichier, vous utilisez un indicateur pour spécifier si vous l’ouvrez pour la lecture, l’écriture ou les deux.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-119">When you use [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) to open a file, you use a flag to specify whether you are opening it for reading, writing, or both.</span></span> <span data-ttu-id="e0d7b-120">Vous pouvez également spécifier des indicateurs qui vous permettent de créer ou de supprimer un fichier.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-120">You can also specify flags that enable you to create or delete a file.</span></span> <span data-ttu-id="e0d7b-121">Utilisez la fonction [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) pour fermer un fichier une fois que vous avez terminé de le lire ou d’écrire dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-121">Use the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function to close a file when you are finished reading or writing to it.</span></span>

<span data-ttu-id="e0d7b-122">Vous pouvez lire et écrire des fichiers à l’aide des fonctions [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) et [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-122">You can read and write files by using the [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) and [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) functions respectively.</span></span> <span data-ttu-id="e0d7b-123">L’opération de lecture ou d’écriture suivante se produit à la position de fichier actuelle ou au pointeur de fichier dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-123">The next read or write operation occurs at the current file position or file pointer in a file.</span></span> <span data-ttu-id="e0d7b-124">La position actuelle du fichier est avancée chaque fois qu’un fichier est lu ou écrit.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-124">The current file position is advanced each time a file is read or written.</span></span>

<span data-ttu-id="e0d7b-125">Vous pouvez également modifier la position actuelle du fichier à l’aide de la fonction [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .</span><span class="sxs-lookup"><span data-stu-id="e0d7b-125">You can also change the current file position by using the [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) function.</span></span> <span data-ttu-id="e0d7b-126">Vous devez vous assurer que vous spécifiez un emplacement valide dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-126">You should ensure that you specify a valid location in a file.</span></span> <span data-ttu-id="e0d7b-127">Si vous spécifiez un emplacement non valide, par exemple au-delà de la fin du fichier, **mmioSeek** peut ne pas renvoyer d’erreur, mais les opérations d’e/s ultérieures peuvent échouer.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-127">If you specify an invalid location, such as past the end of the file, **mmioSeek** may not return an error, but subsequent I/O operations could fail.</span></span>

<span data-ttu-id="e0d7b-128">Il existe des indicateurs que vous pouvez utiliser avec la fonction **mmioOpen** pour les opérations au-delà des e/s de fichier de base.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-128">There are flags you can use with the **mmioOpen** function for operations beyond basic file I/O.</span></span> <span data-ttu-id="e0d7b-129">En spécifiant une structure [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , par exemple, vous pouvez ouvrir des fichiers de mémoire, spécifier une procédure d’e/s personnalisée ou fournir une mémoire tampon pour les e/s mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="e0d7b-129">By specifying an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure, for example, you can open memory files, specify a custom I/O procedure, or supply a buffer for buffered I/O.</span></span>

 

 