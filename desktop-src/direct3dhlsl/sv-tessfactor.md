---
title: SV_TessFactor
description: Définit la quantité de pavage sur chaque bord d’un correctif.
ms.assetid: 970ff744-da5b-4933-866c-dd38b85fb48d
keywords:
- SV_TessFactor HLSL
topic_type:
- apiref
api_name:
- SV_TessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2243827fa1b955079aaf64b9805cf02ac82934bde814ed780570a5ba9b63ade8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285495"
---
# <a name="sv_tessfactor"></a>SV \_ TessFactor

Définit la quantité de pavage sur chaque bord d’un correctif.

## <a name="type"></a>Type



|  Type          |  Topologie d’entrée              |
|------------|----------------|
| float \[ 4\] | correctif Quad     |
| float \[ 3\] | correctif triple      |
| float \[ 2\] | isoligne        |



 

Les facteurs de pavage doivent être déclarés en tant que tableau ; ils ne peuvent pas être empaquetés dans un seul vecteur.

## <a name="remarks"></a>Notes

La valeur du facteur de pavage doit être définie au cours de la fonction de constante de patch du nuanceur de coque.

Valeur de sortie requise pour le nuanceur de coque si vous utilisez des correctifs quad ou tri. Cette valeur est également une valeur d’entrée obligatoire pour que le nuanceur de domaine corresponde aux signatures de données à constante de correctif entre les étapes de pavage.

Pour une isoligne, la première valeur de SV \_ TessFactor est le facteur de pavage de densité de ligne, la deuxième valeur est le facteur de pavage de détail de ligne.

### <a name="tri-patch-tessellation-factors"></a>Facteurs de pavage de correctif tri

Le premier composant fournit le facteur géométrique pour le bord u = = 0 du correctif. Le deuxième composant fournit le facteur géométrique pour le bord v = = 0 du correctif. Le troisième composant fournit le facteur géométrique pour le bord w = = 0 du correctif.

### <a name="quad-patch-tessellation-factors"></a>Facteurs de pavage Quad patch

Le premier composant fournit le facteur géométrique pour le bord u = = 0 du correctif. Le deuxième composant fournit le facteur géométrique pour le bord v = = 0 du correctif. Le troisième composant fournit le facteur géométrique pour le bord u = = 1 du correctif. Le quatrième composant fournit le facteur géométrique pour le bord v = = 1 du correctif. L’ordre des bords est dans le sens inverse des aiguilles d’une montre, à partir du bord u = = 0, qui est le côté gauche du correctif, et à partir du bord v = = 0, qui est le haut du correctif.

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sémantique](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




