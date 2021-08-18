---
description: Une application Direct3D affiche généralement une séquence animée en générant les frames de l’animation dans des mémoires tampons d’arrière-plan et en les présentant dans l’ordre.
ms.assetid: 4ca9a845-f433-4d4a-939e-4b9ab2983927
title: Retournement des surfaces (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c14aa7df63c3956d4974282033b44a7129853940d475b23115f9bca344ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988033"
---
# <a name="flipping-surfaces-direct3d-9"></a>Retournement des surfaces (Direct3D 9)

Une application Direct3D affiche généralement une séquence animée en générant les frames de l’animation dans des mémoires tampons d’arrière-plan et en les présentant dans l’ordre. Les mémoires tampons d’arrière-plan sont organisées en chaînes d’échange. Une chaîne de permutation est une série de mémoires tampons qui sont retournées à l’écran l’une après l’autre. Cela peut être utilisé pour restituer une scène en mémoire, puis retourner la scène à l’écran lorsque le rendu est terminé. Cela évite le phénomène connu sous le nom de déchirement et permet une animation plus lisse.

Chaque périphérique créé dans Direct3D a au moins une chaîne de permutation. Lorsque vous initialisez le premier périphérique Direct3D, vous définissez le membre BackBufferCount des [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md), qui indique à Direct3D le nombre de mémoires tampons d’arrière-plan qui seront dans la chaîne de permutation. L’appel à [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crée alors le périphérique Direct3D et la chaîne de permutation correspondante.

Quand vous utilisez [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) pour demander une opération de basculement de surface, les pointeurs vers la mémoire de surface pour la mémoire tampon d’arrière-plan et les mémoires tampons d’arrière-plan sont permutés. Le retournement est effectué en basculant les pointeurs que le périphérique d’affichage utilise pour référencer la mémoire, et non en copiant la mémoire de surface. Lorsqu’une chaîne de basculement contient une mémoire tampon d’arrière-plan et plusieurs mémoires tampons d’arrière-plan, les pointeurs sont basculés dans un modèle circulaire, comme indiqué dans le diagramme suivant.

![diagramme d’une chaîne de basculement avec une mémoire tampon d’avant et deux mémoires tampons d’arrière-plan](images/trplflip.png)

Vous pouvez créer des chaînes de permutation supplémentaires pour un appareil en appelant [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/desktop/api). Une application peut créer une chaîne de permutation par vue et associer chaque chaîne de permutation à une fenêtre particulière. L’application restitue des images dans les mémoires tampons d’arrière-plan de chaque chaîne de permutation, puis les présente individuellement. Les deux paramètres que **IDirect3DDevice9 :: CreateAdditionalSwapChain** prennent sont un pointeur vers une structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) et l’adresse d’un pointeur vers une interface [**IDirect3DSwapChain9**](/windows/desktop/api) . Vous pouvez ensuite utiliser [**IDirect3DSwapChain9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-present) pour afficher le contenu de la mémoire tampon d’arrière-plan suivante dans le tampon d’avant. Notez qu’un appareil ne peut avoir qu’une seule chaîne d’échange plein écran.

Vous pouvez accéder à une mémoire tampon d’arrière-plan spécifique en appelant les méthodes [**IDirect3DDevice9 :: GetBackBuffer**](/windows/desktop/api) ou [**IDirect3DSwapChain9 :: GetBackBuffer**](/windows/desktop/api) , qui retournent un pointeur vers une interface [**IDirect3DSurface9**](/windows/desktop/api) qui représente la surface de mémoire tampon d’arrière-plan retournée. Notez que l’appel de cette méthode augmente le nombre de références internes sur l’interface [**IDirect3DDevice9**](/windows/desktop/api) . par conséquent, veillez à appeler [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) lorsque vous avez fini d’utiliser cette surface ou une fuite de mémoire se produit.

Rappelez-vous que Direct3D retourne des surfaces en échangeant des pointeurs de mémoire surface dans la chaîne de permutation, et non en échangeant les surfaces elles-mêmes. Cela signifie que vous allez toujours afficher la mémoire tampon d’arrière-plan qui sera affichée ensuite.

Il est important de noter la distinction entre une « opération de basculement », telle qu’elle est effectuée par un pilote de carte d’affichage, et une opération « présente » appliquée à une chaîne de permutation créée avec D3DSWAPEFFECT \_ Flip.

Le terme « Flip » désigne une opération qui modifie la plage d’adresses de mémoire vidéo qu’un adaptateur d’affichage utilise pour générer son signal de sortie, provoquant ainsi l’affichage du contenu d’une mémoire tampon d’arrière-plan précédemment masquée. Dans Direct3D 9, le terme est souvent utilisé plus généralement pour décrire la présentation d’une mémoire tampon d’arrière-plan dans toute chaîne de permutation créée avec l' \_ effet de permutation D3DSWAPEFFECT.

Bien que ces opérations « présentes » soient presque invariablement implémentées par les opérations de basculement lorsque la chaîne de permutation est un plein écran, elles sont nécessairement implémentées par les opérations de copie lorsque la chaîne de permutation est affichée. En outre, un pilote de carte d’affichage peut utiliser le retournement pour implémenter les opérations présentes sur les chaînes d’échange plein écran en fonction de la \_ copie D3DSWAPEFFECT Discard et D3DSWAPEFFECT \_ .

La discussion ci-dessus s’applique au cas couramment utilisé d’une chaîne de permutation plein écran créée avec D3DSWAPEFFECT \_ Flip.

Pour une description plus générale des différents effets de permutation pour les chaînes de permutation à l’écran et en mode fenêtre, consultez [**D3DSWAPEFFECT**](./d3dswapeffect.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
