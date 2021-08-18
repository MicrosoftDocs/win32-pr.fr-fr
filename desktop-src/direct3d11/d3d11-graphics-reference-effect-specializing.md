---
title: Spécialisation des interfaces (Direct3D 11)
description: ID3DX11EffectVariable dispose d’un certain nombre de méthodes pour effectuer un cast de l’interface dans le type d’interface particulier dont vous avez besoin.
ms.assetid: 20892af0-7d4a-4a89-b8d7-4ef225400697
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cff9c74f7a4b4034578b7ddeec2c388f0f953534393ac27778c31ed3856c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126073"
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

 

 




