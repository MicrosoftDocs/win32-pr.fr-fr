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
# <a name="includes-and-defines"></a><span data-ttu-id="75346-103">\#comprend et \# définit</span><span class="sxs-lookup"><span data-stu-id="75346-103">\#includes and \#defines</span></span>

<span data-ttu-id="75346-104">Tous les exemples de la documentation du kit de développement logiciel (SDK) Cryptography sont supposés avoir les directives de compilateur **\# include** et **\# define** suivantes.</span><span class="sxs-lookup"><span data-stu-id="75346-104">All of the examples in the Cryptography SDK documentation are assumed to have the following **\#include** and **\#define** compiler directives.</span></span>


```C++
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
```



<span data-ttu-id="75346-105">En outre, la constante **\_ Win32 \_ winnt** doit être définie de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="75346-105">Additionally, the **\_WIN32\_WINNT** constant must be appropriately defined.</span></span> <span data-ttu-id="75346-106">Pour plus d’informations sur **\_ Win32 \_ winnt**, consultez [utilisation des en-têtes Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="75346-106">For more information about **\_WIN32\_WINNT**, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

 

 
