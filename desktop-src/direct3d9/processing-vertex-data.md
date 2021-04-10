---
description: L’interface IDirect3DDevice9 prend en charge le traitement des vertex dans les logiciels et le matériel.
ms.assetid: c1ac0382-1701-40e4-967a-d400ada96533
title: Traitement des données de vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d350dee4c8de361d02d0d0844968298534ee47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846590"
---
# <a name="processing-vertex-data-direct3d-9"></a>Traitement des données de vertex (Direct3D 9)

L’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) prend en charge le traitement des vertex dans les logiciels et le matériel. En général, les fonctionnalités de l’appareil pour le traitement des vertex logiciels et matériels ne sont pas identiques. Les fonctionnalités matérielles sont variables, en fonction de l’adaptateur d’affichage et du pilote, tandis que les fonctionnalités logicielles sont fixes.

Les indicateurs suivants contrôlent le comportement de traitement des vertex pour la couche d’abstraction matérielle (HAL) et les périphériques de référence.

-   D3DCREATE \_ logiciel \_ VERTEXPROCESSING
-   \_Matériel D3DCREATE \_ VERTEXPROCESSING
-   D3DCREATE \_ mixte \_ VERTEXPROCESSING

Spécifiez l’un des indicateurs de comportement de traitement des vertex lors de l’appel de [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice). L’indicateur en mode mixte permet à l’appareil d’effectuer le traitement des vertex logiciels et matériels. Un seul indicateur de traitement de vertex peut être défini pour un appareil à un moment donné. Notez que l' \_ indicateur VERTEXPROCESSING Hardware D3DCREATE doit \_ être défini lors de la création d’un appareil pur (D3DCREATE \_ PUREDEVICE).

Pour éviter les capacités de traitement double des vertex sur un seul appareil, seules les capacités de traitement du vertex matériel peuvent être interrogées au moment de l’exécution. Les fonctionnalités de traitement des vertex logiciels sont fixes et ne peuvent pas être interrogées au moment de l’exécution.

Le membre VertexProcessingCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) détermine les capacités de traitement du vertex matériel de l’appareil.

Pour le traitement des vertex logiciels, les fonctionnalités suivantes sont prises en charge.

-   membre D3DVTXPCAPS \_ DIRECTIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membre D3DVTXPCAPS \_ LOCALVIEWER de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membre D3DVTXPCAPS \_ MATERIALSOURCE7 de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membre D3DVTXPCAPS \_ POSITIONALLIGHTS de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   membre D3DVTXPCAPS \_ TEXGEN de [D3DVTXPCAPS](d3dvtxpcaps.md)
-   \_membre d’interpolation D3DVTXPCAPS de [D3DVTXPCAPS](d3dvtxpcaps.md)

En outre, le tableau suivant répertorie les valeurs qui sont définies pour les membres de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) pour un appareil en mode de traitement de vertex logiciel.



| Membre                 | Fonctionnalités de traitement des vertex logiciels |
|------------------------|-----------------------------------------|
| MaxActiveLights        | Illimité                               |
| MaxUserClipPlanes      | 6                                       |
| MaxVertexBlendMatrices | 4                                       |
| MaxStreams             | 16                                      |
| MaxVertexIndex         | Égale                              |



 

En général, toute application qui est liée au traitement des vertex doit utiliser un appareil HAL. Le traitement des vertex logiciels fournit un ensemble garanti de fonctionnalités de traitement des vertex, y compris un nombre illimité d’éclairages et une prise en charge complète des nuanceurs de vertex programmables. Vous pouvez basculer entre le traitement des vertex logiciels et matériels à tout moment lors de l’utilisation de l’appareil HAL (qui est le seul type d’appareil prenant en charge le traitement du vertex matériel et logiciel). La seule exigence est que les mémoires tampons de vertex utilisées pour le traitement du vertex logiciel doivent être allouées dans la mémoire système.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
