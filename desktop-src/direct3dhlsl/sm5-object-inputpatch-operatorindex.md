---
title: 'InputPatch :: Operator, fonction'
description: 'Retourne le nième point de contrôle dans le correctif. | InputPatch :: Operator, fonction'
ms.assetid: 2c1eda6b-a9c1-40d3-be91-7a2e8f1da9fc
keywords:
- Fonction d’opérateur HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d95cb8adae6e7a91629614e0ae10b4161dbac3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211466"
---
# <a name="inputpatchoperator--function"></a>InputPatch :: Operator, fonction

Retourne le *n*<sup>ième</sup> point de contrôle dans le correctif.

## <a name="syntax"></a>Syntaxe

``` syntax
T Operator[](
  in uint n
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*n* \[ dans\]
</dt> <dd>

Type : **uint**

Index d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **T**

*N*<sup>ième</sup> point de contrôle.

## <a name="remarks"></a>Notes

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[InputPatch](sm5-object-inputpatch.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




