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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915243"
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

## <a name="return-value"></a>Valeur de retour

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

 

 




