---
description: Nuanceur qui est appelé quand aucune intersection de rayon n’est trouvée ou acceptée.
ms.assetid: ''
title: Nuanceur manque
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: fe8e2ec9cdbb8ef7567b9327ae5af1128597a601
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514550"
---
# <a name="miss-shader"></a>Nuanceur manque

Nuanceur qui est appelé quand aucune intersection de rayon n’est trouvée ou acceptée. Cela est utile pour l’ombrage de l’arrière-plan ou du ciel.  Le nuanceur d’échecs peut utiliser [**CallShader**](callshader-function.md) et **TraceRay** pour planifier davantage de travail.

Le nuanceur d’échecs doit inclure un paramètre de charge utile typée de structure définie par l’utilisateur correspondant à celui fourni à [**TraceRay**](traceray-function.md).


## <a name="shader-type-attribute"></a>Attribut de type Shader


```
[shader("miss")]
```



## <a name="example"></a>Exemple

```
[shader("anyhit")]
void miss_main(inout MyPayload payload)
{
    // Use ray system values to compute contributions of background, sky, etc...
    // Combine contributions into ray payload
    CallShader( ... );  // if desired
    TraceRay( ... );    // if desired
    // this ray query is now complete
}

```

 

 




