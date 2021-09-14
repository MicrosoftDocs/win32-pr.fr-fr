---
title: Constantes D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Ces constantes indiquent comment le compilateur compile un fichier Effect ou comment le runtime traite le fichier Effect.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232571"
---
# <a name="d3dcompile_effect-constants"></a>\_Constantes d’effet D3DCOMPILE

Ces constantes indiquent comment le compilateur compile un fichier Effect ou comment le runtime traite le fichier Effect.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**Effet \_ \_ enfant D3DCOMPILE \_**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Compilez le fichier Effects (. FX) en un effet enfant. Les effets enfants n’ont aucun initialiseur pour les valeurs partagées, car ces effets enfants sont initialisés dans l’effet principal (le pool d’effets).

> [!Note]  
> Les pools d’effets sont pris en charge par les effets 10 (FX10), mais pas par les effets 11 (FX11). Pour plus d’informations sur les différences entre les pools d’effets dans Direct3D 10 et les groupes d’effets dans Direct3D 11, consultez [pools et groupes](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences)d’effets.

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**L' \_ effet D3DCOMPILE \_ autorise les \_ opérations lentes \_**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Désactive le mode de performance et autorise les objets d’État mutable.

Par défaut, le mode de performance est activé. Le mode de performance interdit les objets d’État mutable en empêchant les expressions non littérales d’apparaître dans les définitions d’objets d’État.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

