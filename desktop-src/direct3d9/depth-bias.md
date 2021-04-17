---
description: Les polygones qui sont coplanés dans votre espace 3D peuvent apparaître comme s’ils n’étaient pas coplanés en ajoutant un biais z à chacun d’eux.
ms.assetid: 0ab4f63b-49de-4bd0-a10f-6f90b9706c58
title: Décalage de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce605ea1df161e5ebfed95c214c3dd180ab7ee6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481561"
---
# <a name="depth-bias-direct3d-9"></a>Décalage de profondeur (Direct3D 9)

Les polygones qui sont coplanés dans votre espace 3D peuvent apparaître comme s’ils n’étaient pas coplanés en ajoutant un biais z à chacun d’eux. Il s’agit d’une technique couramment utilisée pour s’assurer que les ombres d’une scène s’affichent correctement. Par exemple, une ombre sur un mur aura probablement la même valeur de profondeur que le mur. Si vous affichez le mur en premier, puis l’ombre, l’ombre peut ne pas être visible ou les artefacts de profondeur peuvent être visibles. Vous pouvez inverser l’ordre dans lequel vous effectuez le rendu des objets coplanaires dans l’espoir d’inverser l’effet, mais les artefacts de profondeur sont toujours susceptibles de se produire.

Une application peut aider à s’assurer que les polygones sont rendus correctement en ajoutant un décalage aux valeurs z que le système utilise lors du rendu des jeux de polygones coplanaires. Pour ajouter un biais z à un ensemble de polygones, appelez la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) juste avant de les afficher, en définissant le paramètre d' *État* sur D3DRS \_ DEPTHBIAS et le paramètre *value* sur une valeur float appropriée (par exemple, une valeur appropriée peut être comprise entre-1,0 et 1,0) ; pour transmettre cette valeur à **SetRenderState** Une valeur de décalage z supérieure augmente la probabilité que les polygones que vous affichez s’affichent avec d’autres polygones coplanaires.


```
Offset = m * D3DRS_SLOPESCALEDEPTHBIAS + D3DRS_DEPTHBIAS
```



où m est la pente de profondeur maximale du triangle rendu.


```
m = max(abs(delta z / delta x), abs(delta z / delta y)) 
```



Les unités pour les \_ États de rendu D3DRS DEPTHBIAS et D3DRS \_ SLOPESCALEDEPTHBIAS varient selon que la mise en mémoire tampon z ou w est activée. L’application doit fournir des valeurs appropriées.

Le biais n’est appliqué à aucune ligne et primitives de point. Toutefois, cette valeur doit être appliquée aux triangles dessinés en mode filaire.


```
// RenderStates
D3DRS_SLOPESCALEDEPTHBIAS, // Defaults to zero
D3DRS_DEPTHBIAS,           // Defaults to zero
```




```
// Caps
D3DPRASTERCAPS_DEPTHBIAS           
D3DPRASTERCAPS_SLOPESCALEDEPTHBIAS 
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline de pixels](pixel-pipeline.md)
</dt> </dl>

 

 
