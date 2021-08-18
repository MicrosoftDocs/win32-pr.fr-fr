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
ms.openlocfilehash: 30f7ce32e66a19984ce43737d9fc9cae83652c851174d7db350ca34628a33033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850822"
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

 

 




