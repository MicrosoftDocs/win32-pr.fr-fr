---
title: Attribut max_is
description: Vous pouvez spécifier les limites valides des numéros d’index d’un tableau à l’aide de l’attribut \ Max \_ is \.
ms.assetid: b629e3cf-544d-47ee-8f8f-b049f693897c
keywords:
- max_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7adb93aa5e01cd29c724ed61e6d5c9d56eb4c0ab4acf7d09d1cd7f919a80a030
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127629"
---
# <a name="the-max_is-attribute"></a>L' \[ \_ attribut Max is \]

Vous pouvez spécifier les limites valides des numéros d’index d’un tableau à l’aide de l' \[ attribut [**Max \_ is**](/windows/desktop/Midl/max-is) \] .

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(5.0)
]
interface arraytest
{
  void fArray5([in] short sMax,
               [in, out, max_is(sMax)]  char achArray[]);
}
```

 

 