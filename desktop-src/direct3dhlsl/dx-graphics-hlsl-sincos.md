---
title: SinCos,
description: Retourne le sinus et le cosinus de x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- HLSL SinCos,
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff2854ea4c8b956298a65107136a963c5591b91de32d108b3179772bd0043a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673479"
---
# <a name="sincos"></a>SinCos,

Retourne le sinus et le cosinus de x.



| SinCos, (*x*, sortie *s*, sortie *c*) |
|-------------------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                   | Description                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[dans \] la valeur spécifiée, en radians.<br/> |
| <span id="s"></span><span id="S"></span>*x*<br/> | \[out \] retourne le sinus de x.<br/>          |
| <span id="c"></span><span id="C"></span>*secteur*<br/> | \[out \] retourne le cosinus de x.<br/>        |



 

## <a name="return-value"></a>Valeur renvoyée

Aucun.

## <a name="type-description"></a>Description du type



| Name | [**Type de modèle**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Type de composant**](dx-graphics-hlsl-intrinsic-functions.md) | Taille                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*  | [**scalaire**](dx-graphics-hlsl-intrinsic-functions.md), **vecteur** ou **matrice** | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | n'importe laquelle                            |
| *s*  | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |
| c    | identique à l’entrée *x*                                                                                              | [**dissocié**](/windows/desktop/WinProg/windows-data-types)                        | la ou les mêmes dimensions comme entrée *x* |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                       | Pris en charge           |
|------------------------------------------------------------------------------------|---------------------|
| [Nuancier modèle 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) et modèles de nuanceur plus élevés | oui                 |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Oui (vs \_ 1 \_ 1 uniquement) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Fonctions intrinsèques (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

