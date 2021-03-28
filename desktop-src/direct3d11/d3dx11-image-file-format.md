---
title: Énumération D3DX11_IMAGE_FILE_FORMAT (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Formats de fichier image pris en charge par les fonctions D3DX11Createxxx et D3DX11Savexxx.'
ms.assetid: 89fa9ab8-3be0-4dc5-a533-94edb01df36a
keywords:
- Énumération D3DX11_IMAGE_FILE_FORMAT Direct3D 11
- Pointeur d’énumération LPD3DX11_IMAGE_FILE_FORMAT Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_FILE_FORMAT
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730ce59bb8a07f3fd8ef78bbeb27b4d01d198f7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982570"
---
# <a name="d3dx11_image_file_format-enumeration"></a><span data-ttu-id="9f07c-106">\_ \_ Énumération de format de fichier image D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="9f07c-106">D3DX11\_IMAGE\_FILE\_FORMAT enumeration</span></span>

> [!Note]  
> <span data-ttu-id="9f07c-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9f07c-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="9f07c-108">Formats de fichier image pris en charge par les fonctions D3DX11Createxxx et D3DX11Savexxx.</span><span class="sxs-lookup"><span data-stu-id="9f07c-108">Image file formats supported by D3DX11Createxxx and D3DX11Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f07c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f07c-109">Syntax</span></span>


```C++
typedef enum D3DX11_IMAGE_FILE_FORMAT { 
  D3DX11_IFF_BMP          = 0,
  D3DX11_IFF_JPG          = 1,
  D3DX11_IFF_PNG          = 3,
  D3DX11_IFF_DDS          = 4,
  D3DX11_IFF_TIFF         = 10,
  D3DX11_IFF_GIF          = 11,
  D3DX11_IFF_WMP          = 12,
  D3DX11_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX11_IMAGE_FILE_FORMAT, *LPD3DX11_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="9f07c-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="9f07c-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9f07c-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="9f07c-111"><span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-112">Format de fichier bitmap Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="9f07c-112">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="9f07c-113">Contient un en-tête qui décrit la résolution du périphérique sur lequel le rectangle de pixels a été créé, les dimensions du rectangle, la taille du tableau de bits, une palette logique et un tableau de bits qui définit la relation entre les pixels de l’image bitmap et les entrées de la palette logique.</span><span class="sxs-lookup"><span data-stu-id="9f07c-113">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="9f07c-114">L’extension de fichier pour ce format est. bmp.</span><span class="sxs-lookup"><span data-stu-id="9f07c-114">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="9f07c-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="9f07c-115"><span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-116">Format de fichier compressé JPEG (Joint Photographic Experts Group).</span><span class="sxs-lookup"><span data-stu-id="9f07c-116">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="9f07c-117">Spécifie la compression des variables des fichiers de document image TIFF (Tagged Image File Format) de 24 bits et de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="9f07c-117">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="9f07c-118">L’extension de fichier pour ce format est. jpg.</span><span class="sxs-lookup"><span data-stu-id="9f07c-118">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="9f07c-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**\_Png D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="9f07c-119"><span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**D3DX11\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-120">Format de fichier PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="9f07c-120">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="9f07c-121">Format bitmap non propriétaire utilisant la compression sans perte.</span><span class="sxs-lookup"><span data-stu-id="9f07c-121">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="9f07c-122">L’extension de fichier pour ce format est. png.</span><span class="sxs-lookup"><span data-stu-id="9f07c-122">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="9f07c-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="9f07c-123"><span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-124">Format de fichier de la surface DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="9f07c-124">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="9f07c-125">Stocke les textures, les textures de volume et les mappages d’environnement cubique, avec ou sans niveaux de mipmap, avec ou sans compression de pixels.</span><span class="sxs-lookup"><span data-stu-id="9f07c-125">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="9f07c-126">L’extension de fichier pour ce format est. DDS.</span><span class="sxs-lookup"><span data-stu-id="9f07c-126">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="9f07c-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**\_TIFF D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="9f07c-127"><span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**D3DX11\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-128">TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="9f07c-128">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="9f07c-129">Les extensions de fichier pour ce format sont. TIF et. TIFF.</span><span class="sxs-lookup"><span data-stu-id="9f07c-129">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="9f07c-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**\_Gif D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="9f07c-130"><span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**D3DX11\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-131">Format GIF (Graphics Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="9f07c-131">Graphics Interchange Format (GIF).</span></span> <span data-ttu-id="9f07c-132">L’extension de fichier pour ce format est. gif.</span><span class="sxs-lookup"><span data-stu-id="9f07c-132">The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="9f07c-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**\_WMP D3DX11 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="9f07c-133"><span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**D3DX11\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-134">Windows Media Photo format (WMP).</span><span class="sxs-lookup"><span data-stu-id="9f07c-134">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="9f07c-135">Ce format est également appelé photo HD et JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="9f07c-135">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="9f07c-136">Les extensions de fichier pour ce format sont. HDP,. JXR et. WDP.</span><span class="sxs-lookup"><span data-stu-id="9f07c-136">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="9f07c-137">Pour fonctionner correctement, **D3DX11 \_ IFF \_ WMP** requiert l’initialisation de com.</span><span class="sxs-lookup"><span data-stu-id="9f07c-137">To work properly, **D3DX11\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="9f07c-138">Par conséquent, appelez [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) dans votre application avant d’appeler D3DX.</span><span class="sxs-lookup"><span data-stu-id="9f07c-138">Therefore, call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="9f07c-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9f07c-139"><span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="9f07c-140">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="9f07c-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="9f07c-141">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9f07c-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="9f07c-142">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="9f07c-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f07c-143">Notes</span><span class="sxs-lookup"><span data-stu-id="9f07c-143">Remarks</span></span>

<span data-ttu-id="9f07c-144">Pour plus d’informations sur certains de ces formats, consultez [types de bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="9f07c-144">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f07c-145">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9f07c-145">Requirements</span></span>



| <span data-ttu-id="9f07c-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f07c-146">Requirement</span></span> | <span data-ttu-id="9f07c-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f07c-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f07c-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f07c-148">Header</span></span><br/> | <dl> <span data-ttu-id="9f07c-149"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f07c-149"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f07c-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f07c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f07c-151">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="9f07c-151">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

