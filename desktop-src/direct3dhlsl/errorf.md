---
title: errorf fonction)
description: Envoie un message d’erreur à la file d’attente d’informations.
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- errorf fonction HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0651a27419a369721806e9aa4717a20088f8f5fbbaa0063628d2feb69648c7cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562679"
---
# <a name="errorf-function"></a>errorf fonction)

Envoie un message d’erreur à la file d’attente d’informations.

## <a name="syntax"></a>Syntaxe

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*format* 
</dt> <dd>

Chaîne de format.

</dd> <dt>

*argument...* 
</dt> <dd>

Arguments facultatifs.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette opération ne fait rien sur les appareils qui ne la prennent pas en charge.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Pris en charge |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) ou version ultérieure.](dx-graphics-hlsl-sm3.md) | oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




