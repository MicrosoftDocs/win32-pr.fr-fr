---
description: D’un point de vue conceptuel, une fenêtre d’affichage est un rectangle à deux dimensions (2D) dans lequel une scène 3D est projetée.
ms.assetid: eddadaa1-9181-47fa-8530-44aa46fea286
title: Viewports et découpage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57f64d17f7abf4e370406f984fa50037be6d44e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108395"
---
# <a name="viewports-and-clipping-direct3d-9"></a>Viewports et découpage (Direct3D 9)

D’un point de vue conceptuel, une fenêtre d’affichage est un rectangle à deux dimensions (2D) dans lequel une scène 3D est projetée. Dans Direct3D, le rectangle existe en tant que coordonnées dans une surface Direct3D que le système utilise comme cible de rendu. La transformation de projection convertit les vertex dans le système de coordonnées utilisé pour la fenêtre d’affichage. Une fenêtre d’affichage est également utilisée pour spécifier la plage de valeurs de profondeur sur une surface de cible de rendu dans laquelle une scène sera restituée (généralement 0,0 à 1,0).

## <a name="the-viewing-frustum"></a>Frustum d’affichage

Un frustum de visualisation est un volume 3D dans une scène positionnée par rapport à l’appareil photo de la fenêtre d’affichage. La forme du volume affecte la façon dont les modèles sont projetés à partir de l’espace de l’appareil photo sur l’écran. Le type de projection le plus courant, une projection en perspective, est chargé de faire en sorte que les objets proches de la caméra soient plus grands que les objets à distance. Pour l’affichage en perspective, les frustum d’affichage peuvent être visualisés sous forme de pyramide, avec la caméra positionnée sur le Conseil, comme indiqué dans l’illustration suivante. Cette pyramide est croisée par un plan de découpage avant et arrière. Le volume dans la pyramide entre les plans de découpage avant et arrière est le frustum d’affichage. Les objets sont visibles uniquement lorsqu’ils sont dans ce volume.

![illustration d’un frustrum d’affichage avec un plan de découpage avant et arrière](images/frustum.png)

Si vous pensez que vous vous trouvez dans une pièce sombre et que vous regardez dans une fenêtre carrée, vous visualisez un frustum d’affichage. Dans cette analogie, le plan de découpage proche est la fenêtre et le plan de découpage arrière est tout à fait interrompre votre vue, le Skyscraper sur la rue, les montagnes dans la distance, ou rien du tout. Vous pouvez voir tout ce qui se trouve à l’intérieur de la pyramide tronquée qui commence au niveau de la fenêtre et se termine avec n’importe quel élément qui interrompt votre affichage, et vous ne voyez rien d’autre.

Le frustum d’affichage est défini par l’angle de vue (champ de vision) et par les distances des plans de découpage avant et arrière, spécifiés en coordonnées z, comme indiqué dans le diagramme suivant.

![diagramme du frustum d’affichage](images/fovdiag.png)

Dans ce diagramme, la variable D correspond à la distance entre l’appareil photo et l’origine de l’espace qui a été défini dans la dernière partie du pipeline Geometry (transformation d’affichage). Il s’agit de l’espace autour duquel vous organisez les limites de votre frustum d’affichage. Pour plus d’informations sur l’utilisation de cette variable D pour générer la matrice de projection, consultez [transformation de projection (Direct3D 9)](projection-transform.md) .

## <a name="viewport-rectangle"></a>Rectangle de la fenêtre d’affichage

Vous définissez le rectangle de la fenêtre d’affichage en C++ à l’aide de la structure [**D3DVIEWPORT9**](d3dviewport9.md) . La structure D3DVIEWPORT9 est utilisée avec les méthodes de manipulation de fenêtre d’affichage suivantes exposées par l’interface IDirect3DDevice9.

-   [**IDirect3DDevice9::GetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getviewport)
-   [**IDirect3DDevice9::SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport)

La structure D3DVIEWPORT9 contient quatre membres : X, Y, largeur, hauteur, qui définissent la zone de la surface cible de rendu dans laquelle une scène sera rendue. Ces valeurs correspondent au rectangle de destination ou au rectangle de la fenêtre d’affichage, comme indiqué dans le diagramme suivant.

![diagramme du rectangle de la fenêtre d’affichage](images/destrect.png)

Les valeurs que vous spécifiez pour les membres X, Y, Width et Height sont des coordonnées d’écran par rapport à l’angle supérieur gauche de la surface de rendu-cible. La structure définit deux membres supplémentaires (MinZ et MaxZ) qui indiquent les plages de profondeur dans lesquelles la scène sera restituée.

Direct3D part du principe que le volume du découpage de la fenêtre d’affichage est compris entre-1,0 et 1,0 dans X, et de 1,0 à-1,0 dans Y. Ce sont les paramètres utilisés le plus souvent par les applications dans le passé. Vous pouvez ajuster les proportions de la fenêtre d’affichage avant le découpage à l’aide de la [transformation de projection](projection-transform.md).

> [!Note]  
> MinZ et MaxZ indiquent les plages de profondeur dans lesquelles la scène sera rendue et ne sont pas utilisées pour le découpage. La plupart des applications définissent ces membres sur 0,0 et 1,0 pour permettre au système de s’afficher sur la plage entière de valeurs de profondeur dans le tampon de profondeur. Dans certains cas, vous pouvez obtenir des effets spéciaux à l’aide d’autres plages de profondeur. Par exemple, pour afficher un affichage de tête dans un jeu, vous pouvez définir les deux valeurs sur 0,0 pour forcer le système à restituer les objets dans une scène au premier plan, ou vous pouvez les définir à 1,0 pour afficher un objet qui doit toujours être en arrière-plan.

 

Les dimensions utilisées dans les membres X, Y, Width et Height de la structure [**D3DVIEWPORT9**](d3dviewport9.md) pour une fenêtre d’affichage définissent l’emplacement et les dimensions de la fenêtre d’affichage sur la surface de la cible de rendu. Ces valeurs sont exprimées en coordonnées d’écran, par rapport à l’angle supérieur gauche de la surface.

Direct3D utilise l’emplacement et les dimensions de la fenêtre d’affichage pour mettre à l’échelle les vertex en fonction d’une scène rendue à l’emplacement approprié sur la surface cible. En interne, Direct3D insère ces valeurs dans la matrice suivante qui est appliquée à chaque vertex.

![équation de la matrice appliquée à chaque vertex](images/vpscale.png)

Cette matrice met à l’échelle les vertex en fonction des dimensions de la fenêtre d’affichage et de la plage de profondeur souhaitée, puis les convertit à l’emplacement approprié sur la surface cible de rendu. La matrice retourne également la coordonnée y pour refléter l’origine d’un écran dans l’angle supérieur gauche avec l’incrémentation y, en descendant vers le bas. Une fois cette matrice appliquée, les vertex sont toujours homogènes, c’est-à-dire qu’ils existent toujours en tant que \[ coordonnées x, y, z et w, \] et ils doivent être convertis en coordonnées non homogènes avant d’être envoyés au rastériseur.

> [!Note]  
> La matrice de mise à l’échelle de la fenêtre d’affichage incorpore les membres MinZ et MaxZ de la structure [**D3DVIEWPORT9**](d3dviewport9.md) pour mettre à l’échelle les sommets en fonction de la plage de profondeur \[ MinZ, MaxZ \] . Cela représente une sémantique différente des versions précédentes de DirectX, dans lesquelles ces membres étaient utilisés pour le découpage.

 

> [!Note]  
> Les applications définissent généralement MinZ et MaxZ sur 0,0 et 1,0, respectivement, pour faire en sorte que le système soit rendu dans l’intégralité de la plage de profondeur. Toutefois, vous pouvez utiliser d’autres valeurs pour atteindre certains effets. Par exemple, vous pouvez définir les deux valeurs sur 0,0 pour forcer tous les objets au premier plan, ou définir à la fois sur 1,0 pour afficher tous les objets en arrière-plan.

 

## <a name="clearing-a-viewport"></a>Effacement d’une fenêtre d’affichage

La désactivation de la fenêtre d’affichage permet de réinitialiser le contenu du rectangle de la fenêtre d’affichage sur la surface de rendu-cible. Il peut également effacer le rectangle dans les surfaces de la mémoire tampon de la profondeur et du stencil.

Utilisez [**IDirect3DDevice9 :: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) pour effacer la fenêtre d’affichage. La méthode accepte un ou plusieurs rectangles qui définissent les zones de la surface qui sont effacées. Si vous affectez la valeur 1 au paramètre Count et le paramètre pRects à l’adresse d’un rectangle unique qui couvre l’intégralité de la zone de fenêtre d’affichage, la fenêtre d’affichage entière est effacée. Une autre façon d’effacer l’intégralité de la fenêtre d’affichage consiste à affecter la valeur **null** au paramètre pRects et le paramètre count à la valeur 0.

[**IDirect3DDevice9 :: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) peut être utilisé pour effacer les bits de stencil dans une mémoire tampon de profondeur. Il vous suffit de définir le paramètre Flags pour déterminer la façon dont **IDirect3DDevice9 :: Clear** fonctionne avec la cible de rendu et toute profondeur ou mémoire tampon de stencil associée. L' \_ indicateur de cible D3DCLEAR efface la fenêtre d’affichage à l’aide d’une couleur RVBA arbitraire que vous fournissez dans l’argument de couleur (il ne s’agit pas de la couleur matérielle). L' \_ indicateur D3DCLEAR ZBUFFER efface la mémoire tampon de profondeur à une profondeur arbitraire que vous spécifiez dans Z : 0,0 est la distance la plus proche, et 1,0 est la plus ancienne. L' \_ indicateur de stencil D3DCLEAR réinitialise les bits du stencil à la valeur que vous fournissez dans l’argument de gabarit. Vous pouvez utiliser des entiers compris entre 0 et 2n-1, où n est le nombre de bits de la mémoire tampon du stencil.

Dans certains cas, vous pouvez effectuer un rendu uniquement vers de petites parties de la cible de rendu et des surfaces de mémoire tampon de profondeur. Les méthodes claires vous permettent également de supprimer plusieurs zones de vos surfaces en un seul appel. Pour ce faire, définissez le paramètre count sur le nombre de rectangles que vous souhaitez effacer et spécifiez l’adresse du premier rectangle dans un tableau de rectangles dans le paramètre pRects.

## <a name="set-up-the-viewport-for-clipping"></a>Configurer la fenêtre d’affichage pour le découpage

Les résultats de la matrice de projection déterminent le volume de découpage dans l’espace de projection comme suit :

-w<sub>c</sub><= x<sub>c</sub><= w<sub>c</sub>

-w<sub>c</sub><= y<sub>c</sub><= w<sub>c</sub>

0 <= z<sub>c</sub><= w<sub>c</sub>

Où : x, y, z et w représentent les coordonnées du vertex après l’application de la transformation de projection. Tous les vertex qui ont un composant x, y ou z-en dehors de ces plages sont découpés, si le découpage est activé (comportement par défaut).

À l’exception des mémoires tampons de vertex, les applications activent ou désactivent le découpage par le biais de l’état de rendu du [**\_ découpage D3DRS**](./d3drenderstatetype.md) . Les informations de découpage pour les mémoires tampons de vertex sont générées au cours du traitement. Pour plus d’informations, consultez [traitement des vertex de fonction fixe (Direct3D 9)](fixed-function-vertex-processing.md) et [traitement programmable de vertex (Direct3D 9)](programmable-vertex-processing.md).

Direct3D n’extrait pas les sommets transformés d’une primitive à partir d’une mémoire tampon de vertex, sauf s’il provient de [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices). Si vous effectuez vos propres transformations et que vous avez besoin de Direct3D pour effectuer le découpage, vous ne devez pas utiliser de mémoires tampons de vertex. Dans ce cas, l’application parcourt les données pour la transformer. Direct3D parcourt les données une deuxième fois pour les découper, puis le pilote restitue les données, ce qui est inefficace. Par conséquent, si l’application transforme les données, doit également découper les données.

Lorsque l’appareil reçoit des sommets prétransformés et allumés (sommets T&L) qui doivent être découpés, pour effectuer l’opération de découpage, les vertex sont transformés dans l’espace de découpage à l’aide de l’espace homogène réciproque du vertex (RHW) et des informations de la fenêtre d’affichage. Le découpage est ensuite effectué. Tous les appareils ne sont pas en charge de l’exécution de cette transformation en arrière afin de découper les sommets T&L.

La \_ fonctionnalité de l’appareil D3DPMISCCAPS CLIPTLVERTS indique si l’appareil est capable de découper les vertex T&L. Si cette fonctionnalité n’est pas définie, l’application est chargée de découper les sommets T&L qu’elle envisage d’envoyer à l’appareil pour qu’elle soit rendue. L’appareil est toujours en capacité de découper les vertex T&L dans le mode de traitement du vertex logiciel (que l’appareil soit créé dans le mode de traitement du vertex logiciel ou basculé vers le mode de traitement du vertex logiciel).

La seule exigence pour configurer les paramètres de la fenêtre d’affichage pour un appareil de rendu consiste à définir le volume de découpage de la fenêtre d’affichage. Pour ce faire, vous devez initialiser et définir des valeurs de découpage pour le volume de découpage et pour la surface de cible de rendu. Les fenêtres d’affichage sont généralement configurées pour être rendues dans la zone complète de la surface de la cible de rendu, mais ce n’est pas une exigence.

Vous pouvez utiliser les paramètres suivants pour les membres de la structure [**D3DVIEWPORT9**](d3dviewport9.md) pour y parvenir en C++.


```
D3DVIEWPORT9 viewData = { 0, 0, width, height, 0.0f, 1.0f };
```



Après avoir défini les valeurs dans la structure [**D3DVIEWPORT9**](d3dviewport9.md) , appliquez les paramètres de la fenêtre d’affichage à l’appareil en appelant sa méthode [**IDirect3DDevice9 :: SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) . L’exemple de code suivant illustre ce à quoi peut ressembler cet appel.


```
HRESULT hr;

hr = pd3dDevice->SetViewport(&viewData);
if(FAILED(hr))
    return hr;
```



Si l’appel s’effectue correctement, les paramètres de la fenêtre d’affichage sont définis et prendront effet lors de l’appel de la méthode de rendu suivante. Pour apporter des modifications aux paramètres de la fenêtre d’affichage, il vous suffit de mettre à jour les valeurs de la structure [**D3DVIEWPORT9**](d3dviewport9.md) et d’appeler à nouveau [**IDirect3DDevice9 :: SetViewport**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport) .

> [!Note]  
> Les membres de la structure [**D3DVIEWPORT9**](d3dviewport9.md) minz et MaxZ indiquent les plages de profondeur dans lesquelles la scène sera rendue et ne sont pas utilisées pour le découpage. La plupart des applications définissent ces membres sur 0,0 et 1,0 pour permettre au système de s’afficher dans l’intégralité de la plage de valeurs de profondeur dans le tampon de profondeur. Dans certains cas, vous pouvez obtenir des effets spéciaux à l’aide d’autres plages de profondeur. Par exemple, pour afficher un affichage de tête dans un jeu, vous pouvez définir les deux valeurs sur 0,0 pour forcer le système à restituer les objets dans une scène au premier plan, ou vous pouvez les définir à 1,0 pour afficher un objet qui doit toujours être en arrière-plan.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> </dl>

 

 
