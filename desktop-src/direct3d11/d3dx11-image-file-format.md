---
title: Énumération D3DX11_IMAGE_FILE_FORMAT (D3DX11tex. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Formats de fichier image pris en charge par les fonctions D3DX11Createxxx et D3DX11Savexxx.'
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
ms.openlocfilehash: 1e34d3ab49987d499114c4b9eee695bfad02055fbbef785a955407e97843208f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536963"
---
# <a name="d3dx11_image_file_format-enumeration"></a>\_ \_ Énumération de format de fichier image D3DX11 \_

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Formats de fichier image pris en charge par les fonctions D3DX11Createxxx et D3DX11Savexxx.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_IFF_BMP"></span><span id="d3dx11_iff_bmp"></span>**D3DX11 \_ IFF \_ BMP**
</dt> <dd>

format de fichier BMP (Windows bitmap). Contient un en-tête qui décrit la résolution du périphérique sur lequel le rectangle de pixels a été créé, les dimensions du rectangle, la taille du tableau de bits, une palette logique et un tableau de bits qui définit la relation entre les pixels de l’image bitmap et les entrées de la palette logique. L’extension de fichier pour ce format est .bmp.

</dd> <dt>

<span id="D3DX11_IFF_JPG"></span><span id="d3dx11_iff_jpg"></span>**D3DX11 \_ IFF \_ jpg**
</dt> <dd>

Format de fichier compressé JPEG (Joint Photographic Experts Group). Spécifie la compression des variables des fichiers de document image TIFF (Tagged Image File Format) de 24 bits et de 8 bits. L’extension de fichier pour ce format est .jpg.

</dd> <dt>

<span id="D3DX11_IFF_PNG"></span><span id="d3dx11_iff_png"></span>**\_Png D3DX11 IFF \_**
</dt> <dd>

Format de fichier PNG (Portable Network Graphics). Format bitmap non propriétaire utilisant la compression sans perte. L’extension de fichier pour ce format est .png.

</dd> <dt>

<span id="D3DX11_IFF_DDS"></span><span id="d3dx11_iff_dds"></span>**D3DX11 \_ IFF \_ DDS**
</dt> <dd>

Format de fichier de la surface DirectDraw (DDS). Stocke les textures, les textures de volume et les mappages d’environnement cubique, avec ou sans niveaux de mipmap, avec ou sans compression de pixels. L’extension de fichier pour ce format est. DDS.

</dd> <dt>

<span id="D3DX11_IFF_TIFF"></span><span id="d3dx11_iff_tiff"></span>**\_TIFF D3DX11 IFF \_**
</dt> <dd>

TIFF (Tagged Image File Format). Les extensions de fichier pour ce format sont. TIF et. TIFF.

</dd> <dt>

<span id="D3DX11_IFF_GIF"></span><span id="d3dx11_iff_gif"></span>**\_Gif D3DX11 IFF \_**
</dt> <dd>

Format GIF (Graphics Interchange Format). L’extension de fichier pour ce format est .gif.

</dd> <dt>

<span id="D3DX11_IFF_WMP"></span><span id="d3dx11_iff_wmp"></span>**\_WMP D3DX11 IFF \_**
</dt> <dd>

Windows Media Photo format (WMP). Ce format est également appelé photo HD et JPEG XR. Les extensions de fichier pour ce format sont. HDP,. JXR et. WDP.

Pour fonctionner correctement, **D3DX11 \_ IFF \_ WMP** requiert l’initialisation de com. Par conséquent, appelez [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) dans votre application avant d’appeler D3DX.

</dd> <dt>

<span id="D3DX11_IFF_FORCE_DWORD"></span><span id="d3dx11_iff_force_dword"></span>**D3DX11 \_ IFF \_ force \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

pour plus d’informations sur certains de ces formats [, consultez Types de bitmaps (GDI+)](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

