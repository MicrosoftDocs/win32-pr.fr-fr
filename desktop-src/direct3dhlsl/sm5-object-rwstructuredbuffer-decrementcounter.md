---
title: RWStructuredBuffer ::D fonction ecrementCounter (HTTPServ. h)
description: Décrémente le compteur masqué de l’objet.
ms.assetid: 24bc0b63-a482-4fa5-9898-2d43bca20cf4
keywords:
- DecrementCounter fonction HLSL
topic_type:
- apiref
api_name:
- DecrementCounter
api_location:
- httpserv.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8302f31cd07b81f4f78abe6a0a1fbcb2e6a1028f6153da69e55e0fb34977b585
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671389"
---
# <a name="decrementcounter-function"></a>DecrementCounter fonction)

Décrémente le compteur masqué de l’objet.

## <a name="syntax"></a>Syntaxe

``` syntax
uint DecrementCounter(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Type : **uint**

Valeur de compteur après décrémentation.

## <a name="remarks"></a>Remarques

La vue d’accès non ordonnée liée doit avoir un compteur de l' [**\_ \_ \_ \_ indicateur UAV de tampon d3d11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag) défini au cours de creationfor cette méthode pour fonctionner.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>HTTPServ. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[RWStructuredBuffer](sm5-object-rwstructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

