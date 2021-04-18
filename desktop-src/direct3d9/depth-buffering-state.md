---
description: La mise en mémoire tampon de profondeur est une méthode de suppression des lignes et des surfaces masquées. Par défaut, Direct3D n’utilise pas la mise en mémoire tampon de profondeur.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: État de la mise en mémoire tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481553"
---
# <a name="depth-buffering-state-direct3d-9"></a>État de la mise en mémoire tampon de profondeur (Direct3D 9)

La mise en mémoire tampon de profondeur est une méthode de suppression des lignes et des surfaces masquées. Par défaut, Direct3D n’utilise pas la mise en mémoire tampon de profondeur.

Pour obtenir une vue d’ensemble conceptuelle des mémoires tampons de profondeur, consultez [mémoires tampons de profondeur (Direct3D 9)](depth-buffers.md).

Les applications C++ mettent à jour l’état de mise en mémoire tampon de profondeur avec l' \_ État de rendu D3DRS ZENABLE, à l’aide d’un membre de l’énumération [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) pour spécifier la nouvelle valeur d’État.

Si votre application doit empêcher Direct3D d’écrire dans le tampon de profondeur, elle peut utiliser la \_ valeur énumérée D3DRS ZWRITEENABLE, en spécifiant D3DZB \_ false comme deuxième paramètre pour l’appel à [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

L’exemple de code suivant montre comment l’état de la mémoire tampon de profondeur est défini pour activer la mise en mémoire tampon z.


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



Votre application peut également utiliser l' \_ État de rendu D3DRS ZFUNC pour contrôler la fonction de comparaison utilisée par Direct3D lors de l’exécution de la mise en mémoire tampon de profondeur.

L’inclinaison Z est une méthode qui consiste à afficher une surface devant l’autre, même si leurs valeurs de profondeur sont identiques. Vous pouvez utiliser cette technique pour un grand nombre d’effets. Un exemple courant est le rendu des ombres sur les murs. L’ombre et le mur ont la même valeur de profondeur. Toutefois, vous souhaitez que votre application affiche l’ombre sur le mur. En donnant une polarisation z à l’ombre, Direct3D les affiche correctement (consultez D3DRS \_ DEPTHBIAS).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
