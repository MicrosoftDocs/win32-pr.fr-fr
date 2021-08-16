---
description: L’exemple de code d’assembly x86 suivant obtient l’ID de session des services Terminal Server associé au processus en cours.
ms.assetid: 9fcb35cb-6813-46a5-aa38-e102f1b6b7dc
title: Obtention de l’ID de session du processus en cours
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4326020f145c98544132703611fbd783edac9ae9eb89a5c69f44b67dc997ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955978"
---
# <a name="getting-the-session-id-of-the-current-process"></a>Obtention de l’ID de session du processus en cours

\[Les adresses mémoire spécifiées par cet exemple de code peuvent changer dans les versions ultérieures de Windows. Pour vous assurer que votre application continuera à s’exécuter correctement à l’avenir, votre application doit appeler [**GetCurrentProcessId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessid) , puis [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) au lieu de l’exemple de code suivant.\]

L’exemple de code d’assembly x86 suivant obtient l’ID de session des services Terminal Server associé au processus en cours.

``` syntax
mov     eax,fs:[00000018]
mov     eax,[eax+0x30]
mov     eax,[eax+0x1d4]
```

 

 
