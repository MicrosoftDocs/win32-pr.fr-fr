---
title: Exemple de texture DDS
description: Pour une texture non compressée, utilisez les \_ indicateurs RGB DDSD et DDPF \_ . pour une texture compressée, utilisez les \_ indicateurs DDSD LINEARSIZE et DDPF \_ FourCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510831"
---
# <a name="dds-texture-example"></a><span data-ttu-id="e12f2-103">Exemple de texture DDS</span><span class="sxs-lookup"><span data-stu-id="e12f2-103">DDS Texture Example</span></span>

<span data-ttu-id="e12f2-104">Pour une texture non compressée, utilisez les \_ indicateurs RGB DDSD et DDPF \_ . pour une texture compressée, utilisez les \_ indicateurs DDSD LINEARSIZE et DDPF \_ FourCC.</span><span class="sxs-lookup"><span data-stu-id="e12f2-104">For an uncompressed texture, use the DDSD\_PITCH and DDPF\_RGB flags; for a compressed texture, use the DDSD\_LINEARSIZE and DDPF\_FOURCC flags.</span></span> <span data-ttu-id="e12f2-105">Pour une texture mipmapped, utilisez également les \_ indicateurs DDSD MIPMAPCOUNT, DDSCAPS \_ MIPMAP et DDSCAPS Complex, ainsi que \_ le membre de décompte mipmap.</span><span class="sxs-lookup"><span data-stu-id="e12f2-105">For a mipmapped texture, use the DDSD\_MIPMAPCOUNT, DDSCAPS\_MIPMAP, and DDSCAPS\_COMPLEX flags also as well as the mipmap count member.</span></span> <span data-ttu-id="e12f2-106">Si les des mipmaps sont générés, tous les niveaux jusqu’à 1 par 1 sont généralement écrits.</span><span class="sxs-lookup"><span data-stu-id="e12f2-106">If mipmaps are generated, all levels down to 1-by-1 are usually written.</span></span>

<span data-ttu-id="e12f2-107">Pour une texture compressée, la taille de chaque image de niveau de mipmap correspond généralement à un quart de la taille du précédent, avec un minimum de 8 (DXT1) ou 16 (DXT2-5) octets (pour les textures carrées).</span><span class="sxs-lookup"><span data-stu-id="e12f2-107">For a compressed texture, the size of each mipmap level image is typically one-fourth the size of the previous, with a minimum of 8 (DXT1) or 16 (DXT2-5) bytes (for square textures).</span></span> <span data-ttu-id="e12f2-108">Utilisez la formule suivante pour calculer la taille de chaque niveau pour une texture non carrée :</span><span class="sxs-lookup"><span data-stu-id="e12f2-108">Use the following formula to calculate the size of each level for a non-square texture:</span></span>


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



<span data-ttu-id="e12f2-109">Ce tableau répertorie la quantité d’espace occupé par chaque couche pour une texture R8G8B8 de 256 par 256, sans utiliser la compression.</span><span class="sxs-lookup"><span data-stu-id="e12f2-109">This table lists the amount of space taken up by each layer for a 256-by-256 R8G8B8 texture, without using compression.</span></span>



| <span data-ttu-id="e12f2-110">Composants DDS</span><span class="sxs-lookup"><span data-stu-id="e12f2-110">DDS Components</span></span>          | <span data-ttu-id="e12f2-111">\# Bits</span><span class="sxs-lookup"><span data-stu-id="e12f2-111">\# Bytes</span></span> |
|-------------------------|----------|
| <span data-ttu-id="e12f2-112">en-tête</span><span class="sxs-lookup"><span data-stu-id="e12f2-112">header</span></span>                  | <span data-ttu-id="e12f2-113">128</span><span class="sxs-lookup"><span data-stu-id="e12f2-113">128</span></span>      |
| <span data-ttu-id="e12f2-114">256-par-256 image principale</span><span class="sxs-lookup"><span data-stu-id="e12f2-114">256-by-256 main image</span></span>   | <span data-ttu-id="e12f2-115">196 608</span><span class="sxs-lookup"><span data-stu-id="e12f2-115">196608</span></span>   |
| <span data-ttu-id="e12f2-116">image mipmap 128-par-128</span><span class="sxs-lookup"><span data-stu-id="e12f2-116">128-by-128 mipmap image</span></span> | <span data-ttu-id="e12f2-117">49152</span><span class="sxs-lookup"><span data-stu-id="e12f2-117">49152</span></span>    |
| <span data-ttu-id="e12f2-118">image mipmap 64-par-64</span><span class="sxs-lookup"><span data-stu-id="e12f2-118">64-by-64 mipmap image</span></span>   | <span data-ttu-id="e12f2-119">12288</span><span class="sxs-lookup"><span data-stu-id="e12f2-119">12288</span></span>    |
| <span data-ttu-id="e12f2-120">image mipmap 32-par-32</span><span class="sxs-lookup"><span data-stu-id="e12f2-120">32-by-32 mipmap image</span></span>   | <span data-ttu-id="e12f2-121">3 072</span><span class="sxs-lookup"><span data-stu-id="e12f2-121">3072</span></span>     |
| <span data-ttu-id="e12f2-122">image mipmap 16 par 16</span><span class="sxs-lookup"><span data-stu-id="e12f2-122">16-by-16 mipmap image</span></span>   | <span data-ttu-id="e12f2-123">768</span><span class="sxs-lookup"><span data-stu-id="e12f2-123">768</span></span>      |
| <span data-ttu-id="e12f2-124">image mipmap 8 par 8</span><span class="sxs-lookup"><span data-stu-id="e12f2-124">8-by-8 mipmap image</span></span>     | <span data-ttu-id="e12f2-125">192</span><span class="sxs-lookup"><span data-stu-id="e12f2-125">192</span></span>      |
| <span data-ttu-id="e12f2-126">image mipmap 4-par-4</span><span class="sxs-lookup"><span data-stu-id="e12f2-126">4-by-4 mipmap image</span></span>     | <span data-ttu-id="e12f2-127">48</span><span class="sxs-lookup"><span data-stu-id="e12f2-127">48</span></span>       |
| <span data-ttu-id="e12f2-128">image mipmap 2 par 2</span><span class="sxs-lookup"><span data-stu-id="e12f2-128">2-by-2 mipmap image</span></span>     | <span data-ttu-id="e12f2-129">12</span><span class="sxs-lookup"><span data-stu-id="e12f2-129">12</span></span>       |
| <span data-ttu-id="e12f2-130">image mipmap 1-par-1</span><span class="sxs-lookup"><span data-stu-id="e12f2-130">1-by-1 mipmap image</span></span>     | <span data-ttu-id="e12f2-131">3</span><span class="sxs-lookup"><span data-stu-id="e12f2-131">3</span></span>        |



 

<span data-ttu-id="e12f2-132">Ce tableau répertorie la quantité d’espace occupé par chaque couche pour la même texture à l’aide de la compression (DXT1).</span><span class="sxs-lookup"><span data-stu-id="e12f2-132">This table lists the amount of space taken up by each layer for the same texture using compression (DXT1).</span></span>



| <span data-ttu-id="e12f2-133">Composants DDS</span><span class="sxs-lookup"><span data-stu-id="e12f2-133">DDS Components</span></span>         | <span data-ttu-id="e12f2-134">\# Bits</span><span class="sxs-lookup"><span data-stu-id="e12f2-134">\# Bytes</span></span> |
|------------------------|----------|
| <span data-ttu-id="e12f2-135">en-tête</span><span class="sxs-lookup"><span data-stu-id="e12f2-135">header</span></span>                 | <span data-ttu-id="e12f2-136">128</span><span class="sxs-lookup"><span data-stu-id="e12f2-136">128</span></span>      |
| <span data-ttu-id="e12f2-137">256-par-64 image principale</span><span class="sxs-lookup"><span data-stu-id="e12f2-137">256-by-64 main image</span></span>   | <span data-ttu-id="e12f2-138">8 192</span><span class="sxs-lookup"><span data-stu-id="e12f2-138">8192</span></span>     |
| <span data-ttu-id="e12f2-139">image mipmap 128-par-32</span><span class="sxs-lookup"><span data-stu-id="e12f2-139">128-by-32 mipmap image</span></span> | <span data-ttu-id="e12f2-140">2 048</span><span class="sxs-lookup"><span data-stu-id="e12f2-140">2048</span></span>     |
| <span data-ttu-id="e12f2-141">image mipmap 64-par-16</span><span class="sxs-lookup"><span data-stu-id="e12f2-141">64-by-16 mipmap image</span></span>  | <span data-ttu-id="e12f2-142">512</span><span class="sxs-lookup"><span data-stu-id="e12f2-142">512</span></span>      |
| <span data-ttu-id="e12f2-143">image mipmap 32-par-8</span><span class="sxs-lookup"><span data-stu-id="e12f2-143">32-by-8 mipmap image</span></span>   | <span data-ttu-id="e12f2-144">128</span><span class="sxs-lookup"><span data-stu-id="e12f2-144">128</span></span>      |
| <span data-ttu-id="e12f2-145">image mipmap 16 par 4</span><span class="sxs-lookup"><span data-stu-id="e12f2-145">16-by-4 mipmap image</span></span>   | <span data-ttu-id="e12f2-146">32</span><span class="sxs-lookup"><span data-stu-id="e12f2-146">32</span></span>       |
| <span data-ttu-id="e12f2-147">image mipmap 8 par 2</span><span class="sxs-lookup"><span data-stu-id="e12f2-147">8-by-2 mipmap image</span></span>    | <span data-ttu-id="e12f2-148">16</span><span class="sxs-lookup"><span data-stu-id="e12f2-148">16</span></span>       |
| <span data-ttu-id="e12f2-149">image mipmap de 4 par 1</span><span class="sxs-lookup"><span data-stu-id="e12f2-149">4-by-1 mipmap image</span></span>    | <span data-ttu-id="e12f2-150">8</span><span class="sxs-lookup"><span data-stu-id="e12f2-150">8</span></span>        |
| <span data-ttu-id="e12f2-151">image mipmap 2 par 1</span><span class="sxs-lookup"><span data-stu-id="e12f2-151">2-by-1 mipmap image</span></span>    | <span data-ttu-id="e12f2-152">8</span><span class="sxs-lookup"><span data-stu-id="e12f2-152">8</span></span>        |
| <span data-ttu-id="e12f2-153">image mipmap 1-par-1</span><span class="sxs-lookup"><span data-stu-id="e12f2-153">1-by-1 mipmap image</span></span>    | <span data-ttu-id="e12f2-154">8</span><span class="sxs-lookup"><span data-stu-id="e12f2-154">8</span></span>        |



 

<span data-ttu-id="e12f2-155">Ce tableau répertorie la quantité d’espace occupée par chaque couche pour la même texture à l’aide d’un format de compression DXGI (dans ce cas BC3 \_ UNORM) qui requiert par conséquent l’en-tête étendu :</span><span class="sxs-lookup"><span data-stu-id="e12f2-155">This table lists the amount of space taken up by each layer for the same texture using a DXGI compression format (in this case BC3\_UNORM) that therefore requires the extended header:</span></span>



| <span data-ttu-id="e12f2-156">Composants DDS</span><span class="sxs-lookup"><span data-stu-id="e12f2-156">DDS Components</span></span>                                                | <span data-ttu-id="e12f2-157">\# Bits</span><span class="sxs-lookup"><span data-stu-id="e12f2-157">\# Bytes</span></span> |
|---------------------------------------------------------------|----------|
| <span data-ttu-id="e12f2-158">Header (FourCC défini sur « facilement »)</span><span class="sxs-lookup"><span data-stu-id="e12f2-158">header (FourCC set to "DX10")</span></span>                                 | <span data-ttu-id="e12f2-159">128</span><span class="sxs-lookup"><span data-stu-id="e12f2-159">128</span></span>      |
| <span data-ttu-id="e12f2-160">en-tête étendu (DXGI format défini au \_ format dxgi \_ BC3 \_ UNORM)</span><span class="sxs-lookup"><span data-stu-id="e12f2-160">extended header (DXGI format set to DXGI\_FORMAT\_BC3\_UNORM)</span></span> | <span data-ttu-id="e12f2-161">20</span><span class="sxs-lookup"><span data-stu-id="e12f2-161">20</span></span>       |
| <span data-ttu-id="e12f2-162">256-par-64 image principale</span><span class="sxs-lookup"><span data-stu-id="e12f2-162">256-by-64 main image</span></span>                                          | <span data-ttu-id="e12f2-163">16384</span><span class="sxs-lookup"><span data-stu-id="e12f2-163">16384</span></span>    |
| <span data-ttu-id="e12f2-164">image mipmap 128-par-32</span><span class="sxs-lookup"><span data-stu-id="e12f2-164">128-by-32 mipmap image</span></span>                                        | <span data-ttu-id="e12f2-165">4096</span><span class="sxs-lookup"><span data-stu-id="e12f2-165">4096</span></span>     |
| <span data-ttu-id="e12f2-166">image mipmap 64-par-16</span><span class="sxs-lookup"><span data-stu-id="e12f2-166">64-by-16 mipmap image</span></span>                                         | <span data-ttu-id="e12f2-167">1 024</span><span class="sxs-lookup"><span data-stu-id="e12f2-167">1024</span></span>     |
| <span data-ttu-id="e12f2-168">image mipmap 32-par-8</span><span class="sxs-lookup"><span data-stu-id="e12f2-168">32-by-8 mipmap image</span></span>                                          | <span data-ttu-id="e12f2-169">256</span><span class="sxs-lookup"><span data-stu-id="e12f2-169">256</span></span>      |
| <span data-ttu-id="e12f2-170">image mipmap 16 par 4</span><span class="sxs-lookup"><span data-stu-id="e12f2-170">16-by-4 mipmap image</span></span>                                          | <span data-ttu-id="e12f2-171">64</span><span class="sxs-lookup"><span data-stu-id="e12f2-171">64</span></span>       |
| <span data-ttu-id="e12f2-172">image mipmap 8 par 2</span><span class="sxs-lookup"><span data-stu-id="e12f2-172">8-by-2 mipmap image</span></span>                                           | <span data-ttu-id="e12f2-173">32</span><span class="sxs-lookup"><span data-stu-id="e12f2-173">32</span></span>       |
| <span data-ttu-id="e12f2-174">image mipmap de 4 par 1</span><span class="sxs-lookup"><span data-stu-id="e12f2-174">4-by-1 mipmap image</span></span>                                           | <span data-ttu-id="e12f2-175">16</span><span class="sxs-lookup"><span data-stu-id="e12f2-175">16</span></span>       |
| <span data-ttu-id="e12f2-176">image mipmap 2 par 1</span><span class="sxs-lookup"><span data-stu-id="e12f2-176">2-by-1 mipmap image</span></span>                                           | <span data-ttu-id="e12f2-177">16</span><span class="sxs-lookup"><span data-stu-id="e12f2-177">16</span></span>       |
| <span data-ttu-id="e12f2-178">image mipmap 1-par-1</span><span class="sxs-lookup"><span data-stu-id="e12f2-178">1-by-1 mipmap image</span></span>                                           | <span data-ttu-id="e12f2-179">16</span><span class="sxs-lookup"><span data-stu-id="e12f2-179">16</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="e12f2-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e12f2-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e12f2-181">Guide de programmation pour DDS</span><span class="sxs-lookup"><span data-stu-id="e12f2-181">Programming Guide for DDS</span></span>](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




