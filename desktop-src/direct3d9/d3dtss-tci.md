---
description: Indicateurs de capacité de la texture du pilote.
ms.assetid: b15509b4-7db1-429a-9468-be7a11dee505
title: D3DTSS_TCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4973e045decd393be2f8a6d340f369761a411a44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950811"
---
# <a name="d3dtss_tci"></a>D3DTSS \_ TCI

Indicateurs de capacité de la texture du pilote.



|                                          |             |                                                                                                                                                                                                                      |
|------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#définition                                 | Valeur       | Description                                                                                                                                                                                                          |
| D3DTSS \_ TCI \_                    | 0x00000000L | Utilise les coordonnées de texture spécifiées contenues dans le format de vertex. Cette valeur est résolue à zéro.                                                                                                               |
| D3DTSS \_ TCI \_ CAMERASPACENORMAL           | 0x00010000L | Utilisez la normale du vertex, transformée en espace de caméra, comme coordonnées de texture d’entrée pour la transformation de texture de cette étape.                                                                                        |
| D3DTSS \_ TCI \_ CAMERASPACEPOSITION         | 0x00020000L | Utilisez la position du vertex, transformée en espace de caméra, comme coordonnées de texture d’entrée pour la transformation de texture de cette étape.                                                                                      |
| D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR | 0x00030000L | Utilisez le vecteur de réflexion, transformé en espace de caméra, comme coordonnée de texture d’entrée pour la transformation de texture de cette étape. Le vecteur de réflexion est calculé à partir de la position du vertex d’entrée et du vecteur normal. |
| D3DTSS \_ TCI \_ SPHEREMAP                   | 0x00040000L | Utilisez les coordonnées de texture spécifiées pour le mappage de sphère.                                                                                                                                                            |



 

Ces constantes sont utilisées par D3DTSS \_ TEXCOORDINDEX.

## <a name="constant-information"></a>Informations constantes



|                          |            |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



