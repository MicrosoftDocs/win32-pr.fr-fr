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
# <a name="declaring-asynchronous-functions"></a><span data-ttu-id="3f94c-104">Déclaration de fonctions asynchrones</span><span class="sxs-lookup"><span data-stu-id="3f94c-104">Declaring Asynchronous Functions</span></span>

<span data-ttu-id="3f94c-105">Pour déclarer une fonction RPC comme asynchrone, commencez par déclarer la fonction dans le cadre d’une définition d’interface dans un fichier IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="3f94c-105">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an Interface Definition Language (IDL) file.</span></span> <span data-ttu-id="3f94c-106">L’utilisation de fonctions RPC asynchrones ne nécessite aucune modification spéciale de votre fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="3f94c-106">The use of asynchronous RPC functions does not require any special alterations to your IDL file.</span></span> <span data-ttu-id="3f94c-107">L’exemple suivant montre un fichier IDL pour une application qui utilise une fonction asynchrone.</span><span class="sxs-lookup"><span data-stu-id="3f94c-107">The following example shows an IDL file for an application that uses one asynchronous function.</span></span>

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

<span data-ttu-id="3f94c-108">Pour toutes les fonctions RPC asynchrones utilisées par votre application, vous devez modifier la déclaration des fonctions asynchrones dans le fichier ACF de votre application.</span><span class="sxs-lookup"><span data-stu-id="3f94c-108">For all asynchronous RPC functions that your application uses, you will need to modify the declaration of the asynchronous functions within your application's ACF file.</span></span> <span data-ttu-id="3f94c-109">Appliquez l’attribut [**\[ Async \]**](../midl/async.md) à chaque nom de fonction asynchrone, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="3f94c-109">Apply the [**\[async\]**](../midl/async.md) attribute to each asynchronous function name, as shown in the following example:</span></span>

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

<span data-ttu-id="3f94c-110">Quand vous appliquez l’attribut **\[ Async \]** dans le fichier ACF, le compilateur MIDL génère automatiquement un paramètre de handle asynchrone supplémentaire dans le code stub.</span><span class="sxs-lookup"><span data-stu-id="3f94c-110">When you apply the **\[async\]** attribute in the ACF file, the MIDL compiler automatically generates an additional asynchronous handle parameter in the stub code.</span></span>

 

 