---
description: Le contenu de la texture est souvent stocké au format sRGB.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cea4b3ba224452e1c3be8f96b7136f4e4f649c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106542875"
---
# <a name="gamma-direct3d-9"></a>Gamma (Direct3D 9)

Le contenu de la texture est souvent stocké au format sRGB. Traditionnellement, les pipelines de pixels supposaient que les couleurs soient linéaires afin que les opérations de fusion aient été effectuées dans l’espace linéaire. Toutefois, étant donné que le contenu sRVB est corrigé, les opérations de fusion dans l’espace linéaire produisent des résultats incorrects. Les cartes vidéo peuvent désormais résoudre ce problème en annulant la correction gamma lors de la lecture de tout contenu sRVB, et en reconvertissant les données en pixels au format sRVB lors de l’écriture de pixels. Dans ce cas, toutes les opérations à l’intérieur du pipeline de pixels sont effectuées dans l’espace linéaire.

## <a name="gamma-correction"></a>Correction gamma

Direct3D 9 peut :

-   Indiquez si une texture est gamma 2,2 corrigé ou non (sRVB ou non). Le pilote est converti en valeur gamma linéaire pour les opérations de fusion au moment de la SetTexture, ou l’échantillonneur le convertit en données linéaires au moment de la recherche.
-   Indiquez si le pipeline de pixels doit être corrigé de nouveau dans l’espace sRVB lors de l’écriture dans la cible de rendu.

Toutes les autres couleurs (couleur claire, couleur matérielle, couleur de vertex, etc.) sont supposées être dans l’espace linéaire. Les applications peuvent corriger la gamma des couleurs écrites dans la mémoire tampon de trame à l’aide d’instructions de nuanceur de pixels. La linéarisation doit être appliquée uniquement aux canaux RVB et non au canal alpha.

Tous les formats de surface ne peuvent pas être linéarisés. Seuls les formats qui passent [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec la \_ requête D3DUSAGE \_ SRGBREAD peuvent être linéarisés. L’état de l’échantillonneur D3DSAMP \_ SRGBTEXTURE est ignoré pour le reste. Seuls les formats de texture non signés sont supposés prendre en charge cette conversion. Les formats de texture non signés incluent uniquement les composants R, G, B et L. Si le canal alpha est présent, il est ignoré. Si les formats mixtes prennent en charge la linéarisation sRVB, seuls les canaux non signés sont affectés. Dans l’idéal, le matériel doit effectuer la linéarisation avant de filtrer, mais dans Direct3D 9, le matériel est autorisé à effectuer la linéarisation après le filtrage.

Tous les formats de surface ne peuvent pas être écrits dans un espace sRVB. Seuls les formats qui passent le [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec l’indicateur d’utilisation D3DUSAGE de \_ requête \_ SRGBWRITE peuvent être linéarisés. L’état de rendu D3DRS \_ SRGBWRITEENABLE est ignoré pour le reste. Huit bits par canal les formats RVB non signés sont censés exposer cette capacité.

Dans l’idéal, le matériel doit effectuer les opérations de fusion de mémoire tampon de trame dans l’espace linéaire, mais le matériel est autorisé à l’exécuter après le nuanceur de pixels mais avant le mélangeur de mémoires tampons de trames. Cela signifie que les opérations de fusion de mémoire tampon de trame qui ont lieu dans l’espace sRVB produiront des résultats incorrects. D3DRS \_ SRGBWRITEENABLE est respecté tout en effectuant une suppression de la cible de rendu. Pour le matériel qui prend en charge [plusieurs cibles de rendu (Direct3D 9)](multiple-render-targets.md) ou des [textures à plusieurs éléments (Direct3D 9)](multiple-element-textures.md), seule la première cible de rendu ou l’élément est écrit.

### <a name="api-changes"></a>Modifications de l’API


```
// New sampler state (DWORD)
// If this is nonzero, the texture is linearized on lookup.
D3DSAMP_SRGBTEXTURE       // Default FALSE

// New render state (DWORD)
D3DRS_SRGBWRITEENABLE     // Default FALSE

// New usage flags
D3DUSAGE_QUERY_SRGBWRITE
D3DUSAGE_QUERY_SRGBREAD
```



### <a name="windowed-swap-chains"></a>Chaînes de permutation avec fenêtres

Il est utile pour les applications de conserver les mémoires tampons d’arrière-plan de leurs chaînes de permutation dans un espace linéaire afin d’activer des opérations de fusion correctes. Étant donné que le bureau n’est généralement pas dans un espace linéaire, une correction gamma est nécessaire avant que le contenu de la mémoire tampon d’arrière-plan puisse être présenté. L’application peut appliquer cette correction en allouant une mémoire tampon supplémentaire et en effectuant sa propre copie de correction à partir de la mémoire tampon linéaire vers la mémoire tampon d’arrière-plan. Cela nécessite une copie supplémentaire qui peut être évitée si le pilote effectue une correction gamma dans le cadre de la fusion de la présentation.

Dans Direct3D 9, un nouvel indicateur, [D3DPRESENT \_ Linear \_ content](d3dpresent.md), est disponible [**pour permettre à la**](/windows/desktop/api) présentation de convertir implicitement l’espace linéaire en sRGB/gamma 2,2. Les applications doivent spécifier cet indicateur si le format de la mémoire tampon est une virgule flottante de 16 bits afin de faire correspondre le mode de fenêtrage présent au comportement gamma plein écran, à condition que la \_ Présentation D3DCAPS3 linéaire \_ à \_ sRVB \_ soit renvoyée pour les fonctionnalités d’appareil récupérées via [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoire tampon de trame](frame-buffer.md)
</dt> </dl>

 

 
