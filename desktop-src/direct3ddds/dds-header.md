---
title: Structure de DDS_HEADER (DDS. h)
description: Décrit un en-tête de fichier DDS.
ms.assetid: 7f8bde30-0ff9-4bb9-b444-5c875e6a0865
keywords:
- DDS_HEADER de la structure DDS
topic_type:
- apiref
api_name:
- DDS_HEADER
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d70fa0c4b05b6655ce0329cc73651ea21d4d808
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532426"
---
# <a name="dds_header-structure"></a>\_Structure d’en-tête DDS

Décrit un en-tête de fichier DDS.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DWORD           dwSize;
  DWORD           dwFlags;
  DWORD           dwHeight;
  DWORD           dwWidth;
  DWORD           dwPitchOrLinearSize;
  DWORD           dwDepth;
  DWORD           dwMipMapCount;
  DWORD           dwReserved1[11];
  DDS_PIXELFORMAT ddspf;
  DWORD           dwCaps;
  DWORD           dwCaps2;
  DWORD           dwCaps3;
  DWORD           dwCaps4;
  DWORD           dwReserved2;
} DDS_HEADER;
```



## <a name="members"></a>Membres

<dl> <dt>

**dwSize nul**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Taille de la structure. Ce membre doit avoir la valeur 124.

</dd> <dt>

**dwFlags**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indicateurs indiquant les membres qui contiennent des données valides.



| Indicateur              | Description                                                  | Valeur    |
|-------------------|--------------------------------------------------------------|----------|
| DDSD \_ Cap        | Obligatoire dans chaque fichier. DDS.                                 | 0x1      |
| hauteur de DDSD \_      | Obligatoire dans chaque fichier. DDS.                                 | 0x2      |
| largeur de DDSD \_       | Obligatoire dans chaque fichier. DDS.                                 | 0x4      |
| DDSD \_       | Obligatoire lorsque le pas à pas est fourni pour une texture non compressée. | 0x8      |
| DDSD \_ PIXELFORMAT | Obligatoire dans chaque fichier. DDS.                                 | 0x1000   |
| DDSD \_ MIPMAPCOUNT | Obligatoire dans une texture mipmapped.                             | 0x20000  |
| DDSD \_ LINEARSIZE  | Obligatoire lorsque le pas à pas est fourni pour une texture compressée.    | 0x80000  |
| DDSD \_ profondeur)       | Obligatoire dans une texture de profondeur.                                 | 0x800000 |



 

> [!Note]  
> Lorsque vous écrivez des fichiers. DDS, vous devez définir les \_ indicateurs DDSD Cap et DDSD \_ PIXELFORMAT, et pour les textures mipmapped, vous devez également définir l' \_ indicateur DDSD MIPMAPCOUNT. Toutefois, lorsque vous lisez un fichier. DDS, vous ne devez pas vous appuyer sur les \_ indicateurs DDSD Cap, DDSD \_ PIXELFORMAT et DDSD \_ MIPMAPCOUNT définis, car certains enregistreurs d’un tel fichier peuvent ne pas définir ces indicateurs.

 

L' \_ indicateur de \_ texture d’indicateurs d’en-tête DDS \_ , qui est défini dans DDS. h, est une combinaison au niveau du bit or de la DDSD \_ Cap, de DDSD \_ Height, de DDSD \_ Width et DDSD \_ PIXELFORMAT Flags.

L' \_ indicateur MIPMAP des indicateurs d’en-tête DDS \_ \_ , qui est défini dans DDS. h, est égal à l' \_ indicateur DDSD MIPMAPCOUNT.

L' \_ \_ indicateur de volume Flags de l’en-tête DDS \_ , qui est défini dans DDS. h, est égal à l' \_ indicateur de profondeur DDSD.

L' \_ \_ indicateur de tangage des indicateurs d’en-tête DDS \_ , qui est défini dans DDS. h, est égal à l’indicateur de pas DDSD \_ .

L' \_ indicateur LINEARSIZE de l’en-tête DDS \_ \_ , défini dans DDS. h, est égal à l' \_ indicateur DDSD LINEARSIZE.

</dd> <dt>

**dwHeight**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Hauteur de la surface (en pixels).

</dd> <dt>

**dwWidth**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Largeur de la surface (en pixels).

</dd> <dt>

**dwPitchOrLinearSize**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

La hauteur ou le nombre d’octets par ligne d’analyse dans une texture non compressée ; nombre total d’octets dans la texture de niveau supérieur pour une texture compressée. Pour plus d’informations sur la façon de calculer le pas, consultez la section relative au format de fichier DDS [dans le Guide de programmation pour DDS](dx-graphics-dds-pguide.md).

</dd> <dt>

**dwDepth**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profondeur d’une texture de volume (en pixels), sinon inutilisée.

</dd> <dt>

**dwMipMapCount**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de niveaux de mipmap, sinon non utilisé.

</dd> <dt>

**dwReserved1 \[ 11\]**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Inutilisé.

</dd> <dt>

**ddspf**
</dt> <dd>

Type : **[ **DDS \_ PIXELFORMAT**](dds-pixelformat.md)**

</dd> <dd>

Le format de pixel (voir [**DDS \_ PIXELFORMAT**](dds-pixelformat.md)).

</dd> <dt>

**dwCaps**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Spécifie la complexité des surfaces stockées.



| Indicateur             | Description                                                                                                                              | Valeur    |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|----------|
| DDSCAPS \_ complexe | Facultatif doit être utilisé sur tout fichier qui contient plusieurs surfaces (un mipmap, une carte d’environnement cubique ou une texture de volume mipmapped). | 0x8      |
| \_MIPMAP DDSCAPS  | Facultatif doit être utilisé pour un mipmap.                                                                                                   | 0x400000 |
| \_texture DDSCAPS | Obligatoire                                                                                                                                 | 0x1000   |



 

> [!Note]  
> Lorsque vous écrivez des fichiers. DDS, vous devez définir l' \_ indicateur de texture DDSCAPS et, pour plusieurs surfaces, vous devez également définir l' \_ indicateur complexe DDSCAPS. Toutefois, lorsque vous lisez un fichier. DDS, vous ne devez pas vous appuyer sur la \_ texture DDSCAPS et les \_ indicateurs complexes DDSCAPS sont définis, car certains enregistreurs d’un tel fichier peuvent ne pas définir ces indicateurs.

 

L' \_ \_ \_ indicateur mipmap des indicateurs de surface DDS, qui est défini dans DDS. h, est une combinaison de bits or des \_ indicateurs mipmap DDSCAPS et DDSCAPS \_ .

L' \_ \_ \_ indicateur de texture indicateurs de surface DDS, qui est défini dans DDS. h, est égal à l' \_ indicateur de texture DDSCAPS.

L' \_ indicateur carte cubique des indicateurs de surface DDS \_ \_ , défini dans DDS. h, est égal à l' \_ indicateur complexe DDSCAPS.

</dd> <dt>

**dwCaps2**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Détails supplémentaires sur les surfaces stockées.



| Indicateur                         | Description                                            | Valeur    |
|------------------------------|--------------------------------------------------------|----------|
| DDSCAPS2 \_ carte cubique            | Requis pour un mappage de cube.                               | 0x200    |
| DDSCAPS2 \_ carte cubique \_ POSITIVEX | Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube. | 0x400    |
| DDSCAPS2 \_ carte cubique \_ NEGATIVEX | Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube. | 0x800    |
| DDSCAPS2 \_ carte cubique \_ positif | Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube. | 0x1000   |
| DDSCAPS2 \_ carte cubique \_ négatif | Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube. | 0x2000   |
| DDSCAPS2 \_ carte cubique \_ POSITIVEZ | Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube. | 0x4000   |
| DDSCAPS2 \_ carte cubique \_ NEGATIVEZ | Obligatoire lorsque ces surfaces sont stockées dans un mappage de cube. | 0x8000   |
| \_Volume DDSCAPS2             | Requis pour une texture de volume.                         | 0x200000 |



 

L' \_ indicateur DDS carte cubique \_ POSITIVEX, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique POSITIVEX.

L' \_ indicateur DDS carte cubique \_ NEGATIVEX, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique NEGATIVEX.

L' \_ \_ indicateur de positif DDS carte cubique, qui est défini dans DDS. h, est une combinaison au niveau du bit or des \_ indicateurs positifs DDSCAPS2 carte cubique et DDSCAPS2 \_ carte cubique \_ .

L' \_ \_ indicateur de négatif DDS carte cubique, qui est défini dans DDS. h, est une combinaison au niveau du bit ou de la DDSCAPS2 \_ carte cubique et DDSCAPS2 \_ carte cubique les \_ indicateurs négatifs.

L' \_ indicateur DDS carte cubique \_ POSITIVEZ, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique POSITIVEZ.

L' \_ indicateur DDS carte cubique \_ NEGATIVEZ, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ indicateurs DDSCAPS2 carte cubique \_ et \_ DDSCAPS2 carte cubique NEGATIVEZ.

L' \_ indicateur DDS carte cubique \_ ALLFACES, qui est défini dans DDS. h, est une combinaison or au niveau du bit des \_ carte cubique DDS \_ POSITIVEX, DDS \_ carte cubique \_ NEGATIVEX, DDS \_ carte cubique \_ positive, DDS \_ carte cubique \_ Negative, DDS \_ carte cubique \_ POSITIVEZ et DDSCAPS2 \_ \_ carte cubique NEGATIVEZ.

L' \_ \_ indicateur de volume des indicateurs DDS, défini dans DDS. h, est égal à l' \_ indicateur de volume DDSCAPS2.

> [!Note]  
> Bien que Direct3D 9 prenne en charge les mappages de cubes partiels, Direct3D 10, 10,1 et 11 nécessitent que vous définissiez les six visages de mappage de cube (autrement dit, vous devez définir DDS \_ carte cubique \_ ALLFACES).

 

</dd> <dt>

**dwCaps3**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Inutilisé.

</dd> <dt>

**dwCaps4**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Inutilisé.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Inutilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Incluez les indicateurs dans **dwFlags** pour les membres de la structure qui contiennent des données valides.

Utilisez cette structure en association avec un [**\_ en-tête DDS \_ DXT10**](dds-header-dxt10.md) pour stocker un tableau de ressources dans un fichier DDS. Pour plus d’informations, consultez [tableaux de texture](dx-graphics-dds-pguide.md).

**DDS \_ L’en-tête** est identique à la structure DDSURFACEDESC2 de DirectDraw sans les dépendances DirectDraw.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence pour DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

