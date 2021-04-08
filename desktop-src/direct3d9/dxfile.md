---
description: Les indicateurs suivants sont utilisés pour spécifier les canaux à utiliser dans une texture. Action déconseillée.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Constantes DXFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f1651d17f5acb2ef24ff9dae2ef547c3df7c0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033487"
---
# <a name="dxfile-constants"></a><span data-ttu-id="a5e4f-104">Constantes DXFILE</span><span class="sxs-lookup"><span data-stu-id="a5e4f-104">DXFILE Constants</span></span>

<span data-ttu-id="a5e4f-105">Les indicateurs suivants sont utilisés pour spécifier les canaux à utiliser dans une texture.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="a5e4f-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="a5e4f-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="a5e4f-107">DXFILEFORMAT</span></span>



|                          |       |                  |
|--------------------------|-------|------------------|
| <span data-ttu-id="a5e4f-108">\#définition</span><span class="sxs-lookup"><span data-stu-id="a5e4f-108">\#define</span></span>                 | <span data-ttu-id="a5e4f-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5e4f-109">Value</span></span> | <span data-ttu-id="a5e4f-110">Description</span><span class="sxs-lookup"><span data-stu-id="a5e4f-110">Description</span></span>      |
| <span data-ttu-id="a5e4f-111">\_binaire DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="a5e4f-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="a5e4f-112">0</span><span class="sxs-lookup"><span data-stu-id="a5e4f-112">0</span></span>     | <span data-ttu-id="a5e4f-113">Fichier binaire.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-113">Binary file.</span></span>     |
| <span data-ttu-id="a5e4f-114">\_texte DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="a5e4f-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="a5e4f-115">1</span><span class="sxs-lookup"><span data-stu-id="a5e4f-115">1</span></span>     | <span data-ttu-id="a5e4f-116">Fichier texte.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-116">Text file.</span></span>       |
| <span data-ttu-id="a5e4f-117">DXFILEFORMAT \_ compressé</span><span class="sxs-lookup"><span data-stu-id="a5e4f-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="a5e4f-118">2</span><span class="sxs-lookup"><span data-stu-id="a5e4f-118">2</span></span>     | <span data-ttu-id="a5e4f-119">Fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-119">Compressed file.</span></span> |



 

<span data-ttu-id="a5e4f-120">Ces \# définitions sont déclarées dans dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="a5e4f-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="a5e4f-121">DXFILELOADOPTIONS</span></span>



|                          |       |                              |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="a5e4f-122">\#définition</span><span class="sxs-lookup"><span data-stu-id="a5e4f-122">\#define</span></span>                 | <span data-ttu-id="a5e4f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5e4f-123">Value</span></span> | <span data-ttu-id="a5e4f-124">Description</span><span class="sxs-lookup"><span data-stu-id="a5e4f-124">Description</span></span>                  |
| <span data-ttu-id="a5e4f-125">DXFILELOAD \_ FROMFILE</span><span class="sxs-lookup"><span data-stu-id="a5e4f-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="a5e4f-126">0x00L</span><span class="sxs-lookup"><span data-stu-id="a5e4f-126">0x00L</span></span> | <span data-ttu-id="a5e4f-127">Charge un fichier à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="a5e4f-128">DXFILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="a5e4f-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="a5e4f-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="a5e4f-129">0x01L</span></span> | <span data-ttu-id="a5e4f-130">Charger un fichier à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="a5e4f-131">DXFILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="a5e4f-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="a5e4f-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="a5e4f-132">0x02L</span></span> | <span data-ttu-id="a5e4f-133">Chargez un fichier à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="a5e4f-134">DXFILELOAD \_ FROMSTREAM</span><span class="sxs-lookup"><span data-stu-id="a5e4f-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="a5e4f-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="a5e4f-135">0x04L</span></span> | <span data-ttu-id="a5e4f-136">Charge un fichier à partir d’un flux.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="a5e4f-137">DXFILELOAD \_ FROMURL</span><span class="sxs-lookup"><span data-stu-id="a5e4f-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="a5e4f-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="a5e4f-138">0x08L</span></span> | <span data-ttu-id="a5e4f-139">Chargez un fichier à partir d’une URL.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="a5e4f-140">Ces \# définitions sont déclarées dans dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5e4f-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5e4f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5e4f-142">Référence de fichier X (héritée)</span><span class="sxs-lookup"><span data-stu-id="a5e4f-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



