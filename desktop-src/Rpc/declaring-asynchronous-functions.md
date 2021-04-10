---
title: Déclaration de fonctions asynchrones
description: Pour déclarer une fonction RPC comme asynchrone, commencez par déclarer la fonction dans le cadre d’une définition d’interface dans un fichier IDL (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Appel de procédure distante RPC, tâches, déclaration de fonctions asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103941439"
---
# <a name="declaring-asynchronous-functions"></a>Déclaration de fonctions asynchrones

Pour déclarer une fonction RPC comme asynchrone, commencez par déclarer la fonction dans le cadre d’une définition d’interface dans un fichier IDL (Interface Definition Language). L’utilisation de fonctions RPC asynchrones ne nécessite aucune modification spéciale de votre fichier IDL. L’exemple suivant montre un fichier IDL pour une application qui utilise une fonction asynchrone.

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

Pour toutes les fonctions RPC asynchrones utilisées par votre application, vous devez modifier la déclaration des fonctions asynchrones dans le fichier ACF de votre application. Appliquez l’attribut [**\[ Async \]**](../midl/async.md) à chaque nom de fonction asynchrone, comme indiqué dans l’exemple suivant :

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

Quand vous appliquez l’attribut **\[ Async \]** dans le fichier ACF, le compilateur MIDL génère automatiquement un paramètre de handle asynchrone supplémentaire dans le code stub.

 

 