---
title: Clonage d’un effet
description: Le clonage d’un effet crée une deuxième copie quasiment identique de l’effet.
ms.assetid: e3870363-5ee8-4fdc-a489-cdaeef8c9c39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 195b4e9a42e595558acc4c512f8662c11b2acde7873e123b242ee272eeea7e8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118538003"
---
# <a name="cloning-an-effect"></a>Clonage d’un effet

Le clonage d’un effet crée une deuxième copie quasiment identique de l’effet. Pour une explication de la raison pour laquelle il n’est pas exact, consultez le qualificateur unique suivant. Une deuxième copie d’un effet est utile quand vous souhaitez utiliser l’infrastructure Effects sur plusieurs threads, puisque le runtime Effect n’est pas thread-safe pour maintenir des performances élevées.

Étant donné que les contextes de périphérique sont également non thread-sécurisés, différents threads doivent passer différents contextes de périphérique à la méthode ID3DX11EffectPass :: apply.

Un effet peut être cloné à l’aide de la syntaxe suivante :


```
ID3DX11Effect* pClonedEffect = NULL;
UINT Flags = D3DX11_EFFECT_CLONE_FORCE_NONSINGLE;
HRESULT hr = pEffect->CloneEffect( Flags, &pClonedEffect );
```



Dans l’exemple ci-dessus, la copie clonée encapsule le même État que l’effet d’origine, quel que soit l’état d’origine de l’effet. En particulier :

1.  Si pEffect est optimisé, l’effet pCloned est optimisé
2.  Si pEffect a des variables gérées par l’utilisateur, pCloned Effect aura les mêmes variables gérées par l’utilisateur (voir la description unique ci-dessous)
3.  Toute mise à jour de variable en attente (jusqu’à ce qu’un appel de mise à jour de l’état de l’appareil) dans pEffect sera en attente dans pClonedEffect

Les objets d’appareil Direct3D 11 suivants sont immuables ou jamais mis à jour par l’infrastructure Effects, de sorte que l’effet cloné pointe vers les mêmes objets que l’effet d’origine :

1.  Objets de bloc d’État (ID3D11BlendState, ID3D11RasterizerState, ID3D11DepthStencilState, ID3D11SamplerState)
2.  Nuanceurs
3.  Instances de classe
4.  Textures (à l’exclusion des mémoires tampons de texture)
5.  Vues d’accès non ordonnées

Les objets d’appareil Direct3D 11 suivants sont immuables et modifiés par le runtime Effect (sauf s’ils sont gérés par l’utilisateur ou uniques dans un effet cloné); de nouvelles copies de ces objets sont créées en cas de non-simple :

1.  Mémoires tampons constantes
2.  Mémoires tampons de texture

## <a name="single-constant-buffers-and-texture-buffers"></a>Mémoires tampons à constante unique et mémoires tampons de texture

Notez que cette discussion s’applique à la fois aux mémoires tampons constantes et aux textures, mais que les mémoires tampons constantes sont prises en compte pour faciliter la lecture.

Il peut arriver qu’une mémoire tampon constante soit uniquement mise à jour par un thread, mais que l’état de l’appareil défini par les effets clonés utilise ces données. Par exemple, l’effet principal peut mettre à jour les matrices universelles et de vue qui sont référencées à partir des nuanceurs dans des effets clonés qui ne modifient pas les matrices de monde et de vue. Dans ces cas, les effets clonés doivent référencer la mémoire tampon constante actuelle au lieu de recréer une.

Il existe deux façons d’obtenir ce résultat souhaité :

1.  Utilisez ID3DX11EffectConstantBuffer :: SetConstantBuffer sur l’effet cloné pour le rendre géré par l’utilisateur
2.  Marquer la mémoire tampon de constante en tant que « Single » dans le code HLSL, en forçant le runtime Effect à traiter comme étant géré par l’utilisateur après le clonage

Il existe deux différences entre les deux méthodes ci-dessus. Tout d’abord, dans la méthode 1, un nouveau ID3D11Buffer sera créé et l’utilisateur avant l’appel de SetConstantBuffer. En outre, après avoir appelé UndoSetConstantBuffer dans l’effet cloné, la variable de la méthode 1will pointe vers la mémoire tampon qui vient d’être créée (les effets sont mis à jour lors de l’application), tandis que la variable de la méthode 2 continue à pointer vers la mémoire tampon d’origine (et non à la mettre à jour sur Apply).

Consultez l’exemple suivant en HLSL :


```
cbuffer ObjectData
{
    float4 Position;
};
single cbuffer ViewData
{
    float4x4 ViewMatrix;
};
```



Lors du clonage, l’effet cloné crée un nouveau ID3D11Buffer pour ObjectData et remplit son contenu à la place de l’application, mais référence le ID3D11Buffer d’origine pour ViewData. Vous pouvez ignorer le qualificateur unique dans le processus de clonage en définissant l' \_ indicateur D3DX11 effet \_ cloner forcer le clone \_ \_ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




