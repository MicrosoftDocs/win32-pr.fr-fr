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
ms.openlocfilehash: ed402b34bdb8ba8caed8dc7cd5b66126d242c9ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941143"
---
# <a name="shader-model-2"></a>Nuancier, modèle 2

Le modèle de nuanceur 2 a ajouté des fonctionnalités supplémentaires au [nuanceur modèle 1](dx-graphics-hlsl-sm1.md).





|--------|-------| | Fonctionnalité | Fonctionnalité | | Jeu d’instructions | <ul><li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Fonctions HLSL</strong></a></li><li>Instructions d’assembly (voir <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">instructions-vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">instructions-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">instructions ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x instructions</a>)</li></ul> | | Ensemble de registres | <ul><li>Registres de nuanceur de pixels (voir registres <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">ps_2_0</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x registres</a>)</li><li>Registres de nuanceur vertex (voir <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">registres-vs_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registres-vs_2_x</a>)</li></ul> | | Nombre maximal de nuanceurs de pixels | <ul><li>ps_2_0-32 texture + 64 arithmétique</li><li>ps_2_x-96 minimum, et jusqu’au nombre d’emplacements dans D3DCAPS9. D3DPSHADERCAPS2_0. NumInstructionSlots. Voir D3DPSHADERCAPS2_0</li></ul> | | Vertex shader Max | 256 instructions | | Profils de nuanceur | ps_2_0, ps_2_x, vs_2_0, vs_2_x | 




 

Pour plus d’informations sur le nuancier Model 2, consultez :

-   [Nuanceur de pixels 2,0](dx9-graphics-reference-asm-ps-2-0.md), [nuanceur de pixels 2. x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Vertex shader 2,0](dx9-graphics-reference-asm-vs-2-0.md), [vertex shader 2. x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles de nuanceur et profils Shader](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




