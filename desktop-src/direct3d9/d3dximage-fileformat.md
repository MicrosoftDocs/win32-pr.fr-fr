---
description: Décrit les formats de fichier image pris en charge. Consultez la section Notes pour obtenir une description de ces formats.
ms.assetid: 245a0052-f156-44ad-ab46-3677a818167e
title: Énumération D3DXIMAGE_FILEFORMAT (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_FILEFORMAT
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 3b1195e7503ff32e92cdbafde941b811dcf86427
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322909"
---
# <a name="d3dximage_fileformat-enumeration"></a><span data-ttu-id="55982-104">D3DXIMAGE \_ FILEFORMAT, énumération</span><span class="sxs-lookup"><span data-stu-id="55982-104">D3DXIMAGE\_FILEFORMAT enumeration</span></span>

<span data-ttu-id="55982-105">Décrit les formats de fichier image pris en charge.</span><span class="sxs-lookup"><span data-stu-id="55982-105">Describes the supported image file formats.</span></span> <span data-ttu-id="55982-106">Consultez la section Notes pour obtenir une description de ces formats.</span><span class="sxs-lookup"><span data-stu-id="55982-106">See Remarks for descriptions of these formats.</span></span>

## <a name="syntax"></a><span data-ttu-id="55982-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55982-107">Syntax</span></span>


```C++
typedef enum D3DXIMAGE_FILEFORMAT { 
  D3DXIFF_BMP          = 0,
  D3DXIFF_JPG          = 1,
  D3DXIFF_TGA          = 2,
  D3DXIFF_PNG          = 3,
  D3DXIFF_DDS          = 4,
  D3DXIFF_PPM          = 5,
  D3DXIFF_DIB          = 6,
  D3DXIFF_HDR          = 7,
  D3DXIFF_PFM          = 8,
  D3DXIFF_FORCE_DWORD  = 0x7fffffff
} D3DXIMAGE_FILEFORMAT, *LPD3DXIMAGE_FILEFORMAT;
```



## <a name="constants"></a><span data-ttu-id="55982-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="55982-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="55982-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="55982-109"><span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="55982-110">Format de fichier bitmap Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="55982-110">Windows bitmap (BMP) file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="55982-111"><span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="55982-112">Format de fichier compressé JPEG (Joint Photographic Experts Group).</span><span class="sxs-lookup"><span data-stu-id="55982-112">Joint Photographics Experts Group (JPEG) compressed file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**\_TGA D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="55982-113"><span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**D3DXIFF\_TGA**</span></span>
</dt> <dd>

<span data-ttu-id="55982-114">Format de fichier d’image Truevision (Targa ou TGA).</span><span class="sxs-lookup"><span data-stu-id="55982-114">Truevision (Targa, or TGA) image file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="55982-115"><span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="55982-116">Format de fichier PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="55982-116">Portable Network Graphics (PNG) file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="55982-117"><span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="55982-118">Format de fichier de la surface DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="55982-118">DirectDraw surface (DDS) file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**</span><span class="sxs-lookup"><span data-stu-id="55982-119"><span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF\_PPM**</span></span>
</dt> <dd>

<span data-ttu-id="55982-120">Format de fichier pixmap portable (PPM).</span><span class="sxs-lookup"><span data-stu-id="55982-120">Portable pixmap (PPM) file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**</span><span class="sxs-lookup"><span data-stu-id="55982-121"><span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF\_DIB**</span></span>
</dt> <dd>

<span data-ttu-id="55982-122">Format de fichier DIB (Device-Independent Bitmap) Windows.</span><span class="sxs-lookup"><span data-stu-id="55982-122">Windows device-independent bitmap (DIB) file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**\_HDR D3DXIFF**</span><span class="sxs-lookup"><span data-stu-id="55982-123"><span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**D3DXIFF\_HDR**</span></span>
</dt> <dd>

<span data-ttu-id="55982-124">Format de fichier HDR (High dynamique Range).</span><span class="sxs-lookup"><span data-stu-id="55982-124">High dynamic range (HDR) file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**</span><span class="sxs-lookup"><span data-stu-id="55982-125"><span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF\_PFM**</span></span>
</dt> <dd>

<span data-ttu-id="55982-126">Format de fichier de carte flottante portable.</span><span class="sxs-lookup"><span data-stu-id="55982-126">Portable float map file format.</span></span>

</dd> <dt>

<span data-ttu-id="55982-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="55982-127"><span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="55982-128">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="55982-128">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="55982-129">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="55982-129">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="55982-130">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="55982-130">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55982-131">Notes</span><span class="sxs-lookup"><span data-stu-id="55982-131">Remarks</span></span>

<span data-ttu-id="55982-132">Les fonctions qui commencent par D3DXLoadxxx prennent en charge tous les formats listés.</span><span class="sxs-lookup"><span data-stu-id="55982-132">Functions that begin with D3DXLoadxxx support all of the formats listed.</span></span> <span data-ttu-id="55982-133">Les fonctions qui commencent par D3DXSavexxx prennent en charge tous les formats énumérés, à l’exception des formats Truevision (. TGA) et portable pixmap (. ppm).</span><span class="sxs-lookup"><span data-stu-id="55982-133">Functions that begin with D3DXSavexxx support all of the formats listed except the Truevision (.tga) and portable pixmap (.ppm) formats.</span></span>

<span data-ttu-id="55982-134">Le tableau suivant répertorie les formats d’entrée et de sortie disponibles.</span><span class="sxs-lookup"><span data-stu-id="55982-134">The following table lists the available input and output formats.</span></span>



| <span data-ttu-id="55982-135">Extension de fichier</span><span class="sxs-lookup"><span data-stu-id="55982-135">File Extension</span></span> | <span data-ttu-id="55982-136">Description</span><span class="sxs-lookup"><span data-stu-id="55982-136">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55982-137">.bmp</span><span class="sxs-lookup"><span data-stu-id="55982-137">.bmp</span></span>           | <span data-ttu-id="55982-138">Format bitmap Windows.</span><span class="sxs-lookup"><span data-stu-id="55982-138">Windows bitmap format.</span></span> <span data-ttu-id="55982-139">Contient un en-tête qui décrit la résolution du périphérique sur lequel le rectangle de pixels a été créé, les dimensions du rectangle, la taille du tableau de bits, une palette logique et un tableau de bits qui définit la relation entre les pixels de l’image bitmap et les entrées de la palette logique.</span><span class="sxs-lookup"><span data-stu-id="55982-139">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> |
| <span data-ttu-id="55982-140">.dds</span><span class="sxs-lookup"><span data-stu-id="55982-140">.dds</span></span>           | <span data-ttu-id="55982-141">Format de fichier de surface DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="55982-141">DirectDraw Surface file format.</span></span> <span data-ttu-id="55982-142">Stocke les textures, les textures de volume et les mappages d’environnement cubique, avec ou sans niveaux de mipmap, avec ou sans compression de pixels.</span><span class="sxs-lookup"><span data-stu-id="55982-142">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="55982-143">Voir [DDS](../direct3ddds/dx-graphics-dds.md).</span><span class="sxs-lookup"><span data-stu-id="55982-143">See [DDS](../direct3ddds/dx-graphics-dds.md).</span></span>                                                                                                                                       |
| <span data-ttu-id="55982-144">.dib</span><span class="sxs-lookup"><span data-stu-id="55982-144">.dib</span></span>           | <span data-ttu-id="55982-145">DIB Windows.</span><span class="sxs-lookup"><span data-stu-id="55982-145">Windows DIB.</span></span> <span data-ttu-id="55982-146">Contient un tableau de bits associés à des structures qui spécifient la largeur et la hauteur de l’image bitmap, le format de couleur de l’appareil sur lequel l’image a été créée et la résolution de l’appareil utilisé pour créer cette image.</span><span class="sxs-lookup"><span data-stu-id="55982-146">Contains an array of bits combined with structures that specify width and height of the bitmapped image, color format of the device where the image was created, and resolution of the device used to create that image.</span></span>                                                                                                              |
| <span data-ttu-id="55982-147">. HDR</span><span class="sxs-lookup"><span data-stu-id="55982-147">.hdr</span></span>           | <span data-ttu-id="55982-148">Format HDR.</span><span class="sxs-lookup"><span data-stu-id="55982-148">HDR format.</span></span> <span data-ttu-id="55982-149">Encode chaque pixel sous la forme d’une couleur RGBE 32 bits, avec 8 bits de mantisse pour le rouge, le vert et le bleu, et un exposant 8 bits partagé.</span><span class="sxs-lookup"><span data-stu-id="55982-149">Encodes each pixel as an RGBE 32-bit color, with 8 bits of mantissa for red, green, and blue, and a shared 8-bit exponent.</span></span> <span data-ttu-id="55982-150">Chaque canal est compressé séparément avec l’encodage de longueur d’exécution (RLE).</span><span class="sxs-lookup"><span data-stu-id="55982-150">Each channel is separately compressed with run-length encoding (RLE).</span></span>                                                                                                                                       |
| <span data-ttu-id="55982-151">.jpg</span><span class="sxs-lookup"><span data-stu-id="55982-151">.jpg</span></span>           | <span data-ttu-id="55982-152">Norme JPEG.</span><span class="sxs-lookup"><span data-stu-id="55982-152">JPEG standard.</span></span> <span data-ttu-id="55982-153">Spécifie la compression des variables des fichiers de document image TIFF (Tagged Image File Format) de 24 bits et de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="55982-153">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="55982-154">. PFM</span><span class="sxs-lookup"><span data-stu-id="55982-154">.pfm</span></span>           | <span data-ttu-id="55982-155">Format de carte à virgule flottante portable.</span><span class="sxs-lookup"><span data-stu-id="55982-155">Portable float map format.</span></span> <span data-ttu-id="55982-156">Format d’image à virgule flottante brut, sans compression.</span><span class="sxs-lookup"><span data-stu-id="55982-156">A raw floating point image format, without any compression.</span></span> <span data-ttu-id="55982-157">L’en-tête de fichier spécifie la largeur de l’image, la hauteur, le monochrome ou la couleur et l’ordre des mots de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="55982-157">The file header specifies image width, height, monochrome or color, and machine word order.</span></span> <span data-ttu-id="55982-158">Les données de pixels sont stockées en tant que valeurs à virgule flottante 32 bits, avec 3 valeurs par pixel pour la couleur et une valeur par pixel pour monochrome.</span><span class="sxs-lookup"><span data-stu-id="55982-158">Pixel data is stored as 32-bit floating point values, with 3 values per pixel for color, and one value per pixel for monochrome.</span></span>                                |
| <span data-ttu-id="55982-159">.png</span><span class="sxs-lookup"><span data-stu-id="55982-159">.png</span></span>           | <span data-ttu-id="55982-160">Format PNG.</span><span class="sxs-lookup"><span data-stu-id="55982-160">PNG format.</span></span> <span data-ttu-id="55982-161">Format bitmap non propriétaire utilisant la compression sans perte.</span><span class="sxs-lookup"><span data-stu-id="55982-161">A non-proprietary bitmap format using lossless compression.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="55982-162">. ppm</span><span class="sxs-lookup"><span data-stu-id="55982-162">.ppm</span></span>           | <span data-ttu-id="55982-163">Format pixmap portable.</span><span class="sxs-lookup"><span data-stu-id="55982-163">Portable Pixmap format.</span></span> <span data-ttu-id="55982-164">Format de fichier binaire ou ASCII pour les images de couleur qui incluent la hauteur et la largeur de l’image et la valeur maximale du composant de couleur.</span><span class="sxs-lookup"><span data-stu-id="55982-164">A binary or ASCII file format for color images that includes image height and width and the maximum color component value.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="55982-165">.tga</span><span class="sxs-lookup"><span data-stu-id="55982-165">.tga</span></span>           | <span data-ttu-id="55982-166">Format de carte graphique Targa ou Truevision.</span><span class="sxs-lookup"><span data-stu-id="55982-166">Targa or Truevision Graphics Adapter format.</span></span> <span data-ttu-id="55982-167">Prend en charge des profondeurs de 8, 15, 16, 24 et 32 bits, y compris l’échelle grise de 8 bits, et contient des données de palette de couleurs facultatives, des données d’origine et de taille d’image (x, y) et des données de pixels.</span><span class="sxs-lookup"><span data-stu-id="55982-167">Supports depths of 8, 15, 16, 24, and 32 bits, including 8-bit gray scale, and contains optional color palette data, image (x, y) origin and size data, and pixel data.</span></span>                                                                                                                               |



 

<span data-ttu-id="55982-168">Pour plus d’informations sur certains de ces formats, consultez [types de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="55982-168">See [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="55982-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55982-169">Requirements</span></span>



| <span data-ttu-id="55982-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55982-170">Requirement</span></span> | <span data-ttu-id="55982-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="55982-171">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55982-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="55982-172">Header</span></span><br/> | <dl> <span data-ttu-id="55982-173"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="55982-173"><dt>D3dx9tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55982-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55982-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55982-175">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="55982-175">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
