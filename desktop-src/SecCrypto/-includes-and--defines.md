---
description: Tous les exemples de la documentation du kit de développement logiciel (SDK) Cryptography sont supposés avoir les \# directives de compilateur include et \# define suivantes.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#comprend et #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dbab2a3c33b510df99c9d2e0fa292af53c96fcc471dfe8180d9d4be06b3a5b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117774274"
---
# <a name="includes-and-defines"></a>\#comprend et \# définit

Tous les exemples de la documentation du kit de développement logiciel (SDK) Cryptography sont supposés avoir les directives de compilateur **\# include** et **\# define** suivantes.


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



En outre, la constante **\_ Win32 \_ winnt** doit être définie de manière appropriée. pour plus d’informations sur **\_ WIN32 \_ winnt**, consultez [utilisation des en-têtes de Windows](../winprog/using-the-windows-headers.md).

 

 
