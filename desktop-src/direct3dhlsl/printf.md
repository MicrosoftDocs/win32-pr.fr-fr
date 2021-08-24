---
title: printf, fonction
description: Envoie un message de nuanceur personnalisé à la file d’attente d’informations.
ms.assetid: 0c6c15fc-1da5-4a26-ade0-5a0489e4f564
keywords:
- fonction printf HLSL
topic_type:
- apiref
api_name:
- printf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 47131cacef436572f519b394a02b4aaa357a426dd80a192868712cb3d7779e24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672519"
---
# <a name="printf-function"></a>printf, fonction

Envoie un message de nuanceur personnalisé à la file d’attente d’informations.

## <a name="syntax"></a>Syntaxe

``` syntax
void printf(
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

 

 




