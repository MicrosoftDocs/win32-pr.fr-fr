---
title: Création d’un bloc RIFF
description: Création d’un bloc RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- e/s de fichier multimédia, création de bloc RIFF
- e/s de fichier, création d’un bloc RIFF
- entrée et sortie (e/s), création d’un bloc RIFF
- E/s (entrée et sortie), création d’un bloc RIFF
- création du bloc RIFF
- mmioCreateChunk fonction)
- RIFF (Resource Interchange File Format)
- RIFF (Resource Interchange File Format)
- E/S RIFF
- Bloc RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842194"
---
# <a name="creating-a-riff-chunk"></a><span data-ttu-id="04216-113">Création d’un bloc RIFF</span><span class="sxs-lookup"><span data-stu-id="04216-113">Creating a RIFF Chunk</span></span>

<span data-ttu-id="04216-114">L’exemple suivant utilise la fonction [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) pour créer un segment avec un identificateur de segment « Riff » et un type de formulaire « RDIB ».</span><span class="sxs-lookup"><span data-stu-id="04216-114">The following example uses the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function to create a chunk with a chunk identifier of "RIFF" and a form type of "RDIB".</span></span>


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



<span data-ttu-id="04216-115">Si vous créez un bloc « RIFF » ou « LIST », vous devez spécifier le type de formulaire ou le type de liste dans le membre **fccType** de la structure [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) .</span><span class="sxs-lookup"><span data-stu-id="04216-115">If you are creating a "RIFF" or "LIST" chunk, you must specify the form type or list type in the **fccType** member of the [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) structure.</span></span> <span data-ttu-id="04216-116">Dans l’exemple précédent, « RDIB » est le type de formulaire.</span><span class="sxs-lookup"><span data-stu-id="04216-116">In the previous example, "RDIB" is the form type.</span></span>

<span data-ttu-id="04216-117">Si vous connaissez la taille du champ de données dans un nouveau bloc, vous pouvez définir le membre **cksize** de la structure **MMCKINFO** lors de la création du bloc.</span><span class="sxs-lookup"><span data-stu-id="04216-117">If you know the size of the data field in a new chunk, you can set the **cksize** member of the **MMCKINFO** structure when you create the chunk.</span></span> <span data-ttu-id="04216-118">Cette valeur sera écrite dans le champ de la taille des données dans le nouveau bloc.</span><span class="sxs-lookup"><span data-stu-id="04216-118">This value will be written to the data size field in the new chunk.</span></span> <span data-ttu-id="04216-119">Si cette valeur n’est pas correcte lorsque vous appelez [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) pour marquer la fin du segment, elle est automatiquement réécrite pour refléter la taille correcte du champ de données.</span><span class="sxs-lookup"><span data-stu-id="04216-119">If this value is not correct when you call [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) to mark the end of the chunk, it will be automatically rewritten to reflect the correct size of the data field.</span></span>

<span data-ttu-id="04216-120">Une fois que vous avez créé un segment à l’aide de la fonction [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , la position de fichier est définie sur le champ de données du segment (8 octets à partir du début du bloc).</span><span class="sxs-lookup"><span data-stu-id="04216-120">After you create a chunk by using the [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) function, the file position is set to the data field of the chunk (8 bytes from the beginning of the chunk).</span></span> <span data-ttu-id="04216-121">Si le segment est un bloc « RIFF » ou « LIST », la position de fichier est définie sur l’emplacement suivant le type de formulaire ou le type de liste (12 octets à partir du début du bloc).</span><span class="sxs-lookup"><span data-stu-id="04216-121">If the chunk is a "RIFF" or "LIST" chunk, the file position is set to the location following the form type or list type (12 bytes from the beginning of the chunk).</span></span>

 

 