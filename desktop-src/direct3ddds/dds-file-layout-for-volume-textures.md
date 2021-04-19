---
title: Exemple de texture de volume DDS
description: Pour une texture de volume, utilisez la DDSCAPS \_ complexe, le \_ volume DDSCAPS2, la profondeur DDSD, les \_ indicateurs et le jeu et dwDepth. Une texture de volume est une extension d’une texture standard pour Direct3D 9 ; une texture de volume peut être définie avec ou sans des mipmaps.
ms.assetid: c1675a6d-129a-4e95-993f-e1be905781cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d82faa8041f2b5c99ef57ee2386ff5de84d787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509802"
---
# <a name="dds-volume-texture-example"></a><span data-ttu-id="97d51-104">Exemple de texture de volume DDS</span><span class="sxs-lookup"><span data-stu-id="97d51-104">DDS Volume Texture Example</span></span>

<span data-ttu-id="97d51-105">Pour une texture de volume, utilisez la DDSCAPS \_ complexe, le \_ volume DDSCAPS2, la profondeur DDSD, les \_ indicateurs et le jeu et dwDepth.</span><span class="sxs-lookup"><span data-stu-id="97d51-105">For a volume texture, use the DDSCAPS\_COMPLEX, DDSCAPS2\_VOLUME, DDSD\_DEPTH, flags and set and dwDepth.</span></span> <span data-ttu-id="97d51-106">Une texture de volume est une extension d’une texture standard pour Direct3D 9 ; une texture de volume peut être définie avec ou sans des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="97d51-106">A volume texture is an extension of a standard texture for Direct3D 9; a volume texture is can be defined with or without mipmaps.</span></span>

<span data-ttu-id="97d51-107">Pour les volumes sans des mipmaps, chaque tranche de profondeur est écrite dans le fichier dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="97d51-107">For volumes without mipmaps, each depth slice is written to the file in order.</span></span> <span data-ttu-id="97d51-108">Si les des mipmaps sont inclus, toutes les tranches de profondeur pour un niveau de mipmap donné sont écrites ensemble, chaque niveau contenant un demi-nombre de secteurs comme niveau précédent, avec un minimum de 1.</span><span class="sxs-lookup"><span data-stu-id="97d51-108">If mipmaps are included, all depth slices for a given mipmap level are written together, with each level containing half as many slices as the previous level with a minimum of 1.</span></span>

<span data-ttu-id="97d51-109">Par exemple, une carte de volume 64 par 64-par-4 utilisant un format de pixel R8G8B8 (3 octets par pixel) avec tous les niveaux de mipmap contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="97d51-109">For example, a 64-by-64-by-4 volume map using a pixel format of R8G8B8 (3 bytes per pixel) with all mipmap levels would contain the following:</span></span>



| <span data-ttu-id="97d51-110">Composants DDS</span><span class="sxs-lookup"><span data-stu-id="97d51-110">DDS Components</span></span>                      | <span data-ttu-id="97d51-111">\# Bits</span><span class="sxs-lookup"><span data-stu-id="97d51-111">\# Bytes</span></span>    |
|-------------------------------------|-------------|
| <span data-ttu-id="97d51-112">en-tête</span><span class="sxs-lookup"><span data-stu-id="97d51-112">header</span></span>                              | <span data-ttu-id="97d51-113">128 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-113">128 bytes</span></span>   |
| <span data-ttu-id="97d51-114">64-par-64 tranche 1 sur 4 image principale.</span><span class="sxs-lookup"><span data-stu-id="97d51-114">64-by-64 slice 1 of 4 main image.</span></span>   | <span data-ttu-id="97d51-115">12288 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-115">12288 bytes</span></span> |
| <span data-ttu-id="97d51-116">64-par-64 tranche 2 sur 4 image principale.</span><span class="sxs-lookup"><span data-stu-id="97d51-116">64-by-64 slice 2 of 4 main image.</span></span>   | <span data-ttu-id="97d51-117">12288 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-117">12288 bytes</span></span> |
| <span data-ttu-id="97d51-118">64-par-64 tranche 3 sur 4 image principale.</span><span class="sxs-lookup"><span data-stu-id="97d51-118">64-by-64 slice 3 of 4 main image.</span></span>   | <span data-ttu-id="97d51-119">12288 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-119">12288 bytes</span></span> |
| <span data-ttu-id="97d51-120">64-par-64 tranche 4 sur 4 image principale.</span><span class="sxs-lookup"><span data-stu-id="97d51-120">64-by-64 slice 4 of 4 main image.</span></span>   | <span data-ttu-id="97d51-121">12288 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-121">12288 bytes</span></span> |
| <span data-ttu-id="97d51-122">32-par-32 section 1 sur 2 image mipmap.</span><span class="sxs-lookup"><span data-stu-id="97d51-122">32-by-32 slice 1 of 2 mipmap image.</span></span> | <span data-ttu-id="97d51-123">3072 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-123">3072 bytes</span></span>  |
| <span data-ttu-id="97d51-124">32-par-32 section 2 sur 2 image mipmap.</span><span class="sxs-lookup"><span data-stu-id="97d51-124">32-by-32 slice 2 of 2 mipmap image.</span></span> | <span data-ttu-id="97d51-125">3072 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-125">3072 bytes</span></span>  |
| <span data-ttu-id="97d51-126">16 par 16, tranche 1 sur 1 image mipmap.</span><span class="sxs-lookup"><span data-stu-id="97d51-126">16-by-16 slice 1 of 1 mipmap image.</span></span> | <span data-ttu-id="97d51-127">768 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-127">768 bytes</span></span>   |
| <span data-ttu-id="97d51-128">8 par 8, tranche 1 sur 1 image mipmap.</span><span class="sxs-lookup"><span data-stu-id="97d51-128">8-by-8 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="97d51-129">192 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-129">192 bytes</span></span>   |
| <span data-ttu-id="97d51-130">4-par-4 section 1 sur 1 image mipmap.</span><span class="sxs-lookup"><span data-stu-id="97d51-130">4-by-4 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="97d51-131">48 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-131">48 bytes</span></span>    |
| <span data-ttu-id="97d51-132">2-par-2 découpe 1 de 1 image mipmap.</span><span class="sxs-lookup"><span data-stu-id="97d51-132">2-by-2 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="97d51-133">12 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-133">12 bytes</span></span>    |
| <span data-ttu-id="97d51-134">1-par-1 tranche 1 sur 1 image mipmap.</span><span class="sxs-lookup"><span data-stu-id="97d51-134">1-by-1 slice 1 of 1 mipmap image.</span></span>   | <span data-ttu-id="97d51-135">3 octets</span><span class="sxs-lookup"><span data-stu-id="97d51-135">3 bytes</span></span>     |



 

<span data-ttu-id="97d51-136">Notez que le plus petit niveau de mipmap n’est que 3 octets, car bitCount est 24 et aucune compression n’est ajoutée à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="97d51-136">Note that the smallest mipmap level is only 3 bytes because the bitcount is 24 and there is no added compression at this level.</span></span>

<span data-ttu-id="97d51-137">La prise en charge des textures de volume a été ajoutée dans DirectX 8.</span><span class="sxs-lookup"><span data-stu-id="97d51-137">Support for volume textures was added in DirectX 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97d51-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97d51-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d51-139">Guide de programmation pour DDS</span><span class="sxs-lookup"><span data-stu-id="97d51-139">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




