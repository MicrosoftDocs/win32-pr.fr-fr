---
description: L’exemple de code suivant illustre l’utilisation d’un objet mutex pour déterminer si MSN Explorer est connecté.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Détermination de l’état de connexion de MSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d7af3511035c997493f0439a8635c1a928a75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523959"
---
# <a name="determining-if-msn-is-in-the-sign-in-state"></a>Détermination de l’état de connexion de MSN

L’exemple de code suivant illustre l’utilisation d’un objet mutex pour déterminer si MSN Explorer est connecté. Lorsque vous avez fini d’utiliser le descripteur, veillez à appeler la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) .

> [!Note]  
> Cet objet mutex peut être utilisé pour la vérification de MSN Explorer 7. État de la connexion *x* . Elle n’est peut-être pas disponible dans les versions ultérieures.

 


```C++
    HANDLE hMSNSignedInMutex;

    hMSNSignedInMutex = OpenMutex(SYNCHRONIZE, FALSE, 
        "{ECCC50B5-064B-4693-B104-925714A4C74B}");

    if (hMSNSignedInMutex != NULL)
    {
        // MSN Explorer is signed in
    }
```



 

 
