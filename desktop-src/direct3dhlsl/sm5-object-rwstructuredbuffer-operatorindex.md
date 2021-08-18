---
title: 'RWStructuredBuffer :: Operator, fonction'
description: 'Retourne une variable de ressource. | RWStructuredBuffer :: Operator, fonction'
ms.assetid: e821b60e-38db-463f-b0c6-47f2a4c9ccee
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
ms.openlocfilehash: ad2e8085a52a920f7fe87a2820398877167a137c14c4ebe39bacd71ae2ba0324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118509318"
---
# <a name="rwstructuredbufferoperator--function"></a>RWStructuredBuffer :: Operator, fonction

Retourne une variable de ressource.

## <a name="syntax"></a>Syntaxe

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*pos* \[ dans\]
</dt> <dd>

Type : **uint**

Position d’index.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **R**

Variable de ressource.

## <a name="remarks"></a>Remarques

Une ressource structurée peut être indexée en fonction des noms de composants des structures.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




