---
description: Tous les exemples de la documentation du kit de développement logiciel (SDK) Cryptography sont supposés avoir les \# directives de compilateur include et \# define suivantes.
ms.assetid: 98f85e7d-e557-4dde-b510-891b37daec87
title: '#comprend et #defines'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9834fd8103b9fd28a01e416bd1df8b03fb7ad680
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535108"
---
# <a name="includes-and-defines"></a>\#comprend et \# définit

Tous les exemples de la documentation du kit de développement logiciel (SDK) Cryptography sont supposés avoir les directives de compilateur **\# include** et **\# define** suivantes.


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



En outre, la constante **\_ Win32 \_ winnt** doit être définie de manière appropriée. Pour plus d’informations sur **\_ Win32 \_ winnt**, consultez [utilisation des en-têtes Windows](../winprog/using-the-windows-headers.md).

 

 
