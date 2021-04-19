---
description: Un effet est créé en le chargeant dans le Framework Effects.
ms.assetid: b0a12620-4f8f-44d9-bc73-2c3ab30f80af
title: Créer un effet (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b630bae35b8e1390a4be77e5cb5e4aaa3f41d9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514107"
---
# <a name="create-an-effect-direct3d-10"></a>Créer un effet (Direct3D 10)

Un effet est créé en le chargeant dans le Framework Effects. Si l’effet n’a jamais été compilé, il sera compilé lors de sa création. Les effets déjà chargés en mémoire peuvent être créés en appelant [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md). L’exemple de code suivant utilise [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md) pour créer un effet à partir d’un fichier.


```
ID3D10Effect* g_pEffect10 = NULL; 

// Read the effect file 
D3DX10CreateEffectFromFile( "BasicHLSL10.fx", NULL, NULL,
  D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
  &g_pEffect10, NULL );
```



La lecture d’un effet requiert les mêmes paramètres que la compilation d’un effet, ainsi qu’un appareil et un pool.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un effet (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



