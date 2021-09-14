---
title: " in, String et out, prototype de chaîne"
description: Le prototype de fonction suivant utilise deux paramètres, un paramètre \ in, String \ et un paramètre \ out, String \.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416634"
---
# <a name="in-string-and-out-string-prototype"></a>\[in, String \] et \[ out, prototype de chaîne \]

Le prototype de fonction suivant utilise deux paramètres : un \[ [**dans**](/windows/desktop/Midl/in)un paramètre de [**chaîne**](/windows/desktop/Midl/string) \] et un \[ paramètre de **chaîne** [**out**](/windows/desktop/Midl/out-idl) \] .

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

Le premier paramètre est \[ [**dans**](/windows/desktop/Midl/in) \] uniquement. Cette chaîne d’entrée est uniquement transmise à partir du client vers le serveur. Le serveur l’utilise comme base pour un traitement ultérieur. La chaîne n’est pas modifiée et n’est pas requise à nouveau par le client, il n’est donc pas nécessaire de la retourner au client.

Le deuxième paramètre, représentant la réponse du médecin, est \[ uniquement [**sortant**](/windows/desktop/Midl/out-idl) \] . Cette chaîne de réponse est uniquement transmise du serveur au client. La taille d’allocation est fournie afin que les stubs de serveur puissent allouer de la mémoire à celle-ci. Étant donné que *pszOutput* est un \[ pointeur [**ref**](/windows/desktop/Midl/ref) \] , le client doit disposer de suffisamment de mémoire allouée pour la chaîne avant l’appel. La chaîne de réponse est écrite dans cette zone de mémoire lorsque la procédure distante retourne.

 

 