---
title: Registre temporaire (référence HLSL VS)
description: Un registre temporaire de nuanceur de sommets est utilisé pour conserver les résultats intermédiaires.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313798"
---
# <a name="temporary-register-hlsl-vs-reference"></a>Registre temporaire (référence HLSL VS)

Un registre temporaire de nuanceur de sommets est utilisé pour conserver les résultats intermédiaires.

Un registre temporaire doit être initialisé avant d’être utilisé. Chaque registre temporaire dispose d’un accès en écriture unique et triple lecture. Cela signifie qu’une instruction de nuanceur unique peut utiliser jusqu’à trois registres temporaires comme entrées.

Les valeurs d’un registre temporaire qui restent des appels précédents du nuanceur vertex ne peuvent pas être utilisées.

Un registre se compose de propriétés qui déterminent le comportement de chaque registre.



| Propriété        | Description                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nom            | r \[ n \] . n est un numéro de Registre facultatif. La valeur par défaut est 0, et est la valeur utilisée si aucune valeur n’est spécifiée.                                                                                 |
| Count           | Un maximum de 12 registres.                                                                                                                                                                  |
| Autorisations d’e/s | En lecture/écriture. Ce registre peut être lu ou écrit par l’API ou par le nuanceur.                                                                                                               |
| Ports de lecture      | Le nombre de fois qu’un registre peut être lu dans une instruction unique est 3. Un registre temporaire est le seul registre qui peut être lu et écrit plusieurs fois dans une même instruction. |



 

Chaque registre temporaire dispose d’un accès en écriture unique et triple lecture. Par conséquent, une instruction peut avoir jusqu’à trois registres temporaires dans son ensemble d’opérandes de source d’entrée.

Aucune valeur dans un registre temporaire qui reste des appels précédents du nuanceur vertex ne peut être utilisée. Les nuanceurs de sommets qui lisent une valeur à partir d’un registre temporaire avant d’y écrire échouent à l’appel de l’API Direct3D pour créer le nuanceur de sommets.

## <a name="example"></a>Exemple

Voici un exemple d’utilisation d’un registre temporaire :


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre temporaire     | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




