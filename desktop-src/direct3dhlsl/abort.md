---
title: Abort, fonction (Corecrt \_ Terminate. h)
description: Envoie un message d’erreur à la file d’attente d’informations et met fin à l’appel de dessin ou de distribution en cours d’exécution.
ms.assetid: b8ce153b-0d1c-4294-b88e-b7e50e708ab9
keywords:
- fonction d’abandon HLSL
topic_type:
- apiref
api_name:
- abort
api_location:
- corecrt_terminate.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9428a03b422aed9ff6fae097459a53369d3a30e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232649"
---
# <a name="abort-function"></a>abort (fonction)

Envoie un message d’erreur à la file d’attente d’informations et met fin à l’appel de dessin ou de distribution en cours d’exécution.

## <a name="syntax"></a>Syntaxe

``` syntax
void abort(
    
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

 
</dt> <dd>

None

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette opération ne fait rien sur les rastériseurs qui ne la prennent pas en charge.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Prise en charge |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) ou version ultérieure.](dx-graphics-hlsl-sm3.md) | Oui       |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Corecrt \_ Terminate. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





