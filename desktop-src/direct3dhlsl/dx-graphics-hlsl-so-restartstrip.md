---
title: RestartStrip (objet Stream-Output DirectX HLSL)
description: Met fin à la bande primitive en cours et démarre une nouvelle bande. Si la bande actuelle n’a pas assez de vertex émis pour remplir la topologie primitive, la primitive incomplète à la fin sera ignorée.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13b150de4394ecc7a8b52e050a673354326f4bd1533cf80a737807ffd6bcf43e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068159"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (objet Stream-Output DirectX HLSL)

Met fin à la bande primitive en cours et démarre une nouvelle bande. Si la bande actuelle n’a pas assez de vertex émis pour remplir la topologie primitive, la primitive incomplète à la fin sera ignorée.

RestartStrip();



 

## <a name="parameters"></a>Paramètres



| Élément                                                                                     | Description |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**None**<br/> |             |



 

## <a name="return-value"></a>Valeur de retour

None

## <a name="remarks"></a>Remarques

Une bande coupée provoque la fin de la bande actuelle et une nouvelle bande. Une bande peut être effectuée en appelant explicitement cette méthode, ou simplement en affichant jusqu’à la valeur d’index maximale (1, qui est 0xFFFFFFFF pour les index 32 bits ou 0xFFFF pour les index 16 bits). Chaque instance d’un dessin indexé avec une instance indexée génère automatiquement une bande. Cela est vrai même si la topologie n’est pas une bande triangulaire.

> [!Note]  
> La prise en charge du redémarrage et de la « valeur magique » pour une coupe est uniquement disponible sur les appareils de [niveau de fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 ou ultérieur.

 

La sortie est toujours supposée être une bande triangulaire. Pour transformer la sortie en une liste de triangles, vous devez appeler RestartStrip entre chaque triangle. Les ventilateurs triangulaires ne sont pas pris en charge.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Pris en charge |
|-----------------------------------------------------------|-----------|
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Stream-sortie (objet)](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

