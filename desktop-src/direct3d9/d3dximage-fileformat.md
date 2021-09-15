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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520516"
---
# <a name="d3dximage_fileformat-enumeration"></a>D3DXIMAGE \_ FILEFORMAT, énumération

Décrit les formats de fichier image pris en charge. Consultez la section Notes pour obtenir une description de ces formats.

## <a name="syntax"></a>Syntaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXIFF_BMP"></span><span id="d3dxiff_bmp"></span>**D3DXIFF \_ BMP**
</dt> <dd>

format de fichier BMP (Windows bitmap).

</dd> <dt>

<span id="D3DXIFF_JPG"></span><span id="d3dxiff_jpg"></span>**D3DXIFF \_ jpg**
</dt> <dd>

Format de fichier compressé JPEG (Joint Photographic Experts Group).

</dd> <dt>

<span id="D3DXIFF_TGA"></span><span id="d3dxiff_tga"></span>**\_TGA D3DXIFF**
</dt> <dd>

Format de fichier d’image Truevision (Targa ou TGA).

</dd> <dt>

<span id="D3DXIFF_PNG"></span><span id="d3dxiff_png"></span>**D3DXIFF \_ PNG**
</dt> <dd>

Format de fichier PNG (Portable Network Graphics).

</dd> <dt>

<span id="D3DXIFF_DDS"></span><span id="d3dxiff_dds"></span>**D3DXIFF \_ DDS**
</dt> <dd>

Format de fichier de la surface DirectDraw (DDS).

</dd> <dt>

<span id="D3DXIFF_PPM"></span><span id="d3dxiff_ppm"></span>**D3DXIFF \_ ppm**
</dt> <dd>

format de fichier pixmap Portable (PPM).

</dd> <dt>

<span id="D3DXIFF_DIB"></span><span id="d3dxiff_dib"></span>**D3DXIFF \_ DIB**
</dt> <dd>

Windows format de fichier DIB (device-independent bitmap).

</dd> <dt>

<span id="D3DXIFF_HDR"></span><span id="d3dxiff_hdr"></span>**\_HDR D3DXIFF**
</dt> <dd>

Format de fichier HDR (High dynamique Range).

</dd> <dt>

<span id="D3DXIFF_PFM"></span><span id="d3dxiff_pfm"></span>**D3DXIFF \_ PFM**
</dt> <dd>

Format de fichier de carte flottante portable.

</dd> <dt>

<span id="D3DXIFF_FORCE_DWORD"></span><span id="d3dxiff_force_dword"></span>**D3DXIFF \_ forcer \_ DWORD**
</dt> <dd>

Force cette énumération à se compiler à 32 bits de taille. Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits. Cette valeur n'est pas utilisée.

</dd> </dl>

## <a name="remarks"></a>Notes

Les fonctions qui commencent par D3DXLoadxxx prennent en charge tous les formats listés. Les fonctions qui commencent par D3DXSavexxx prennent en charge tous les formats énumérés, à l’exception des formats Truevision (. TGA) et portable pixmap (. ppm).

Le tableau suivant répertorie les formats d’entrée et de sortie disponibles.



| Extension de fichier | Description                                                                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bmp           | format bitmap Windows. Contient un en-tête qui décrit la résolution du périphérique sur lequel le rectangle de pixels a été créé, les dimensions du rectangle, la taille du tableau de bits, une palette logique et un tableau de bits qui définit la relation entre les pixels de l’image bitmap et les entrées de la palette logique. |
| .dds           | Format de fichier de surface DirectDraw. Stocke les textures, les textures de volume et les mappages d’environnement cubique, avec ou sans niveaux de mipmap, avec ou sans compression de pixels. Voir [DDS](../direct3ddds/dx-graphics-dds.md).                                                                                                                                       |
| .dib           | Windows Bitmap. Contient un tableau de bits associés à des structures qui spécifient la largeur et la hauteur de l’image bitmap, le format de couleur de l’appareil sur lequel l’image a été créée et la résolution de l’appareil utilisé pour créer cette image.                                                                                                              |
| . HDR           | Format HDR. Encode chaque pixel sous la forme d’une couleur RGBE 32 bits, avec 8 bits de mantisse pour le rouge, le vert et le bleu, et un exposant 8 bits partagé. Chaque canal est compressé séparément avec l’encodage de longueur d’exécution (RLE).                                                                                                                                       |
| .jpg           | Norme JPEG. Spécifie la compression des variables des fichiers de document image TIFF (Tagged Image File Format) de 24 bits et de 8 bits.                                                                                                                                                                                                       |
| . PFM           | Format de carte à virgule flottante portable. Format d’image à virgule flottante brut, sans compression. L’en-tête de fichier spécifie la largeur de l’image, la hauteur, le monochrome ou la couleur et l’ordre des mots de l’ordinateur. Les données de pixels sont stockées en tant que valeurs à virgule flottante 32 bits, avec 3 valeurs par pixel pour la couleur et une valeur par pixel pour monochrome.                                |
| .png           | Format PNG. Format bitmap non propriétaire utilisant la compression sans perte.                                                                                                                                                                                                                                                                            |
| . ppm           | Format pixmap portable. Format de fichier binaire ou ASCII pour les images de couleur qui incluent la hauteur et la largeur de l’image et la valeur maximale du composant de couleur.                                                                                                                                                                                                 |
| .tga           | Format de carte graphique Targa ou Truevision. Prend en charge des profondeurs de 8, 15, 16, 24 et 32 bits, y compris l’échelle grise de 8 bits, et contient des données de palette de couleurs facultatives, des données d’origine et de taille d’image (x, y) et des données de pixels.                                                                                                                               |



 

Pour plus d’informations sur certains de ces formats, consultez [types de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
