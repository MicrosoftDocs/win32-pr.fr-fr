---
title: Structure de DDS_HEADER_DXT10 (DDS. h)
description: Extension d’en-tête DDS pour gérer des tableaux de ressources, des formats de pixel DXGI qui ne sont pas mappés aux structures de format de pixel Microsoft DirectDraw héritées et des métadonnées supplémentaires.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 de la structure DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a2f5dd4a6948d38b86b49584db81937ce5148b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535167"
---
# <a name="dds_header_dxt10-structure"></a>\_Structure DXT10 d’en-tête DDS \_

Extension d’en-tête DDS pour gérer des tableaux de ressources, des formats de pixel DXGI qui ne sont pas mappés aux structures de format de pixel Microsoft DirectDraw héritées et des métadonnées supplémentaires.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a>Membres

<dl> <dt>

**dxgiFormat**
</dt> <dd>

Type : **[ **dxgi \_ format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Format de pixel de la surface (voir [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourceDimension**
</dt> <dd>

Type : **[ **\_ \_ dimension de ressource D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifie le type de ressource. Les valeurs suivantes pour ce membre sont un sous-ensemble des valeurs de [**la \_ \_ dimension de ressource D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) ou de l’énumération de [**\_ \_ dimension de ressource d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :



| Type                                                              | Description                                                                                                                                                                                                                                                                                                                                                            | Valeur |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_TEXTURE1D dimension DDS \_ (D3D10 de \_ dimension de ressource \_ \_ TEXTURE1D) | La ressource est une [texture 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types). Le membre **dwWidth** de [**l' \_ en-tête DDS**](dds-header.md) spécifie la taille de la texture. En règle générale, vous définissez le membre **dwHeight** de l' **\_ en-tête DDS** sur 1 ; vous devez également définir l' \_ indicateur DDSD Height dans le membre **dwFlags** de l' **\_ en-tête DDS**.                      | 2     |
| \_TEXTURE2D dimension DDS \_ (D3D10 de \_ dimension de ressource \_ \_ TEXTURE2D) | La ressource est une [texture 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) avec une zone spécifiée par les membres **dwWidth** et **dwHeight** de l' [**\_ en-tête DDS**](dds-header.md). Vous pouvez également utiliser ce type pour identifier une texture de mappage de cube. Pour plus d’informations sur l’identification d’une texture de mappage de cube, consultez membres **miscFlag** et **arraySize** . | 3     |
| \_TEXTURE3D dimension DDS \_ (D3D10 de \_ dimension de ressource \_ \_ TEXTURE3D) | La ressource est une [texture 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) avec un volume spécifié par les membres **dwWidth**, **dwHeight** et **dwDepth** de [**l' \_ en-tête DDS**](dds-header.md). Vous devez également définir l' \_ indicateur de profondeur DDSD dans le membre **dwFlags** de l' **\_ en-tête DDS**.                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifie d’autres options moins courantes pour les ressources. La valeur suivante pour ce membre est un sous-ensemble des valeurs de [**l' \_ \_ \_ indicateur div de la ressource D3D10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) ou de l’énumération des [**\_ \_ \_ indicateurs divers des ressources d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :



| Type                             | Description                                                                                                  | Valeur |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| \_ \_ TEXTURECUBE divers des ressources DDS \_ | Indique qu’une [texture 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) est une texture de mappage de cube. | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre d’éléments dans le tableau.

Pour une [texture 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) qui est également une texture de mappage de cube, ce nombre représente le nombre de cubes. Ce nombre est le même que le nombre dans le membre **NumCubes** de [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) ou [**d3d11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)). Dans ce cas, le fichier DDS contient des \* textures 2D arraySize 6. Pour plus d’informations sur ce cas, consultez la description de **miscFlag** .

Pour une [texture 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), vous devez définir ce nombre sur 1.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Contient des métadonnées supplémentaires (anciennement réservées). Les 3 bits de poids faible indiquent le mode Alpha de la ressource associée. Les 29 premiers bits sont réservés et sont généralement 0.



| Type                            | Description                                                                                                                              | Valeur |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_mode Alpha \_ DDS \_ inconnu       | Le contenu du canal alpha est inconnu. Il s’agit de la valeur des fichiers hérités, qui est généralement supposée être alpha « rectiligne ».                 | 0x0   |
| \_mode Alpha \_ DDS \_ simple      | Tout contenu de canal alpha est supposé utiliser une valeur alpha directe.                                                                             | 0x1   |
| \_mode Alpha \_ DDS \_ prémultiplié | Tout contenu de canal alpha utilise l’alpha prémultiplié. Les seuls formats de fichier hérités qui indiquent ces informations sont « DX2 » et « DX4 ». | 0x2   |
| \_ \_ opaque en mode Alpha \_ opaque        | Tout contenu de canal alpha est défini sur entièrement opaque.                                                                                    | 0x3   |
| \_ \_ personnalisé en mode Alpha DDS \_        | Tout contenu de canal alpha est utilisé en tant que quatrième canal et n’est pas destiné à représenter la transparence (directe ou prémultipliée).      | 0x4   |



 

> [!Note]  
> Les bibliothèques d’utilitaires D3DX 10 et [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) héritées ne peuvent pas être chargées. Fichier DDS avec **miscFlags2** non égal à zéro.

 

</dd> </dl>

## <a name="remarks"></a>Notes

Utilisez cette structure avec un [**\_ en-tête DDS**](dds-header.md) pour stocker un tableau de ressources dans un fichier DDS. Pour plus d’informations, consultez [tableaux de texture](dx-graphics-dds-pguide.md).

Cet en-tête est présent si le membre **dwFourCC** de la structure [**DDS \_ PIXELFORMAT**](dds-pixelformat.md) a la valeur « facilement ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence pour DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

