---
description: Identifie l’utilisation prévue des données de vertex.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Énumération D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 707a5b7b886ac9366733e1b17322ac61c7d9703cb6ef8ac1e095cf1300fd508d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857509"
---
# <a name="d3ddeclusage-enumeration"></a>Énumération D3DDECLUSAGE

Identifie l’utilisation prévue des données de vertex.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Position D3DDECLUSAGE**
</dt> <dd>

Placez les données entre (-1,-1) et (1, 1). Utilisez \_ la position D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier une position non transformée pour le traitement de vertex de fonction fixe et le du paveur n-patch. Utilisez \_ la position D3DDECLUSAGE avec un index d’utilisation de 1 pour spécifier la position non transformée dans le nuanceur de sommets de fonction fixe pour l’interpolation de vertex.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**
</dt> <dd>

Fusion des données de poids. Utilisez D3DDECLUSAGE \_ BLENDWEIGHT avec un index d’utilisation de 0 pour spécifier les pondérations de fusion utilisées dans la fusion de vertex indexée et non indexée.

</dd> <dt>

<span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**
</dt> <dd>

Fusion des données d’index. Utilisez D3DDECLUSAGE \_ BLENDINDICES avec un index d’utilisation de 0 pour spécifier des index de matrice pour les pelures de palette indexées.

</dd> <dt>

<span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normal**
</dt> <dd>

Données normales au vertex. Utilisez D3DDECLUSAGE \_ normal avec un index d’utilisation égal à 0 pour spécifier les normales aux sommets pour le traitement des vertex de fonction fixe et le du paveur n-patch. Utilisez D3DDECLUSAGE \_ normal avec un index d’utilisation de 1 pour spécifier les normales aux sommets pour le traitement des vertex de fonction fixe pour l’interpolation de vertex.

</dd> <dt>

<span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ psize**
</dt> <dd>

Données de taille en points. Utilisez D3DDECLUSAGE \_ psize avec un index d’utilisation de 0 pour spécifier l’attribut de taille de point utilisé par le moteur d’installation du rastériseur pour étendre un point à un quadruple pour la fonctionnalité point-Sprite.

</dd> <dt>

<span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ texcoord**
</dt> <dd>

Données de coordonnée de texture. Utilisez D3DDECLUSAGE \_ texcoord, n pour spécifier des coordonnées de texture dans le traitement du vertex de fonction fixe et dans les nuanceurs de pixels antérieurs à PS \_ 3 \_ 0. Elles peuvent être utilisées pour transmettre des données définies par l’utilisateur.

</dd> <dt>

<span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE \_ tangente**
</dt> <dd>

Données de tangente de vertex.

</dd> <dt>

<span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BInormal**
</dt> <dd>

Données binormales de vertex.

</dd> <dt>

<span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**
</dt> <dd>

Valeur à virgule flottante positive unique. Utilisez D3DDECLUSAGE \_ TESSFACTOR avec un index d’utilisation de 0 pour spécifier un facteur de pavage utilisé dans l’unité de pavage pour contrôler le taux de pavage. Pour plus d’informations sur le type de données, consultez D3DDECLTYPE \_ FLOAT1.

</dd> <dt>

<span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**\_Position D3DDECLUSAGE**
</dt> <dd>

Les données de vertex contiennent des données de position transformées allant de (0,0) à (largeur de la fenêtre d’affichage, hauteur de la fenêtre d’affichage). Utilisez D3DDECLUSAGE \_ position avec un index d’utilisation égal à 0 pour spécifier la position transformée. Lorsqu’une déclaration contenant cette valeur est définie, le pipeline n’effectue pas de traitement de vertex.

</dd> <dt>

<span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Couleur D3DDECLUSAGE**
</dt> <dd>

Les données de vertex contiennent une couleur diffuse ou spéculaire. Utilisez la \_ couleur D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier la couleur diffuse dans le nuanceur de sommets de fonction fixe et les nuanceurs de pixels avant PS \_ 3 \_ 0. Utilisez la \_ couleur D3DDECLUSAGE avec un index d’utilisation de 1 pour spécifier la couleur spéculaire dans le nuanceur de sommets de fonction fixe et les nuanceurs de pixels antérieurs à PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**\_Brouillard D3DDECLUSAGE**
</dt> <dd>

Les données de vertex contiennent des données de brouillard. Utilisez \_ le brouillard D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier une valeur de fusion de brouillard utilisée après la fin de l’ombrage de pixel. Cela s’applique aux nuanceurs de pixels antérieurs à la version PS \_ 3 \_ 0.

</dd> <dt>

<span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE \_ profondeur)**
</dt> <dd>

Les données de vertex contiennent des données de profondeur.

</dd> <dt>

<span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**\_Exemple D3DDECLUSAGE**
</dt> <dd>

Les données de vertex contiennent des exemples de données. Utilisez \_ l’exemple D3DDECLUSAGE avec un index d’utilisation de 0 pour spécifier la valeur de déplacement à rechercher. Il peut être utilisé uniquement avec D3DDECLUSAGE \_ LOOKUPPRESAMPLED ou D3DDECLUSAGE \_ Lookup.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les données de vertex sont déclarées avec un tableau de structures [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Chaque élément du tableau contient un type d’utilisation.

Pour plus d’informations sur les déclarations de vertex, consultez la rubrique [déclaration de vertex (Direct3D 9)](vertex-declaration.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Énumérations Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[Déclaration de vertex (Direct3D 9)](vertex-declaration.md)
</dt> </dl>

 

 




