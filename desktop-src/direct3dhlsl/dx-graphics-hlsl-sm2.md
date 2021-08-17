---
title: Nuancier, modèle 2
description: Le modèle de nuanceur 2 a ajouté des fonctionnalités supplémentaires au nuanceur modèle 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23b4caa0e4da92e992eb0486f5a998ad7d21016dc691563f29589c5fc9ab5310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119973"
---
# <a name="shader-model-2"></a>Nuancier, modèle 2

Le modèle de nuanceur 2 a ajouté des fonctionnalités supplémentaires au [nuanceur modèle 1](dx-graphics-hlsl-sm1.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Fonctionnalité</td>
<td>Utilité</td>
</tr>
<tr class="even">
<td>Jeu d'instructions</td>
<td><ul>
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Fonctions HLSL</strong></a></li>
<li>Instructions d’assembly (voir <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">instructions-vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">instructions-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">instructions ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x instructions</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ensemble de registres</td>
<td><ul>
<li>Registres de nuanceur de pixels (voir registres <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x registres</a>)</li>
<li>Registres de nuanceur vertex (voir <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">registres-vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registres-vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Nuanceur de pixels max.</td>
<td><ul>
<li>ps_2_0-32 texture + 64 arithmétique</li>
<li>ps_2_x-96 minimum, et jusqu’au nombre d’emplacements dans D3DCAPS9. D3DPSHADERCAPS2_0. NumInstructionSlots. Voir D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vertex shader Max</td>
<td>instructions 256</td>
</tr>
<tr class="even">
<td>Profils de nuanceur</td>
<td>ps_2_0, ps_2_x, vs_2_0, vs_2_x</td>
</tr>
</tbody>
</table>



 

Pour plus d’informations sur le nuancier Model 2, consultez :

-   [Nuanceur de pixels 2,0](dx9-graphics-reference-asm-ps-2-0.md), [nuanceur de pixels 2. x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Vertex shader 2,0](dx9-graphics-reference-asm-vs-2-0.md), [vertex shader 2. x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de nuanceur et profils Shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




