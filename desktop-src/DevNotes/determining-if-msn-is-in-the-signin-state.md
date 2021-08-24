---
description: L’exemple de code suivant illustre l’utilisation d’un objet mutex pour déterminer si MSN Explorer est connecté.
ms.assetid: ec52a61c-9d2c-4327-977b-fb13d042bc37
title: Détermination de l’état de connexion de MSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da0abffc1735d2bf7af6ee6f9a68bf0d71ca1a2fda44176a0905c3e8faec6d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654190"
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



 

 
