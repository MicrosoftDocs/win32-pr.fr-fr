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
ms.openlocfilehash: 4a708d2893a19369d2db42f4551e3fafa4a1ff7a4680bf8676de32f79764289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795523"
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

## <a name="remarks"></a>Remarques

Cette opération ne fait rien sur les rastériseurs qui ne la prennent pas en charge.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Pris en charge |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) ou version ultérieure.](dx-graphics-hlsl-sm3.md) | oui       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Corecrt \_ Terminate. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





