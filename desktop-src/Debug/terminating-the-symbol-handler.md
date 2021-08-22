---
description: Le code suivant nettoie toute la mémoire associée à la gestion des symboles pour le processus spécifié, à l’aide de SymCleanup.
ms.assetid: 270a1984-9e66-4dd2-accb-d715287f1ec0
title: Arrêt du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af49c26ffe1a80fad3bf7b03fc18699c07e9b025e8b07b5f6bb6c377cde743b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956938"
---
# <a name="terminating-the-symbol-handler"></a>Arrêt du gestionnaire de symboles

Le code suivant nettoie toute la mémoire associée à la gestion des symboles pour le processus spécifié, à l’aide de [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup).


```C++
if (SymCleanup(hProcess))
{
    // SymCleanup returned success
}
else
{
    // SymCleanup failed
    DWORD error = GetLastError();
    printf("SymCleanup returned error : %d\n", error);
}
```



 

 



