---
description: En savoir plus sur une combinaison d’un ou plusieurs indicateurs qui contrôlent le comportement de création de l’appareil dans la constante D3DVTXPCAPS.
ms.assetid: 2d3e548f-8559-4a36-b814-6d598bead1d0
title: D3DVTXPCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b544f3e4a69de23607366832aca110e42c61d6d
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011082"
---
# <a name="d3dvtxpcaps"></a>D3DVTXPCAPS

Combinaison d’un ou de plusieurs indicateurs qui contrôlent le comportement de création de l’appareil.



| \#définition                                | Description                                                                                                                                                                                        |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DVTXPCAPS \_ DIRECTIONALLIGHTS          | L’appareil peut faire des lumières directionnelles.                                                                                                                                                                  |
| D3DVTXPCAPS \_ LOCALVIEWER                | L’appareil peut effectuer une visionneuse locale.                                                                                                                                                                        |
| D3DVTXPCAPS \_ MATERIALSOURCE7            | Lorsque cette limite est définie, l’appareil prend en charge les États de couleur : D3DRS \_ AMBIENTMATERIALSOURCE, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ EMISSIVEMATERIALSOURCE et D3DRS SPECULARMATERIALSOURCE \_ . |
| D3DVTXPCAPS \_ non \_ TEXGEN \_ NONLOCALVIEWER | L’appareil ne prend pas en charge la génération de texture en mode visionneuse non locale.                                                                                                                               |
| D3DVTXPCAPS \_ POSITIONALLIGHTS           | L’appareil peut effectuer des lumières de position (y compris un point et un point).                                                                                                                                         |
| D3DVTXPCAPS \_ TEXGEN                     | L’appareil peut effectuer des texgen.                                                                                                                                                                              |
| D3DVTXPCAPS \_ TEXGEN \_ SPHEREMAP          | L’appareil prend en charge D3DTSS \_ TCI \_ SPHEREMAP.                                                                                                                                                            |
| \_Interpolation D3DVTXPCAPS                   | L’appareil peut effectuer l’interpolation des sommets.                                                                                                                                                                     |



 

## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



