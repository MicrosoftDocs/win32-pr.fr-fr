---
title: printf (fonction)
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
ms.openlocfilehash: 74492cc613e22f335eace684300f0380e5751a95
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940502"
---
# <a name="printf-function"></a>printf (fonction)

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

## <a name="remarks"></a>Notes

Cette opération ne fait rien sur les appareils qui ne la prennent pas en charge.

### <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                        | Prise en charge |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4 (DirectX HLSL) ou version ultérieure.](dx-graphics-hlsl-sm3.md) | Oui       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




