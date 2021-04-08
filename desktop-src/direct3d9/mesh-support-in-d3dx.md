---
description: D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Prise en charge des maillages dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0b2b1dd0e5d4c5a212005afe400bb559f1689a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103949960"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Prise en charge des maillages dans D3DX (Direct3D 9)

D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.

## <a name="meshes"></a>Maillages

D3DX implémente la construction de maillage pour charger, manipuler et restituer le contenu du fichier. x. Une maille est fondamentalement une collection de vertex définissant une géométrie et un ensemble d’index définissant les visages. Il existe plusieurs types de maillage.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fournit les notions de base. [**ID3DXMesh**](id3dxmesh.md) hérite de ID3DXBaseMesh et ajoute l’optimisation de maillage à l’aide du cache de vertex par puce. [**ID3DXSkinInfo**](id3dxskininfo.md) fournit la prise en charge des maillages dépouillés.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fournit des méthodes pour manipuler et interroger les objets de maillage [**ID3DXMesh**](id3dxmesh.md) , qui héritent du maillage de base. Cela comprend les opérations d’adjacence, la récupération de la mémoire tampon Geometry, les opérations de verrouillage/déverrouillage (vertex et index) et les informations de copie, de rendu, de face et de vertex.

> [!Note]  
> Les interfaces ID3DXPMesh et ID3DXSPMesh (pour prendre en charge les maillages progressifs et simplifiés, respectivement) disponibles dans les versions antérieures de Direct3D 9 ont été supprimées.

 

## <a name="mesh-architecture"></a>Architecture de maillage

Une maille contient les données d’un modèle complexe. Il s’agit d’un conteneur de données abstraites qui contient des ressources telles que des textures et des matériaux, ainsi que des attributs tels que des données de position et des données de contiguïté. Il existe plusieurs opérations de maillage qui améliorent les performances de dessin et l’apparence d’une surface. En outre, il existe un certain nombre d’autres concepts de maillage qui affecteront les fonctionnalités des opérations de maillage. La compréhension de ces concepts de maille pour vous permettre de les appliquer améliorera les performances du maillage.

## <a name="mesh-object-data"></a>Données d’objet de maillage

Un maillage contient une mémoire tampon de vertex, une mémoire tampon d’index et une mémoire tampon d’attribut.

-   La mémoire tampon de vertex contient les données de vertex, qui sont les vertex de maillage.
-   Le tampon d’index contient des indices de vertex pour accéder à la mémoire tampon de vertex. Cela peut réduire la taille de la mémoire tampon du vertex en réduisant les vertex en double. Seul un maillage indexé utilise la mémoire tampon d’index. Si un maillage est constitué d’une liste de triangles, par exemple, il n’utilise pas la mémoire tampon d’index.
-   La mémoire tampon d’attribut contient des données d’attribut. Les attributs sont des propriétés des vertex de maillage, sans ordre particulier. Un maillage D3DX stocke des attributs dans un groupe de DWORDs, pour chaque visage.

### <a name="attribute-tables"></a>Tables d’attributs

Une table d’attributs est une représentation concise du contenu d’une mémoire tampon d’attribut. Les tables d’attributs peuvent être créées en appelant l’une des méthodes optimize avec D3DXMESHOPT \_ ATTRSORT, en verrouillant la mémoire tampon d’attribut et en la remplissant avec des données, ou en appelant SetAttributeTable. Une maille contient une table d’attributs lorsque la maille est réorganisée en groupes. Cela se produit lorsque l’optimisation est appelée, en supposant qu’une option de tri d’attribut (D3DXMESHOPT \_ ATTRSORT ou version ultérieure) est fournie. Les maillages D3DX utilisent des listes de triangles indexées et sont donc dessinés avec [**IDirect3DDevice9 ::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Les tables d’attributs sont créées suite à l’appel de la fonction optimize. Les visages n’ont pas besoin d’être adjacents, car l’optimisation les réorganisera pour être adjacentes. Par exemple, les mains d’un maillage humain peuvent utiliser le même attribut. L’ID permet de trier les visages en groupes. Les maillages des fichiers. x ont généré automatiquement des attributs pour les propriétés Material et texture. Vous devez appeler optimize (ATTRSORT) ou l’optimisation plus efficace (VERTEXCACHE) pour obtenir de bonnes performances. Les fonctions Load essaient de présenter les données dans le formulaire exact dans lequel elles ont été enregistrées. Si vous utilisez un maillage basé sur une mémoire tampon de vertex/d’index, l’API de maillage fournit des fonctions d’optimisation et des transformations d’apparence avec peu de surcharge.

Les types d’optimisation sont cumulatifs, en partant du moins optimal (D3DXMESHOPT \_ compact) au meilleur (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER effectue un tri de compactage et d’attribut. D3DXMESHOPT \_ VERTEXCACHE est toujours recommandé, même sur les appareils sans un véritable cache de vertex.

## <a name="application-data"></a>Données d'application

Les données d’application sont des données de maillage gérées par une application. Il existe un couplage étroit entre les données de vertex de maillage et les données gérées par ces mémoires tampons.

La mémoire tampon de matériaux contient n matériaux. Les documents sont retournés par la fonction Load lorsque le fichier. x est chargé. Chaque sous-ensemble peut avoir ses propres matériaux et textures. La mémoire tampon de matériaux est statique.

La mémoire tampon d’adjacence contient des informations sur les bords, les visages et les visages adjacents. Certaines opérations de maillage dépendent de savoir quelles faces sont adjacentes les unes aux autres. Ces informations, appelées données d’contiguïté, sont conservées dans une mémoire tampon de contiguïté. Il ne fait pas partie de la maille mais est géré par l’application et doit être fourni aux méthodes de maillage si nécessaire.

La mémoire tampon d’instance Effects contient une liste d’instances d’effet. Une instance Effect stocke l’État. Ces informations d’État sont utilisées pour initialiser le pipeline. Une instance Effect contient des paires nom-valeur dans un effet.

## <a name="advanced-mesh-topics"></a>Rubriques avancées sur le maillage

Les maillages optimisés sont basés sur la fonctionnalité de maillage de base et ajoutent une fonctionnalité d’optimisation du cache de vertex avec deux méthodes : Optimize, qui crée un nouveau maillage et OptimizeInPlace, qui modifie le maillage d’origine.

D3DXGeneratePMesh utilise l’algorithme de simplification D3DX pour générer un maillage progressif à partir du maillage d’entrée. D3DXSimplifyMesh génère une maille standard du niveau de détail donné à partir d’un maillage d’entrée à l’aide du même algorithme de simplification. L’utilisateur contrôle la métrique d’erreur utilisée par le biais des pondérations spécifiées pour le composant par vertex et des pondérations spécifiées par vertex. Les pondérations par composant sont multipliées par la partie des composants de l’erreur calculée par réduction de bord. Les pondérations par vertex sont multipliées par la valeur de métrique d’erreur déterminée pour la suppression de ce vertex. Par exemple, si vous ne souhaitez pas qu’un sommet soit supprimé, définissez le poids de ce vertex spécifique sur une valeur élevée. Inversement, si vous voulez qu’elle soit supprimée précédemment, définissez-la sur une petite valeur (inférieure à 1).

[**ID3DXSkinInfo**](id3dxskininfo.md) prend en charge les caractères dépouillés. Un caractère dépouillé est défini par un ensemble de mailles et un ensemble d’os qui affectent les vertex des mailles. Les segments sont représentés sous la forme d’une hiérarchie de transformation. Pour chaque maille, il existe une matrice pour chaque segment qui l’affecte, ce qui transforme le maillage en espace de coordonnées local du segment. Cette matrice correspond à la transformation de l’espace à l’espacement du segment pour la maille. Elle est définie au moment où la structure est associée à la maille dans le processus de création.

### <a name="skinning"></a>Apparence

Le dépouillement est une technique permettant de transformer des vertex de maillage à l’aide d’os. Les segments sont généralement organisés dans une structure hiérarchique, comme les segments d’un corps humain. Les vertex d’objets sont ensuite associés aux segments, comme l’attachement de l’apparence aux segments. Lorsque les segments sont transformés, l’apparence est également transformée.

Les maillages dépouillés utilisent des segments pour influencer un certain nombre de vertex. Les données de transformation osseuse sont fournies par l’utilisateur, afin d’influencer le désrtment des segments. La maille utilise les segments transformés pour influencer les vertex associés aux segments. Les palettes sont des tableaux de transformations SRT. Les palettes sont souvent implémentées sous forme de matrices, mais elles peuvent contenir des valeurs SRT.

### <a name="progressive-mesh-trimming"></a>Découpage de maillage progressif

Les zones de détail faibles peuvent se permettre de perdre des vertex qui ne modifient pas l’apparence rendue de l’aire. Cela est particulièrement vrai pour les objets lorsqu’ils s’éloignent de l’appareil photo. C’est ce que l’on appelle le niveau de détail. Les utilisateurs disposent de contrôles de rendu au niveau de l’API pour définir le niveau de détail afin d’optimiser l’efficacité du rendu.

Les objets de maillage progressif commencent par un grand nombre de visages et simplifient l’utilisation pour réduire le nombre de visages. Une maille progressive indépendante est appelée maille progressive indépendante de la vue (VIPM).

Une autre façon de réduire le nombre de faces consiste à les tronquer. Cela supprime en fait les vertex et les faces de la maille. La troncation peut être effectuée à l’extrémité supérieure (pour limiter le nombre maximal de faces) ou à l’extrémité inférieure (pour limiter le nombre minimal de visages). Le découpage améliore les performances de dessin ; Toutefois, il est préférable d’utiliser la prudence pour préserver la qualité visuelle. La suppression est illustrée dans l’exemple du kit de développement logiciel (SDK) de maille progressive.

Pour les zones de visibilité élevée, la résolution peut être augmentée à l’aide d’un niveau de détail progressif (PLOD). Il s’agit d’une technique permettant de diviser une face unique en deux visages.

### <a name="patch-meshes"></a>Maillages de correctifs

Deux types spécialisés de maillages de correctifs sont également pris en charge : les carreaux de rectangle et de triangle. La maille de correction du rectangle est un filet de correction dont les points de contrôle sont disposés dans une séquence rectangulaire. Les correctifs de rectangle et de triangle permettent de créer des surfaces de poids fort. Elles ne sont pas aussi couramment utilisées que les maillages de triangle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 
