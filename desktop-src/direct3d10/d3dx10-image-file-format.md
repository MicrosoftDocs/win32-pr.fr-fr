---
description: Formats de fichier image pris en charge par les fonctions D3DXCreatexxx et D3DX10Savexxx.
ms.assetid: 39602f3c-5c91-4667-96d0-c3bdba712d88
title: Énumération D3DX10_IMAGE_FILE_FORMAT (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_FILE_FORMAT
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: fba878a40f510cc5e76256161255e01deaa7ee04
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762260"
---
# <a name="d3dx10_image_file_format-enumeration"></a><span data-ttu-id="2649a-103">\_ \_ Énumération de format de fichier image d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="2649a-103">D3DX10\_IMAGE\_FILE\_FORMAT enumeration</span></span>

<span data-ttu-id="2649a-104">Formats de fichier image pris en charge par les fonctions D3DXCreatexxx et D3DX10Savexxx.</span><span class="sxs-lookup"><span data-stu-id="2649a-104">Image file formats supported by D3DXCreatexxx and D3DX10Savexxx functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2649a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2649a-105">Syntax</span></span>


```C++
typedef enum D3DX10_IMAGE_FILE_FORMAT { 
  D3DX10_IFF_BMP          = 0,
  D3DX10_IFF_JPG          = 1,
  D3DX10_IFF_PNG          = 3,
  D3DX10_IFF_DDS          = 4,
  D3DX10_IFF_TIFF         = 10,
  D3DX10_IFF_GIF          = 11,
  D3DX10_IFF_WMP          = 12,
  D3DX10_IFF_FORCE_DWORD  = 0x7fffffff
} D3DX10_IMAGE_FILE_FORMAT, *LPD3DX10_IMAGE_FILE_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="2649a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="2649a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2649a-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="2649a-107"><span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10\_IFF\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-108">Format de fichier bitmap Windows (BMP).</span><span class="sxs-lookup"><span data-stu-id="2649a-108">Windows bitmap (BMP) file format.</span></span> <span data-ttu-id="2649a-109">Contient un en-tête qui décrit la résolution du périphérique sur lequel le rectangle de pixels a été créé, les dimensions du rectangle, la taille du tableau de bits, une palette logique et un tableau de bits qui définit la relation entre les pixels de l’image bitmap et les entrées de la palette logique.</span><span class="sxs-lookup"><span data-stu-id="2649a-109">Contains a header that describes the resolution of the device on which the rectangle of pixels was created, the dimensions of the rectangle, the size of the array of bits, a logical palette, and an array of bits that defines the relationship between pixels in the bitmapped image and entries in the logical palette.</span></span> <span data-ttu-id="2649a-110">L’extension de fichier pour ce format est. bmp.</span><span class="sxs-lookup"><span data-stu-id="2649a-110">The file extension for this format is .bmp.</span></span>

</dd> <dt>

<span data-ttu-id="2649a-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ jpg**</span><span class="sxs-lookup"><span data-stu-id="2649a-111"><span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10\_IFF\_JPG**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-112">Format de fichier compressé JPEG (Joint Photographic Experts Group).</span><span class="sxs-lookup"><span data-stu-id="2649a-112">Joint Photographic Experts Group (JPEG) compressed file format.</span></span> <span data-ttu-id="2649a-113">Spécifie la compression des variables des fichiers de document image TIFF (Tagged Image File Format) de 24 bits et de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="2649a-113">Specifies variable compression of 24-bit RGB color and 8-bit gray-scale Tagged Image File Format (TIFF) image document files.</span></span> <span data-ttu-id="2649a-114">L’extension de fichier pour ce format est. jpg.</span><span class="sxs-lookup"><span data-stu-id="2649a-114">The file extension for this format is .jpg.</span></span>

</dd> <dt>

<span data-ttu-id="2649a-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**\_Png d3dx10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="2649a-115"><span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**D3DX10\_IFF\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-116">Format de fichier PNG (Portable Network Graphics).</span><span class="sxs-lookup"><span data-stu-id="2649a-116">Portable Network Graphics (PNG) file format.</span></span> <span data-ttu-id="2649a-117">Format bitmap non propriétaire utilisant la compression sans perte.</span><span class="sxs-lookup"><span data-stu-id="2649a-117">A non-proprietary bitmap format using lossless compression.</span></span> <span data-ttu-id="2649a-118">L’extension de fichier pour ce format est. png.</span><span class="sxs-lookup"><span data-stu-id="2649a-118">The file extension for this format is .png.</span></span>

</dd> <dt>

<span data-ttu-id="2649a-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF \_ DDS**</span><span class="sxs-lookup"><span data-stu-id="2649a-119"><span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10\_IFF\_DDS**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-120">Format de fichier de la surface DirectDraw (DDS).</span><span class="sxs-lookup"><span data-stu-id="2649a-120">DirectDraw surface (DDS) file format.</span></span> <span data-ttu-id="2649a-121">Stocke les textures, les textures de volume et les mappages d’environnement cubique, avec ou sans niveaux de mipmap, avec ou sans compression de pixels.</span><span class="sxs-lookup"><span data-stu-id="2649a-121">Stores textures, volume textures, and cubic environment maps, with or without mipmap levels, and with or without pixel compression.</span></span> <span data-ttu-id="2649a-122">L’extension de fichier pour ce format est. DDS.</span><span class="sxs-lookup"><span data-stu-id="2649a-122">The file extension for this format is .dds.</span></span>

</dd> <dt>

<span data-ttu-id="2649a-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**\_TIFF d3dx10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="2649a-123"><span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**D3DX10\_IFF\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-124">TIFF (Tagged Image File Format).</span><span class="sxs-lookup"><span data-stu-id="2649a-124">Tagged Image File Format (TIFF).</span></span> <span data-ttu-id="2649a-125">Les extensions de fichier pour ce format sont. TIF et. TIFF.</span><span class="sxs-lookup"><span data-stu-id="2649a-125">The file extensions for this format are .tif and .tiff.</span></span>

</dd> <dt>

<span data-ttu-id="2649a-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**\_Gif d3dx10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="2649a-126"><span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**D3DX10\_IFF\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-127">Format GIF (Graphics Interchange Format). L’extension de fichier pour ce format est. gif.</span><span class="sxs-lookup"><span data-stu-id="2649a-127">Graphics Interchange Format (GIF).The file extension for this format is .gif.</span></span>

</dd> <dt>

<span data-ttu-id="2649a-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**\_WMP d3dx10 IFF \_**</span><span class="sxs-lookup"><span data-stu-id="2649a-128"><span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**D3DX10\_IFF\_WMP**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-129">Windows Media Photo format (WMP).</span><span class="sxs-lookup"><span data-stu-id="2649a-129">Windows Media Photo format (WMP).</span></span> <span data-ttu-id="2649a-130">Ce format est également appelé photo HD et JPEG XR.</span><span class="sxs-lookup"><span data-stu-id="2649a-130">This format is also known as HD Photo and JPEG XR.</span></span> <span data-ttu-id="2649a-131">Les extensions de fichier pour ce format sont. HDP,. JXR et. WDP.</span><span class="sxs-lookup"><span data-stu-id="2649a-131">The file extensions for this format are .hdp, .jxr, and .wdp.</span></span>

<span data-ttu-id="2649a-132">Pour fonctionner correctement, **d3dx10 \_ IFF \_ WMP** requiert l’initialisation de com.</span><span class="sxs-lookup"><span data-stu-id="2649a-132">To work properly, **D3DX10\_IFF\_WMP** requires that you initialize COM.</span></span> <span data-ttu-id="2649a-133">Par conséquent, appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) dans votre application avant d’appeler D3DX.</span><span class="sxs-lookup"><span data-stu-id="2649a-133">Therefore, call [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) in your application before you call D3DX.</span></span>

</dd> <dt>

<span data-ttu-id="2649a-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2649a-134"><span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10\_IFF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2649a-135">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="2649a-135">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2649a-136">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2649a-136">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2649a-137">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="2649a-137">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2649a-138">Notes</span><span class="sxs-lookup"><span data-stu-id="2649a-138">Remarks</span></span>

<span data-ttu-id="2649a-139">Pour plus d’informations sur certains de ces formats, consultez [types de bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .</span><span class="sxs-lookup"><span data-stu-id="2649a-139">See [Types of Bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) for more information on some of these formats.</span></span>

<span data-ttu-id="2649a-140">D3DX10 utilise le composant de création d’images Windows pour implémenter la majorité des types de fichiers bitmap pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2649a-140">D3DX10 makes use of the Windows Imaging Component to implement the majority of the supported bitmap file types.</span></span> <span data-ttu-id="2649a-141">Pour plus d’informations, consultez [vue d’ensemble du composant de création d’images Windows](https://msdn.microsoft.com/library/ms737408.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2649a-141">See [Windows Imaging Component Overview](https://msdn.microsoft.com/library/ms737408.aspx) for additional information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2649a-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2649a-142">Requirements</span></span>



| <span data-ttu-id="2649a-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2649a-143">Requirement</span></span> | <span data-ttu-id="2649a-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="2649a-144">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2649a-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="2649a-145">Header</span></span><br/> | <dl> <span data-ttu-id="2649a-146"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="2649a-146"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2649a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2649a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2649a-148">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="2649a-148">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
