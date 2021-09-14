---
description: Répertorie les handles utilisés par l’API SSPI.
ms.assetid: 94b622d0-7c04-4513-841f-0df9b5d49136
title: Handles SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e388633cfee0d0f0470e519bac124a0bd1c70fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127096369"
---
# <a name="sspi-handles"></a>Handles SSPI

SSPI utilise les types de handles suivants et le pointeur vers ces handles :

-   **SecHandle** et **PSecHandle**
-   **CredHandle** et **PCredHandle**
-   **CtxtHandle** et **PCtxtHandle**

Ces types de handle et les pointeurs vers ces types de descripteurs sont définis comme suit.


```C++
typedef struct _SecHandle {
  ULONG_PTR       dwLower;
  ULONG_PTR       dwUpper;
} SecHandle, * PSecHandle;

typedef SecHandle    CredHandle;
typedef PSecHandle   PCredHandle;

typedef SecHandle    CtxtHandle;
typedef PSecHandle   PCtxtHandle;
```



 

 



