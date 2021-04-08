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
# <a name="d3dx10_image_file_format-enumeration"></a>\_ \_ Énumération de format de fichier image d3dx10 \_

Formats de fichier image pris en charge par les fonctions D3DXCreatexxx et D3DX10Savexxx.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_IFF_BMP"></span><span id="d3dx10_iff_bmp"></span>**D3DX10 \_ IFF \_ BMP**
</dt> <dd>

Format de fichier bitmap Windows (BMP). Contient un en-tête qui décrit la résolution du périphérique sur lequel le rectangle de pixels a été créé, les dimensions du rectangle, la taille du tableau de bits, une palette logique et un tableau de bits qui définit la relation entre les pixels de l’image bitmap et les entrées de la palette logique. L’extension de fichier pour ce format est. bmp.

</dd> <dt>

<span id="D3DX10_IFF_JPG"></span><span id="d3dx10_iff_jpg"></span>**D3DX10 \_ IFF \_ jpg**
</dt> <dd>

Format de fichier compressé JPEG (Joint Photographic Experts Group). Spécifie la compression des variables des fichiers de document image TIFF (Tagged Image File Format) de 24 bits et de 8 bits. L’extension de fichier pour ce format est. jpg.

</dd> <dt>

<span id="D3DX10_IFF_PNG"></span><span id="d3dx10_iff_png"></span>**\_Png d3dx10 IFF \_**
</dt> <dd>

Format de fichier PNG (Portable Network Graphics). Format bitmap non propriétaire utilisant la compression sans perte. L’extension de fichier pour ce format est. png.

</dd> <dt>

<span id="D3DX10_IFF_DDS"></span><span id="d3dx10_iff_dds"></span>**D3DX10 \_ IFF \_ DDS**
</dt> <dd>

Format de fichier de la surface DirectDraw (DDS). Stocke les textures, les textures de volume et les mappages d’environnement cubique, avec ou sans niveaux de mipmap, avec ou sans compression de pixels. L’extension de fichier pour ce format est. DDS.

</dd> <dt>

<span id="D3DX10_IFF_TIFF"></span><span id="d3dx10_iff_tiff"></span>**\_TIFF d3dx10 IFF \_**
</dt> <dd>

TIFF (Tagged Image File Format). Les extensions de fichier pour ce format sont. TIF et. TIFF.

</dd> <dt>

<span id="D3DX10_IFF_GIF"></span><span id="d3dx10_iff_gif"></span>**\_Gif d3dx10 IFF \_**
</dt> <dd>

Format GIF (Graphics Interchange Format). L’extension de fichier pour ce format est. gif.

</dd> <dt>

<span id="D3DX10_IFF_WMP"></span><span id="d3dx10_iff_wmp"></span>**\_WMP d3dx10 IFF \_**
</dt> <dd>

Windows Media Photo format (WMP). Ce format est également appelé photo HD et JPEG XR. Les extensions de fichier pour ce format sont. HDP,. JXR et. WDP.

Pour fonctionner correctement, **d3dx10 \_ IFF \_ WMP** requiert l’initialisation de com. Par conséquent, appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) dans votre application avant d’appeler D3DX.

</dd> <dt>

<span id="D3DX10_IFF_FORCE_DWORD"></span><span id="d3dx10_iff_force_dword"></span>**D3DX10 \_ IFF \_ force \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour plus d’informations sur certains de ces formats, consultez [types de bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

D3DX10 utilise le composant de création d’images Windows pour implémenter la majorité des types de fichiers bitmap pris en charge. Pour plus d’informations, consultez [vue d’ensemble du composant de création d’images Windows](https://msdn.microsoft.com/library/ms737408.aspx) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 
