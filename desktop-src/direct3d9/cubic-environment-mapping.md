---
description: Les cartes d’environnement cubiques, parfois appelées « mappages de cube », sont des textures qui contiennent des données d’image représentant la scène entourant un objet, comme si l’objet était au centre d’un cube.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Mappage d’environnement cubique (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b02f86528c52c2e8e9376eb92e4452735c2613cc9b7dda08a8a07e8473193ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565339"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Mappage d’environnement cubique (Direct3D 9)

Les cartes d’environnement cubiques, parfois appelées « mappages de cube », sont des textures qui contiennent des données d’image représentant la scène entourant un objet, comme si l’objet était au centre d’un cube. Chaque face de la carte d’environnement cubique couvre un champ de vue de 90 degré dans le sens horizontal et vertical, et il existe six visages par mappage de cube. L’orientation des visages est présentée dans l’illustration suivante.

![illustration d’un cube avec des axes de coordonnées centrales perpendiculaires aux visages de cube](images/cubemap-cube.png)

Chaque face du cube est orientée perpendiculairement au plan x/y, y/z ou x/z, dans l’espace universel. L’illustration suivante montre comment chaque plan correspond à un visage.

![illustration de faces de cube avec des projections de coordonnées à partir de plans](images/cube-faces.png)

Les mappages d’environnement cubiques sont implémentés sous la forme d’une série d’objets texture. Les applications peuvent utiliser des images statiques pour le mappage d’environnement cubique, ou elles peuvent être rendues dans les faces du mappage de cube pour effectuer un mappage d’environnement dynamique. Cette technique exige que les surfaces du mappage de cube soient des surfaces de cible de rendu valides, créées avec l' \_ indicateur D3DUSAGE RENDERTARGET défini.

Les visages d’un mappage de cube n’ont pas besoin de contenir des rendus extrêmement détaillés de la scène environnante. Dans la plupart des cas, les mappages d’environnement sont appliqués à des surfaces courbées. Compte tenu de la quantité de courbure utilisée par la plupart des applications, la distorsion réfléchissante résultante est beaucoup plus détaillée dans la cartographie des environnements, en termes de mémoire et de charge de rendu.

## <a name="mipmapped-cubic-environment-maps"></a>Cartes de l’environnement cubique Mipmapped

Les mappages de cube peuvent être mipmapped. Pour créer un mappage de cube mipmapped, définissez le paramètre levels de la méthode [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) sur le nombre de niveaux souhaité. Vous pouvez envisager la topographie de ces surfaces comme indiqué dans le diagramme suivant.

![diagramme d’un mappage de cube mipmapped avec n niveaux MIP](images/cubemap-mipped.png)

Les applications qui créent des cartes d’environnement cubiques mipmapped peuvent accéder à chaque visage en appelant la méthode [**GetCubeMapSurface**](/windows/desktop/api) . Commencez par définir la valeur appropriée à partir du type énuméré [**D3DCUBEMAP \_ faces**](./d3dcubemap-faces.md) , comme indiqué dans [création de surfaces de mappage d’environnement cubique (Direct3D 9)](creating-cubic-environment-map-surfaces.md). Ensuite, sélectionnez le niveau à récupérer en définissant le paramètre de niveau **GetCubeMapSurface** sur le niveau de mipmap souhaité. N’oubliez pas que 0 correspond à l’image de niveau supérieur.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>coordonnées de Texture pour l’environnement cubique Cartes

Les coordonnées de texture qui indexent une carte d’environnement cubique ne sont pas des coordonnées de style u, v simples, telles qu’elles sont utilisées lorsque les textures standard sont appliquées. En fait, les mappages d’environnement cubique n’utilisent pas du tout des coordonnées de texture. À la place d’un ensemble de coordonnées de texture, les mappages d’environnement cubique requièrent un vecteur 3D. Vous devez veiller à spécifier un format de vertex correct. En plus d’indiquer au système le nombre de jeux de coordonnées de texture que votre application utilise, vous devez fournir des informations sur le nombre d’éléments dans chaque ensemble. Direct3D offre le jeu de macros [**\_ TEXCOORDSIZEN D3DFVF**](d3dfvf-texcoordsizen.md) à cet effet. Ces macros acceptent un seul paramètre, identifiant l’index du jeu de coordonnées de texture pour lequel la taille est décrite. Dans le cas d’un vecteur 3D, vous incluez le modèle binaire créé par la \_ macro D3DFVF TEXCOORDSIZE3. L’exemple de code suivant montre comment cette macro est utilisée.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



Dans certains cas, tels que le mappage de lumière diffuse, vous utilisez la normale de vertex d’espace de caméra pour le vecteur. Dans d’autres cas, comme le mappage d’environnement spéculaire, vous utilisez un vecteur de réflexion. Étant donné que les normales des sommets transformés sont largement comprises, les informations qui se concentrent sur le calcul d’un vecteur de réflexion.

Le calcul d’un vecteur de réflexion par vous-même nécessite une compréhension de la position de chaque vertex et d’un vecteur du point de vue de ce vertex. Direct3D peut calculer automatiquement les vecteurs de réflexion pour votre géométrie. L’utilisation de cette fonctionnalité permet d’économiser de la mémoire, car vous n’avez pas besoin d’inclure des coordonnées de texture pour la carte d’environnement. Cela réduit également la bande passante et, dans le cas d’un appareil de la couche d’abstraction T&L, il peut être beaucoup plus rapide que les calculs que votre application peut créer de manière autonome. Pour utiliser cette fonctionnalité, dans l’étape de texture qui contient le mappage d’environnement cubique, définissez l’état de l' \_ étape de texture D3DTSS TEXCOORDINDEX sur une combinaison du \_ membre D3DTSS TCI \_ CAMERASPACEREFLECTIONVECTOR de [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) et l’index d’un jeu de coordonnées de texture. Dans certaines situations, comme le mappage de lumière diffuse, vous pouvez utiliser \_ le \_ membre D3DTSS TCI CAMERASPACENORMAL de **D3DTEXTURESTAGESTATETYPE**, ce qui amène le système à utiliser le vecteur d’adressage de la texture transformé, espace caméra, normal. L’index est utilisé uniquement par le système pour déterminer le mode d’habillage de la texture.

L’exemple de code suivant montre comment cette valeur est utilisée.


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



Lorsque vous activez la génération automatique de coordonnées de texture, le système utilise l’une des deux formules pour calculer le vecteur de réflexion pour chaque vertex. Lorsque l' \_ État de rendu D3DRS LOCALVIEWER est défini sur **true**, la formule suivante est utilisée.

![formule du vecteur de réflexion (r = 2 (exn) n-e)](images/reflection-vector-local.png)

Dans la formule précédente, R est le vecteur de réflexion qui est calculé, E est le vecteur de position à œil normalisé, et N est le vertex de l’espace de caméra normal.

Lorsque l' \_ État de rendu D3DRS LOCALVIEWER est défini sur **false**, le système utilise la formule suivante.

![formule du vecteur de réflexion (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Les éléments R et N de cette formule sont identiques à la formule précédente. L’élément N<sub>z</sub> est l’espace universel Z du vertex normal, et I est le vecteur (0, 0, 1) d’un point de vue distant infini. Le système utilise le vecteur de réflexion de l’une des formules pour sélectionner et traiter la face appropriée du mappage de cube.

> [!Note]  
> Dans la plupart des cas, les applications doivent activer la normalisation automatique des normales des vertex. Pour ce faire, affectez \_ à D3DRS NORMALIZENORMALS la **valeur true**. Si vous n’activez pas cet état de rendu, l’apparence de la carte d’environnement sera radicalement différente de ce que vous pourriez vous attendre.

 

Des informations supplémentaires sont fournies dans la rubrique suivante.

-   [Création de surfaces de mappage d’environnement cubique (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage d’environnement](environment-mapping.md)
</dt> </dl>

 

 
