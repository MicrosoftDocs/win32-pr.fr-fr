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
ms.openlocfilehash: a76f8c27ed50c7d7eab1b37cd5c60257691b8db5e5af412f5b3bfe678c283bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486699"
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

## <a name="remarks"></a>Remarques

T peut être n’importe quel type de données, y compris une structure.

Cette fonction est prise en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ConsumeStructuredBuffer](sm5-object-consumestructuredbuffer.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




