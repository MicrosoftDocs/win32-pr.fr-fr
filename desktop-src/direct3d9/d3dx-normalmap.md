---
description: Constantes de génération de mappages normales.
ms.assetid: edf4c3e4-1af4-43b4-80c7-6fab02575f7b
title: D3DX_NORMALMAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4263237cedf92a5e322f2fe139e9afe2297f6b9b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342854"
---
# <a name="d3dx_normalmap"></a>D3DX \_ NORMALMAP

Constantes de génération de mappages normales.



| \#définition                            | Description                                                                                                                                                                                        |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_NORMALMAP \_ en miroir \_ D3DX          | Indique que les pixels du bord de la texture sur l’axe des u doivent être mis en miroir, et non encapsulés.                                                                                                   |
| \_Miroir D3DX \_ NORMALMAP \_ V          | Indique que les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.                                                                                                   |
| \_Miroir D3DX NORMALMAP \_             | Identique à la spécification de la mise en miroir de D3DX \_ NORMALMAP \_ MIRROR \_ U \| D3DX \_ NORMALMAP \_ \_ .                                                                                                                       |
| D3DX \_ NORMALMAP \_ INVERTSIGN         | Inverse la direction de chaque normal.                                                                                                                                                              |
| D3DX \_ NORMALMAP \_ calcul \_ occlusion | Calcule le terme d’occlusion par pixel et l’encode en alpha. Une valeur alpha de 1 signifie que le pixel n’est pas masqué, et une valeur alpha de 0 signifie que le pixel est complètement masqué. |



 

## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur           |
|--------------------------|------------|
| En-tête                   | d3dx9tex. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> <dt>

[**D3DXComputeNormalMap**](d3dxcomputenormalmap.md)
</dt> </dl>

 

 



