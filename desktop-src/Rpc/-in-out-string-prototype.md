---
title: " in, out, prototype de chaîne"
description: Le prototype de fonction suivant utilise un paramètre unique \ in, out, String \ pour les chaînes d’entrée et de sortie.
ms.assetid: 5a652b79-11ca-4780-aac1-60a22f96b4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed8ed47c02ea3e08672d529bf7ce9f627925518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941096"
---
# <a name="in-out-string-prototype"></a>\[in, out, prototype de chaîne \]

Le prototype de fonction suivant utilise un \[ paramètre de [**chaîne**](/windows/desktop/Midl/string) [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)unique \] pour les chaînes d’entrée et de sortie. La chaîne contient tout d’abord l’entrée du patient et est ensuite remplacée par la réponse du médecin, comme indiqué ci-dessous :

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

Cet exemple est similaire à celui qui a utilisé une chaîne à comptage unique pour l’entrée et la sortie. Comme avec cet exemple, la \[ [**taille \_ est**](/windows/desktop/Midl/size-is) l' \] attribut qui détermine le nombre d’éléments alloués sur le serveur. L' \[ attribut de [**chaîne**](/windows/desktop/Midl/string) \] indique au stub d’appeler **strlen** pour déterminer le nombre d’éléments transmis.

Le client alloue toute la mémoire avant l’appel en tant que :

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

Notez que la fonction Analyze ne doit plus calculer la longueur de la chaîne de retour comme dans l’exemple compté de chaîne où l’attribut de **\[ chaîne \]** n’a pas été utilisé. À présent, les stubs calculent la longueur comme indiqué :

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 