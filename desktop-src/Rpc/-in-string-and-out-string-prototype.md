---
title: " in, String et out, prototype de chaîne"
description: Le prototype de fonction suivant utilise deux paramètres, un paramètre \ in, String \ et un paramètre \ out, String \.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941306"
---
# <a name="in-string-and-out-string-prototype"></a><span data-ttu-id="3823a-103">\[in, String \] et \[ out, prototype de chaîne \]</span><span class="sxs-lookup"><span data-stu-id="3823a-103">\[in, string\] and \[out, string\] Prototype</span></span>

<span data-ttu-id="3823a-104">Le prototype de fonction suivant utilise deux paramètres : un \[ [**dans**](/windows/desktop/Midl/in)un paramètre de [**chaîne**](/windows/desktop/Midl/string) \] et un \[ paramètre de **chaîne** [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="3823a-104">The following function prototype uses two parameters: an \[[**in**](/windows/desktop/Midl/in), [**string**](/windows/desktop/Midl/string)\] parameter and an \[[**out**](/windows/desktop/Midl/out-idl), **string**\] parameter.</span></span>

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

<span data-ttu-id="3823a-105">Le premier paramètre est \[ [**dans**](/windows/desktop/Midl/in) \] uniquement.</span><span class="sxs-lookup"><span data-stu-id="3823a-105">The first parameter is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="3823a-106">Cette chaîne d’entrée est uniquement transmise à partir du client vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="3823a-106">This input string is only transmitted from the client to the server.</span></span> <span data-ttu-id="3823a-107">Le serveur l’utilise comme base pour un traitement ultérieur.</span><span class="sxs-lookup"><span data-stu-id="3823a-107">The server uses it as the basis for further processing.</span></span> <span data-ttu-id="3823a-108">La chaîne n’est pas modifiée et n’est pas requise à nouveau par le client, il n’est donc pas nécessaire de la retourner au client.</span><span class="sxs-lookup"><span data-stu-id="3823a-108">The string is not modified and is not required again by the client, so it does not have to be returned to the client.</span></span>

<span data-ttu-id="3823a-109">Le deuxième paramètre, représentant la réponse du médecin, est \[ uniquement [**sortant**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="3823a-109">The second parameter, representing the doctor's response, is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="3823a-110">Cette chaîne de réponse est uniquement transmise du serveur au client.</span><span class="sxs-lookup"><span data-stu-id="3823a-110">This response string is only transmitted from the server to the client.</span></span> <span data-ttu-id="3823a-111">La taille d’allocation est fournie afin que les stubs de serveur puissent allouer de la mémoire à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="3823a-111">The allocation size is provided so that the server stubs can allocate memory for it.</span></span> <span data-ttu-id="3823a-112">Étant donné que *pszOutput* est un \[ pointeur [**ref**](/windows/desktop/Midl/ref) \] , le client doit disposer de suffisamment de mémoire allouée pour la chaîne avant l’appel.</span><span class="sxs-lookup"><span data-stu-id="3823a-112">Since *pszOutput* is a \[[**ref**](/windows/desktop/Midl/ref)\] pointer, the client must have sufficient memory allocated for the string before the call.</span></span> <span data-ttu-id="3823a-113">La chaîne de réponse est écrite dans cette zone de mémoire lorsque la procédure distante retourne.</span><span class="sxs-lookup"><span data-stu-id="3823a-113">The response string is written into this area of memory when the remote procedure returns.</span></span>

 

 