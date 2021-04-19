---
description: L’interface ID3D10EffectVariable dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.
ms.assetid: c0842a1d-b78c-44b2-89c7-452d54efe403
title: Spécialisation des interfaces (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ce8bc29ae16ada650da7283beb1dd858948cae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514941"
---
# <a name="specializing-interfaces-direct3d-10"></a>Spécialisation des interfaces (Direct3D 10)

L' [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin. Les méthodes se présentent sous la forme *type* et incluent une méthode pour chaque type de variable d’effet (tel que AsBlend, AsConstantBuffer, etc.).

Par exemple, supposons que vous ayez un effet avec deux variables globales : Time et une transformation universelle.


```
float    g_fTime;
float4x4 g_mWorld;
```



Voici un exemple (à partir de l' [exemple SimpleSample10](https://msdn.microsoft.com/library/Ee416428(v=VS.85).aspx)) qui obtient ces variables :


```
ID3D10EffectVariable* g_pVariable;
ID3D10EffectMatrixVariable* g_pmWorld;
ID3D10EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect10->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pfTime = g_pEffect10->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



En spécialisant les interfaces, vous pouvez réduire le code à un seul appel.


```
g_pmWorld = (g_pEffect10->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect10->GetVariableByName("g_fTime"))->AsScalar();
```



Les interfaces qui héritent de l' [**interface ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable) ont également ces méthodes, mais elles ont été conçues pour retourner des objets non valides ; Seuls les appels de l' **interface ID3D10EffectVariable** retournent des objets valides. Les applications peuvent tester l’objet retourné pour voir s’il est valide en appelant [**ID3D10EffectVariable :: IsValid**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectvariable-isvalid).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



