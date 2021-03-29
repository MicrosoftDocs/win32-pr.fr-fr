---
title: 'OutputPatch :: Operator, fonction'
description: 'Retourne le nième point de contrôle dans le correctif. | OutputPatch :: Operator, fonction'
ms.assetid: 3ac15fe8-8bab-46a2-8826-61ade927c99e
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
ms.openlocfilehash: 8194713dc4967151991fab95000fa70c40122f26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322061"
---
# <a name="outputpatchoperator--function"></a>OutputPatch :: Operator, fonction

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
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[OutputPatch](sm5-object-outputpatch.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




