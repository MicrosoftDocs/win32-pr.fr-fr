---
title: Étape de Output-Merger
description: L’étape de fusion de sortie (OM) génère la couleur de pixel rendue finale à l’aide d’une combinaison de l’état du pipeline, des données de pixels générées par les nuanceurs de pixels, du contenu des cibles de rendu et du contenu des mémoires tampons de profondeur/stencil.
ms.assetid: 8be68c15-2deb-4804-b683-30080a876189
keywords:
- étape de fusion de sortie (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8de2851fdea3a22cc42033d2c13454be72ba8ab
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335213"
---
# <a name="output-merger-stage"></a>Étape de Output-Merger

L’étape de fusion de sortie (OM) génère la couleur de pixel rendue finale à l’aide d’une combinaison de l’état du pipeline, des données de pixels générées par les nuanceurs de pixels, du contenu des cibles de rendu et du contenu des mémoires tampons de profondeur/stencil. L’étape OM est la dernière étape permettant de déterminer les pixels visibles (avec test des stencils de profondeur) et de fusionner les couleurs finales des pixels.



Différences entre Direct3D 9 et Direct3D 10 :

- Direct3D 9 implémente le test alpha (à l’aide de l' [État alpha-test](/windows/desktop/direct3d9/alpha-testing-state)) pour contrôler si un pixel est écrit dans une cible de rendu de sortie.
- Direct3D 10 et les versions ultérieures n’implémentent pas un test alpha (ou un état de test alpha). Cela peut être contrôlé à l’aide d’un nuanceur de pixels ou avec la fonctionnalité de profondeur/gabarit.



 

## <a name="depth-stencil-testing-overview"></a>Vue d’ensemble du test Depth-Stencil

Une mémoire tampon de stencil de profondeur, créée en tant que ressource de texture, peut contenir à la fois des données de profondeur et des données de stencil. Les données de profondeur sont utilisées pour déterminer les pixels les plus proches de l’appareil photo, et les données du stencil sont utilisées pour masquer les pixels qui peuvent être mis à jour. Au final, les données de la profondeur et de la valeur du stencil sont utilisées par l’étape de fusion de sortie pour déterminer si un pixel doit être dessiné ou non. Le diagramme suivant illustre le fonctionnement conceptuel du test des stencils de profondeur.

![Diagramme illustrant le fonctionnement du test des stencils de profondeur](images/d3d10-depth-stencil-test.png)

Pour configurer le test des stencils de profondeur, consultez [Configuration des fonctionnalités de Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md). Un objet de stencil de profondeur encapsule l’état de gabarit de profondeur. Une application peut spécifier l’état du stencil de profondeur, ou l’étape OM utilisera les valeurs par défaut. Les opérations de fusion sont effectuées par pixel si l’échantillonnage multiple est désactivé. Si l’échantillonnage multiple est activé, la fusion se produit sur une base par échantillonnage multiple.

Le processus d’utilisation de la mémoire tampon de profondeur pour déterminer le pixel à dessiner est appelé mise en mémoire tampon de profondeur, également parfois appelé mise en mémoire tampon z.

Une fois les valeurs de profondeur atteintes à l’étape de fusion de sortie (qu’elles proviennent d’une interpolation ou d’un nuanceur de pixels), elles sont toujours ancrées : z = min (Viewport. MaxDepth, Max (Viewport. MinDepth, z)) en fonction du format/précision de la mémoire tampon de profondeur, à l’aide de règles à virgule flottante. Après le verrouillage, la valeur de profondeur est comparée (à l’aide de DepthFunc) à la valeur de mémoire tampon de profondeur existante. Si aucun tampon de profondeur n’est lié, le test de profondeur passe toujours.

S’il n’existe aucun composant de stencil dans le format de mémoire tampon de profondeur, ou si aucune limite de mémoire tampon de profondeur n’est liée, le test de stencil passe toujours. Dans le cas contraire, la fonctionnalité n’est pas modifiée à partir de Direct3D 9.

Une seule mémoire tampon de gabarit ou de profondeur peut être active à la fois ; toute vue de ressource liée doit correspondre (taille et dimensions identiques) à la vue de la profondeur/du gabarit. Cela ne signifie pas que la taille de la ressource doit être la même que la taille de la vue doit correspondre.

Pour plus d’informations sur le test des stencils de profondeur, consultez le [didacticiel 14](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="blending-overview"></a>Vue d’ensemble de la fusion

La fusion combine une ou plusieurs valeurs de pixel pour créer une couleur de pixel finale. Le diagramme suivant illustre le processus impliqué dans la fusion de données de pixels.

![Diagramme illustrant le fonctionnement de la fusion de données](images/d3d10-blend-state.png)

Conceptuellement, vous pouvez visualiser ce graphique de Flow implémenté deux fois dans l’étape de fusion de sortie : la première fusionne les données RVB, alors qu’en parallèle, une deuxième fusionne les données alpha. Pour savoir comment utiliser l’API pour créer et définir l’état de fusion, consultez Configuration de la [fonctionnalité de fusion](d3d10-graphics-programming-guide-blend-state.md).

La fonction Fixed-Blend peut être activée indépendamment pour chaque cible de rendu. Toutefois, il n’existe qu’un seul jeu de contrôles Blend, de sorte que le même lissage est appliqué à tous les RenderTargets avec la fusion activée. Les valeurs de fusion (y compris BlendFactor) sont toujours ancrées à la plage du format de cible de rendu avant la fusion. Le verrouillage est effectué par cible de rendu, en respectant le type de cible de rendu. La seule exception concerne les formats float16, float11 ou float10 qui ne sont pas ancrées afin que les opérations de fusion sur ces formats puissent être effectuées avec une précision ou une plage au moins égale à celle du format de sortie. Les zéros de NaN et signés sont propagés dans tous les cas (y compris les poids de fusion 0,0).

Lorsque vous utilisez des cibles de rendu sRVB, le Runtime convertit la couleur de la cible de rendu en espace linéaire avant d’effectuer la fusion. Le Runtime convertit la dernière valeur fusionnée en espace sRVB avant de l’enregistrer à nouveau dans la cible de rendu.

Différences entre Direct3D 9 et Direct3D 10 :

- Dans Direct3D 9, la fusion de fonction fixe peut être activée indépendamment pour chaque cible de rendu.
- Dans Direct3D 10 et versions ultérieures, il existe une seule Description de l’état de fusion. par conséquent, une valeur de fusion peut être définie pour toutes les cibles de rendu.



 

### <a name="dual-source-color-blending"></a>Dual-Source de la fusion des couleurs

Cette fonctionnalité permet à l’étape de fusion de sortie d’utiliser simultanément des sorties de nuanceur de pixels (o0 et O1) comme entrées d’une opération de fusion avec la cible de rendu unique à l’emplacement 0. Les opérations de fusion valides sont les suivantes : Add, Subtract et revsubtract. Les options de fusion valides pour SrcBlend, DestBlend, SrcBlendAlpha ou DestBlendAlpha incluent : **d3d11 \_ Blend \_ src1 \_ Color**, **d3d11 \_ Blend \_ INV \_ src1 \_ Color**, **d3d11 \_ Blend \_ src1 \_ alpha**, **d3d11 \_ Blend \_ INV \_ src1 \_ alpha**. L’équation de fusion et le masque d’écriture de sortie spécifient les composants que le nuanceur de pixels est en train de sortir. Les composants supplémentaires sont ignorés.

L’écriture dans d’autres sorties de nuanceur de pixels (O2, O3, etc.) n’est pas définie. vous ne pouvez pas écrire dans une cible de rendu si elle n’est pas liée à l’emplacement 0. L’écriture de oDepth est valide pendant la fusion de couleurs à double source.

Pour obtenir des exemples, consultez [fusion de sorties de nuanceur de pixels](d3d10-graphics-programming-guide-blend-state.md).

## <a name="multiple-rendertargets-overview"></a>Vue d’ensemble de plusieurs RenderTargets

Un nuanceur de pixels peut être utilisé pour effectuer le rendu sur au moins 8 cibles de rendu distinctes, qui doivent toutes être du même type (buffer, Texture1D, Texture1DArray, etc.). En outre, toutes les cibles de rendu doivent avoir la même taille dans toutes les dimensions (largeur, hauteur, profondeur, taille de tableau, nombre d’échantillons). Chaque cible de rendu peut avoir un format de données différent.

Vous pouvez utiliser n’importe quelle combinaison d’emplacements de cibles de rendu (jusqu’à 8). Toutefois, un affichage des ressources ne peut pas être lié à plusieurs emplacements de rendu-cible simultanément. Une vue peut être réutilisée tant que les ressources ne sont pas utilisées simultanément.

## <a name="output-write-mask-overview"></a>Vue d’ensemble du masque de Output-Write

Utilisez un masque d’écriture de sortie pour contrôler (par composant) les données qui peuvent être écrites dans une cible de rendu.

## <a name="sample-mask-overview"></a>Présentation de l’exemple de masque

Un exemple de masque est un masque de couverture à exemple de 32 bits qui détermine les exemples qui sont mis à jour dans les cibles de rendu actives. Un seul exemple de masque est autorisé. Le mappage des bits dans un exemple de masque aux exemples d’une ressource est défini par un utilisateur. Pour le rendu n-Sample, les n premiers bits (à partir du LSB) de l’échantillon de masque sont utilisés (32 bits le nombre maximal de bits).


## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                    | Description                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Configuration de la fonctionnalité Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md)<br/> | Cette section décrit les étapes de configuration de la mémoire tampon du stencil de profondeur et l’état du gabarit de profondeur pour l’étape de fusion de sortie.<br/>                                                                                                                           |
| [Configuration de la fonctionnalité de fusion](d3d10-graphics-programming-guide-blend-state.md)<br/>        | Les opérations de fusion sont effectuées sur chaque sortie de nuanceur de pixels (valeur RVBA) avant que la valeur de sortie ne soit écrite dans une cible de rendu. Si l’échantillonnage multiple est activé, la fusion est effectuée sur chaque échantillon multiple ; dans le cas contraire, la fusion est effectuée sur chaque pixel.<br/> |
| [Décalage de profondeur](d3d10-graphics-programming-guide-output-merger-stage-depth-bias.md)<br/>             | Les polygones en espace 3D peuvent être affichés comme s’ils n’étaient pas coplanés en ajoutant un biais (ou un biais de profondeur) à chacun d’eux.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pipeline graphique](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Étapes de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

