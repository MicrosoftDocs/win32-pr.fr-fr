---
description: Un nuanceur qui est appelé à partir d’un autre nuanceur avec l’intrinsèque CallShader.
ms.assetid: ''
title: Nuanceur pouvant être appelé
ms.date: 05/31/2018
ms.localizationpriority: low
ms.topic: reference
topic_type:
- APIRef
- kbSyntax
api_name:
- Callable Shader
api_type:
- NA
ms.openlocfilehash: b84ec6ea58fbc456db1747259f687a2fb6c8cb0fe3374b3d32396861dcd2f9b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461069"
---
# <a name="callable-shader"></a>Nuanceur pouvant être appelé

Un nuanceur qui est appelé à partir d’un autre nuanceur avec l’intrinsèque [**CallShader**](callshader-function.md) .

Une structure de paramètre est fournie sur le site d’appel **CallShader** , qui doit correspondre à la structure de paramètre utilisée dans le nuanceur pouvant être appelé, pointée par l’index demandé dans la table de nuanceur pouvant être appelée fournie par la méthode [**DispatchRays**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) .  Le nuanceur pouvant être appelé doit déclarer ce paramètre comme *INOUT*.  En outre, le nuanceur pouvant être appelé peut lire les entrées de la dimension et de l’index de lancement. Pour plus d’informations, consultez [**intrinsèques de valeurs système**](direct3d-12-raytracing-hlsl-system-value-intrinsics.md). 


## <a name="shader-type-attribute"></a>Attribut de type Shader


```
[shader("callable")]
```



## <a name="example"></a>Exemple

```
[shader("callable")]
void callable_main(inout MyParams params)
{
    // Perform some common operations and update params
    CallShader( ... );  // maybe
}

```

 

 




