---
title: Types simples
description: Tous les types simples sont représentés par un caractère de format unique qui indique le type par son nom.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e265c24d1eaf4b85ab67c7f8997c656257522bfc8290e73596a8628bdd4215c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925159"
---
# <a name="simple-types"></a>Types simples

Tous les types simples sont représentés par un caractère de format unique qui indique le type par son nom. Cela comprend tous les types numériques et d’autres types d’IDL spéciaux. La liste est la suivante :

``` syntax
FC_BYTE,                    // 0x01
FC_CHAR,                    // 0x02
FC_SMALL,                   // 0x03
FC_USMALL,                  // 0x04
FC_WCHAR,                   // 0x05
FC_SHORT,                   // 0x06
FC_USHORT,                  // 0x07
FC_LONG,                    // 0x08
FC_ULONG,                   // 0x09
FC_FLOAT,                   // 0x0a
FC_HYPER,                   // 0x0b
FC_DOUBLE,                  // 0x0c
FC_ENUM16,                  // 0x0d
FC_ENUM32,                  // 0x0e
FC_ERROR_STATUS_T,          // 0x10
FC_INT3264,                 // 0xb8
FC_UINT3264,                // 0xb9
```

Les types INT3264 de petite, WCHAR, HYPER, ERROR \_ Status \_ \_ \_ sont des intrinsèques MIDL avec des interprétations RPC spéciales. Les types INT et \_ \_ Int32 sont mappés à FC \_ long, unsigned int et unsigned \_ \_ Int32 Map to FC \_ ULong, \_ \_ Int64 et unsigned \_ \_ Int64 Map to FC \_ hyper.

Les \_ \_ types INT128, FLOAT128 et FLOAT80 ne sont pas pris en charge.

 

 




