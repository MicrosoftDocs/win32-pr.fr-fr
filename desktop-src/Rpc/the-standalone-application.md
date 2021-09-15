---
title: Application autonome
description: Cette application autonome, qui se compose d’un appel à une seule fonction, forme la base de notre application distribuée.
ms.assetid: 640f5d01-84c8-4fe8-9dae-f4d55cc6f06b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf1b11df2372a1db5c74659d1800b62e53b7309
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311402"
---
# <a name="the-standalone-application"></a>Application autonome

Cette application autonome, qui se compose d’un appel à une seule fonction, forme la base de notre application distribuée. La fonction, **HelloProc**, est définie dans son propre fichier source afin qu’elle puisse être compilée et liée à une application autonome ou une application distribuée.


```C++
/* file hellop.c */
#include <stdio.h>
#include <windows.h>

void HelloProc(char * pszString)
{
    printf("%s\n", pszString);
}
 
/* file: hello.c, a stand-alone application */
#include "hellop.c"

void main(void)
{
    char * pszString = "Hello, World";
    HelloProc(pszString);
}
```



 

 




