---
title: 'RWStructuredBuffer :: IncrementCounter, fonction (HTTPServ. h)'
description: Incrémente le compteur masqué de l’objet.
ms.assetid: 66385d4f-6db8-49ae-a73a-49089695f5ee
keywords:
- IncrementCounter fonction HLSL
topic_type:
- apiref
api_name:
- IncrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0002f82873de1c56ce5a7d79c9adb13bdf7ebc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124419"
---
# <a name="incrementcounter-function"></a>IncrementCounter fonction)

Incrémente le compteur masqué de l’objet.

## <a name="syntax"></a>Syntaxe

``` syntax
uint IncrementCounter(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Type : **uint**

Valeur de compteur pré-incrémentée.

## <a name="remarks"></a>Notes

Pour que cette méthode fonctionne, la vue d’accès non triée liée doit avoir un [**\_ \_ \_ \_ compteur d’indicateur UAV de tampon d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) défini lors de la création.

Une ressource structurée peut être indexée en fonction des noms de composants des structures.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>HTTPServ. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

