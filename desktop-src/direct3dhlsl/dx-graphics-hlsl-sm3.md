---
title: Modèle de nuanceur 3
description: Le modèle de nuanceur 3 a ajouté des fonctionnalités supplémentaires au nuanceur modèle 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104383048"
---
# <a name="shader-model-3-hlsl-reference"></a>Shader Model 3 (référence HLSL)

Le modèle de nuanceur 3 a ajouté des fonctionnalités supplémentaires au [nuanceur modèle 2](dx-graphics-hlsl-sm2.md).



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
<li>Instructions d’assembly (voir instructions <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">ps_3_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">instructions-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ensemble de registres</td>
<td><ul>
<li>Registres de nuanceur de pixels (voir <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">registres ps_3_0</a>)</li>
<li>Registres de nuanceur vertex (voir <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">Registers-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Nuanceur de pixels max.</td>
<td>512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxPixelShader30InstructionSlots (voir <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Vertex shader Max</td>
<td>512 minimum et jusqu’au nombre d’emplacements dans D3DCAPS9. MaxVertexShader30InstructionSlots (voir <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</td>
</tr>
<tr class="even">
<td>Profils de nuanceur</td>
<td>ps_3_0, vs_3_0</td>
</tr>
</tbody>
</table>



 

Pour plus d’informations sur les nuanceurs de modèle 3, consultez :

-   [Nuanceur de pixels 3,0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Vertex Shader 3,0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de nuanceur et profils Shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 