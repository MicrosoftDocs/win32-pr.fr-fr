---
title: 'ConsumeStructuredBuffer :: consume, fonction'
description: Supprime une valeur à partir de la fin de la mémoire tampon.
ms.assetid: b4f7b472-9274-463d-99b0-f05b74f54fc1
keywords:
- Utiliser la fonction HLSL
topic_type:
- apiref
api_name:
- Consume
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d5a43c53089a7e7b19d0f1ecef5c0e5608e8ee9
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104030483"
---
# <a name="consume-function"></a>Consume (fonction)

Supprime une valeur à partir de la fin de la mémoire tampon.

## <a name="syntax"></a>Syntaxe

``` syntax
T Consume(void);
```

## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Type : **T**

La valeur supprimée (peut être une structure).

## <a name="remarks"></a>Notes

T peut être n’importe quel type de données, y compris une structure.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




