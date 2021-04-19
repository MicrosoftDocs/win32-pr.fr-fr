---
title: Structure _BITMAPINFOHEADER
description: La \_ structure BITMAPINFOHEADER définit le format d’une image vidéo.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Structure de _BITMAPINFOHEADER Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526631"
---
# <a name="_bitmapinfoheader-structure"></a><span data-ttu-id="37a98-104">\_BITMAPINFOHEADER, structure</span><span class="sxs-lookup"><span data-stu-id="37a98-104">\_BITMAPINFOHEADER structure</span></span>

<span data-ttu-id="37a98-105">La structure **\_ BITMAPINFOHEADER** définit le format d’une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="37a98-105">The **\_BITMAPINFOHEADER** structure defines the format of a video frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a98-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37a98-106">Syntax</span></span>


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="37a98-107">Membres</span><span class="sxs-lookup"><span data-stu-id="37a98-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="37a98-108">**bisize**</span><span class="sxs-lookup"><span data-stu-id="37a98-108">**biSize**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-109">Spécifie le nombre d’octets requis par la structure.</span><span class="sxs-lookup"><span data-stu-id="37a98-109">Specifies the number of bytes required by the structure.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-110">**bichasse**</span><span class="sxs-lookup"><span data-stu-id="37a98-110">**biWidth**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-111">Spécifie la largeur de l’image bitmap, en pixels.</span><span class="sxs-lookup"><span data-stu-id="37a98-111">Specifies the width of the bitmap, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-112">**bihauteur**</span><span class="sxs-lookup"><span data-stu-id="37a98-112">**biHeight**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-113">Spécifie la hauteur, en pixels, de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="37a98-113">Specifies the height of the bitmap, in pixels.</span></span> <span data-ttu-id="37a98-114">Si la **bihauteur** est positive, le bitmap est un DIB ascendant et son origine est l’angle inférieur gauche.</span><span class="sxs-lookup"><span data-stu-id="37a98-114">If **biHeight** is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner.</span></span> <span data-ttu-id="37a98-115">Si la valeur **bihauteur** est négative, l’image bitmap est un DIB descendant et son origine est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="37a98-115">If **biHeight** is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.</span></span> <span data-ttu-id="37a98-116">Si la **bihauteur** est négative, ce qui indique un DIB de haut en haut, la **compression** doit être de type de bits \_ RVB bi ou bi \_ .</span><span class="sxs-lookup"><span data-stu-id="37a98-116">If **biHeight** is negative, indicating a top-down DIB, **biCompression** must be either BI\_RGB or BI\_BITFIELDS.</span></span> <span data-ttu-id="37a98-117">Les DIB descendants ne peuvent pas être compressés.</span><span class="sxs-lookup"><span data-stu-id="37a98-117">Top-down DIBs cannot be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-118">**biplans**</span><span class="sxs-lookup"><span data-stu-id="37a98-118">**biPlanes**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-119">Spécifie le nombre de plans pour l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="37a98-119">Specifies the number of planes for the target device.</span></span> <span data-ttu-id="37a98-120">Cette valeur doit être définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="37a98-120">This value must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-121">**biBitCount**</span><span class="sxs-lookup"><span data-stu-id="37a98-121">**biBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-122">Spécifie le nombre de bits par pixel.</span><span class="sxs-lookup"><span data-stu-id="37a98-122">Specifies the number of bits per pixel.</span></span> <span data-ttu-id="37a98-123">Le membre **biBitCount** de la structure **BITMAPINFOHEADER** détermine le nombre de bits qui définissent chaque pixel et le nombre maximal de couleurs dans l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="37a98-123">The **biBitCount** member of the **BITMAPINFOHEADER** structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap.</span></span> <span data-ttu-id="37a98-124">Ce membre doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="37a98-124">This member must be one of the following values.</span></span>



| <span data-ttu-id="37a98-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="37a98-125">Value</span></span> | <span data-ttu-id="37a98-126">Description</span><span class="sxs-lookup"><span data-stu-id="37a98-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a98-127">1</span><span class="sxs-lookup"><span data-stu-id="37a98-127">1</span></span>     | <span data-ttu-id="37a98-128">La bitmap est monochrome et le membre bmiColors contient deux entrées.</span><span class="sxs-lookup"><span data-stu-id="37a98-128">The bitmap is monochrome, and the bmiColors member contains two entries.</span></span> <span data-ttu-id="37a98-129">Chaque bit du tableau de bitmaps représente un pixel.</span><span class="sxs-lookup"><span data-stu-id="37a98-129">Each bit in the bitmap array represents a pixel.</span></span> <span data-ttu-id="37a98-130">Si le bit est clair, le pixel est affiché avec la couleur de la première entrée dans la table bmiColors ; Si le bit est défini, le pixel a la couleur de la deuxième entrée dans la table.</span><span class="sxs-lookup"><span data-stu-id="37a98-130">If the bit is clear, the pixel is displayed with the color of the first entry in the bmiColors table; if the bit is set, the pixel has the color of the second entry in the table.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="37a98-131">2</span><span class="sxs-lookup"><span data-stu-id="37a98-131">2</span></span>     | <span data-ttu-id="37a98-132">La bitmap possède quatre valeurs de couleur possibles.</span><span class="sxs-lookup"><span data-stu-id="37a98-132">The bitmap has four possible color values.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="37a98-133">4</span><span class="sxs-lookup"><span data-stu-id="37a98-133">4</span></span>     | <span data-ttu-id="37a98-134">La bitmap a un maximum de 16 couleurs, et le membre bmiColors contient jusqu’à 16 entrées.</span><span class="sxs-lookup"><span data-stu-id="37a98-134">The bitmap has a maximum of 16 colors, and the bmiColors member contains up to 16 entries.</span></span> <span data-ttu-id="37a98-135">Chaque pixel de la bitmap est représenté par un index 4 bits dans la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="37a98-135">Each pixel in the bitmap is represented by a 4-bit index into the color table.</span></span> <span data-ttu-id="37a98-136">Par exemple, si le premier octet de la bitmap est 0x1F, l’octet représente deux pixels.</span><span class="sxs-lookup"><span data-stu-id="37a98-136">For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels.</span></span> <span data-ttu-id="37a98-137">Le premier pixel contient la couleur de la deuxième entrée de la table, tandis que le deuxième pixel contient la couleur dans le seizième entrée de la table.</span><span class="sxs-lookup"><span data-stu-id="37a98-137">The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="37a98-138">8</span><span class="sxs-lookup"><span data-stu-id="37a98-138">8</span></span>     | <span data-ttu-id="37a98-139">La bitmap a un maximum de 256 couleurs et le membre bmiColors contient jusqu’à 256 entrées.</span><span class="sxs-lookup"><span data-stu-id="37a98-139">The bitmap has a maximum of 256 colors, and the bmiColors member contains up to 256 entries.</span></span> <span data-ttu-id="37a98-140">Dans ce cas, chaque octet du tableau représente un pixel unique.</span><span class="sxs-lookup"><span data-stu-id="37a98-140">In this case, each byte in the array represents a single pixel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="37a98-141">16</span><span class="sxs-lookup"><span data-stu-id="37a98-141">16</span></span>    | <span data-ttu-id="37a98-142">La bitmap a un maximum de 2 ^ 16 couleurs.</span><span class="sxs-lookup"><span data-stu-id="37a98-142">The bitmap has a maximum of 2^16 colors.</span></span> <span data-ttu-id="37a98-143">Si le membre de bicompression de l’BITMAPINFOHEADER est BI \_ RGB, le membre bmiColors est **null**.</span><span class="sxs-lookup"><span data-stu-id="37a98-143">If the biCompression member of the BITMAPINFOHEADER is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="37a98-144">Chaque mot du tableau de bitmaps représente un pixel unique.</span><span class="sxs-lookup"><span data-stu-id="37a98-144">Each WORD in the bitmap array represents a single pixel.</span></span> <span data-ttu-id="37a98-145">Les inintensités relatives de rouge, de vert et de bleu sont représentées par 5 bits pour chaque composant de couleur.</span><span class="sxs-lookup"><span data-stu-id="37a98-145">The relative intensities of red, green, and blue are represented with 5 bits for each color component.</span></span> <span data-ttu-id="37a98-146">La valeur du bleu est comprise dans les 5 bits les moins significatifs, suivis de 5 bits chacun pour le vert et le rouge.</span><span class="sxs-lookup"><span data-stu-id="37a98-146">The value for blue is in the least significant 5 bits, followed by 5 bits each for green and red.</span></span> <span data-ttu-id="37a98-147">Le bit le plus significatif n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="37a98-147">The most significant bit is not used.</span></span> <span data-ttu-id="37a98-148">La table de couleurs bmiColors est utilisée pour optimiser les couleurs utilisées sur les appareils basés sur une palette et doit contenir le nombre d’entrées spécifié par le membre biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="37a98-148">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span> |
| <span data-ttu-id="37a98-149">24</span><span class="sxs-lookup"><span data-stu-id="37a98-149">24</span></span>    | <span data-ttu-id="37a98-150">La bitmap a un maximum de 2 ^ 24 couleurs et le membre bmiColors a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="37a98-150">The bitmap has a maximum of 2^24 colors, and the bmiColors member is **NULL**.</span></span> <span data-ttu-id="37a98-151">Chaque triplet de 3 octets dans le tableau de bitmaps représente les indizaines relatives de bleu, vert et rouge, respectivement, pour un pixel.</span><span class="sxs-lookup"><span data-stu-id="37a98-151">Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="37a98-152">La table de couleurs bmiColors est utilisée pour optimiser les couleurs utilisées sur les appareils basés sur une palette et doit contenir le nombre d’entrées spécifié par le membre biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="37a98-152">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="37a98-153">32</span><span class="sxs-lookup"><span data-stu-id="37a98-153">32</span></span>    | <span data-ttu-id="37a98-154">La bitmap a un maximum de 2 ^ 32 couleurs.</span><span class="sxs-lookup"><span data-stu-id="37a98-154">The bitmap has a maximum of 2^32 colors.</span></span> <span data-ttu-id="37a98-155">Si le membre de bicompression est BI \_ RGB, le membre bmiColors a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="37a98-155">If the biCompression member is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="37a98-156">Chaque DWORD dans le tableau de bitmaps représente les indizaines relatives de bleu, vert et rouge, respectivement, pour un pixel.</span><span class="sxs-lookup"><span data-stu-id="37a98-156">Each DWORD in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="37a98-157">L’octet de poids fort de chaque DWORD n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="37a98-157">The high byte in each DWORD is not used.</span></span> <span data-ttu-id="37a98-158">La table de couleurs bmiColors est utilisée pour optimiser les couleurs utilisées sur les appareils basés sur une palette et doit contenir le nombre d’entrées spécifié par le membre biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="37a98-158">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="37a98-159">**Compression**</span><span class="sxs-lookup"><span data-stu-id="37a98-159">**biCompression**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-160">Spécifie le type de compression d’une image bitmap ascendante compressée (les DIB descendants ne peuvent pas être compressés).</span><span class="sxs-lookup"><span data-stu-id="37a98-160">Specifies the type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed).</span></span> <span data-ttu-id="37a98-161">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="37a98-161">This member can be the one of the following values.</span></span>



| <span data-ttu-id="37a98-162">Valeur</span><span class="sxs-lookup"><span data-stu-id="37a98-162">Value</span></span>         | <span data-ttu-id="37a98-163">Description</span><span class="sxs-lookup"><span data-stu-id="37a98-163">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a98-164">\_RGB bi</span><span class="sxs-lookup"><span data-stu-id="37a98-164">BI\_RGB</span></span>       | <span data-ttu-id="37a98-165">Format non compressé.</span><span class="sxs-lookup"><span data-stu-id="37a98-165">An uncompressed format.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="37a98-166">champs de \_ passe bi</span><span class="sxs-lookup"><span data-stu-id="37a98-166">BI\_BITFIELDS</span></span> | <span data-ttu-id="37a98-167">Spécifie que l’image bitmap n’est pas compressée et que la table des couleurs est composée de trois masques de couleur DWORD qui spécifient respectivement les composants rouge, vert et bleu de chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="37a98-167">Specifies that the bitmap is not compressed and that the color table consists of three DWORD color masks that specify the red, green, and blue components, respectively, of each pixel.</span></span> <span data-ttu-id="37a98-168">Cela est valide lorsqu’il est utilisé avec des bitmaps 16-bpp et 32-BPP.</span><span class="sxs-lookup"><span data-stu-id="37a98-168">This is valid when used with 16-bpp and 32-bpp bitmaps.</span></span> <span data-ttu-id="37a98-169">Cette valeur est valide dans Microsoft Windows CE version 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="37a98-169">This value is valid in Microsoft Windows CE version 2.0 and later.</span></span> |



 

</dd> <dt>

<span data-ttu-id="37a98-170">**biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="37a98-170">**biSizeImage**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-171">Spécifie la taille de l’image, en octets.</span><span class="sxs-lookup"><span data-stu-id="37a98-171">Specifies the size of the image, in bytes.</span></span> <span data-ttu-id="37a98-172">Cette valeur peut être définie sur zéro pour les \_ bitmaps RGB bi.</span><span class="sxs-lookup"><span data-stu-id="37a98-172">This may be set to zero for BI\_RGB bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-173">**biXPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="37a98-173">**biXPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-174">Spécifie la résolution horizontale, en pixels par mètre, de l’appareil cible pour l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="37a98-174">Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.</span></span> <span data-ttu-id="37a98-175">Une application peut utiliser cette valeur pour sélectionner une image bitmap d’un groupe de ressources qui correspond le mieux aux caractéristiques de l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="37a98-175">An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-176">**biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="37a98-176">**biYPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-177">Spécifie la résolution verticale, en pixels par mètre, de l’appareil cible pour l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="37a98-177">Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-178">**biClrUsed**</span><span class="sxs-lookup"><span data-stu-id="37a98-178">**biClrUsed**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-179">Spécifie le nombre d’index de couleurs qui sont réellement utilisés par la bitmap dans la table des couleurs.</span><span class="sxs-lookup"><span data-stu-id="37a98-179">Specifies the number of color indexes in the color table that are actually used by the bitmap.</span></span> <span data-ttu-id="37a98-180">Si cette valeur est égale à zéro, la bitmap utilise le nombre maximal de couleurs correspondant à la valeur du membre **biBitCount** pour le mode de compression spécifié par la **compression**.</span><span class="sxs-lookup"><span data-stu-id="37a98-180">If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the **biBitCount** member for the compression mode specified by **biCompression**.</span></span>

</dd> <dt>

<span data-ttu-id="37a98-181">**biClrImportant**</span><span class="sxs-lookup"><span data-stu-id="37a98-181">**biClrImportant**</span></span>
</dt> <dd>

<span data-ttu-id="37a98-182">Spécifie le nombre d’index de couleurs requis pour l’affichage de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="37a98-182">Specifies the number of color indexes required for displaying the bitmap.</span></span> <span data-ttu-id="37a98-183">Si cette valeur est égale à zéro, toutes les couleurs sont requises.</span><span class="sxs-lookup"><span data-stu-id="37a98-183">If this value is zero, all colors are required.</span></span>

<span data-ttu-id="37a98-184">Si biClrUsed est différent de zéro et que le membre biBitCount est inférieur à 16, le membre biClrUsed spécifie le nombre réel de couleurs auxquelles le moteur graphique ou le pilote de périphérique accède.</span><span class="sxs-lookup"><span data-stu-id="37a98-184">If biClrUsed is nonzero and the biBitCount member is less than 16, the biClrUsed member specifies the actual number of colors the graphics engine or device driver accesses.</span></span> <span data-ttu-id="37a98-185">Si biBitCount a une valeur supérieure ou égale à 16, le membre biClrUsed spécifie la taille de la table de couleurs utilisée pour optimiser les performances des palettes de couleurs système.</span><span class="sxs-lookup"><span data-stu-id="37a98-185">If biBitCount is 16 or greater, the biClrUsed member specifies the size of the color table used to optimize performance of the system color palettes.</span></span> <span data-ttu-id="37a98-186">Si biBitCount est égal à 16 ou 32, la palette de couleurs optimale commence immédiatement après les trois masques DWORD.</span><span class="sxs-lookup"><span data-stu-id="37a98-186">If biBitCount equals 16 or 32, the optimal color palette starts immediately following the three DWORD masks.</span></span>

<span data-ttu-id="37a98-187">Si la bitmap est un bitmap condensé (une image bitmap dans laquelle le tableau bitmap suit immédiatement la \_ structure BITMAPINFOHEADER et est référencé par un pointeur unique), le membre biClrUsed doit être égal à zéro ou à la taille réelle de la table de couleurs.</span><span class="sxs-lookup"><span data-stu-id="37a98-187">If the bitmap is a packed bitmap (a bitmap in which the bitmap array immediately follows the \_BITMAPINFOHEADER structure and is referenced by a single pointer), the biClrUsed member must be either zero or the actual size of the color table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37a98-188">Notes</span><span class="sxs-lookup"><span data-stu-id="37a98-188">Remarks</span></span>

<span data-ttu-id="37a98-189">Cette structure est contenue dans une structure **\_ VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="37a98-189">This structure is contained within a **\_VIDEOINFOHEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="37a98-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37a98-190">Requirements</span></span>



| <span data-ttu-id="37a98-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37a98-191">Requirement</span></span> | <span data-ttu-id="37a98-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="37a98-192">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="37a98-193">En-tête</span><span class="sxs-lookup"><span data-stu-id="37a98-193">Header</span></span><br/> | <dl> <span data-ttu-id="37a98-194"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37a98-194"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a98-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37a98-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a98-196">**Structures**</span><span class="sxs-lookup"><span data-stu-id="37a98-196">**Structures**</span></span>](structures.md)
</dt> <dt>

[<span data-ttu-id="37a98-197">**\_VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="37a98-197">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)
</dt> </dl>

 

 





