---
title: fonction DST
description: Calcule un vecteur de distance. | fonction DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- fonction DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b0d8112902486102e6a4338445a2526b23cab8dafb2ea8b7d68b87d5b803af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068339"
---
# <a name="dst-function"></a>fonction DST

Calcule un vecteur de distance.

## <a name="syntax"></a>Syntaxe

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*src0* \[ dans\]
</dt> <dd>

Type : **[fVector](dx-graphics-hlsl-vector.md)**

Premier vecteur.

</dd> <dt>

*src1* \[ dans\]
</dt> <dd>

Type : **[fVector](dx-graphics-hlsl-vector.md)**

Deuxième vecteur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[fVector](dx-graphics-hlsl-vector.md)**

Vecteur de distance calculé.

## <a name="remarks"></a>Remarques

Cette fonction intrinsèque fournit les mêmes fonctionnalités que l' [heure d’été](dst---vs.md)de l’instruction du nuanceur de sommets.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions intrinsèques](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




