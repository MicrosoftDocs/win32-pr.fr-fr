---
title: Spécialisation des interfaces (Direct3D 11)
description: ID3DX11EffectVariable dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9f8adb5a5bb184473ff5679df99f0b71557fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674246"
---
# <a name="specializing-interfaces-direct3d-11"></a>Spécialisation des interfaces (Direct3D 11)

[**ID3DX11EffectVariable**](id3dx11effectvariable.md) dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin. Les méthodes se présentent sous la forme *AsType* et incluent une méthode pour chaque type de variable d’effet (tel que AsBlend, AsConstantBuffer, etc.).

Par exemple, supposons que vous ayez un effet avec deux variables globales : Time et une transformation universelle.


```
float    g_fTime;
float4x4 g_mWorld;
```



Voici un exemple qui obtient ces variables :


```
ID3DX11EffectVariable* g_pVariable;
ID3DX11EffectMatrixVariable* g_pmWorld;
ID3DX11EffectScalarVariable* g_pfTime;

g_pVariable = g_pEffect11->GetVariableByName("g_mWorld");
g_pmWorld = g_pVariable->AsMatrix();
g_pVariable = g_pEffect11->GetVariableByName("g_fTime");
g_pfTime = g_pVariable->AsScalar();
```



En spécialisant les interfaces, vous pouvez réduire le code à un seul appel.


```
g_pmWorld = (g_pEffect11->GetVariableByName("g_mWorld"))->AsMatrix();
g_pfTime = (g_pEffect11->GetVariableByName("g_fTime"))->AsScalar();
```



Les interfaces qui héritent de [**ID3DX11EffectVariable**](id3dx11effectvariable.md) ont également ces méthodes, mais elles ont été conçues pour retourner des objets non valides ; Seuls les appels de **ID3DX11EffectVariable** retournent des objets valides. Les applications peuvent tester l’objet retourné pour voir s’il est valide en appelant [**ID3DX11EffectVariable :: IsValid**](id3dx11effectvariable-isvalid.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 




