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
# <a name="in-out-string-prototype"></a><span data-ttu-id="1d573-103">\[in, out, prototype de chaîne \]</span><span class="sxs-lookup"><span data-stu-id="1d573-103">\[in, out, string\] Prototype</span></span>

<span data-ttu-id="1d573-104">Le prototype de fonction suivant utilise un \[ paramètre de [**chaîne**](/windows/desktop/Midl/string) [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl)unique \] pour les chaînes d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="1d573-104">The following function prototype uses a single \[[**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl), [**string**](/windows/desktop/Midl/string)\] parameter for both the input and output strings.</span></span> <span data-ttu-id="1d573-105">La chaîne contient tout d’abord l’entrée du patient et est ensuite remplacée par la réponse du médecin, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="1d573-105">The string first contains patient input and is then overwritten with the doctor response as shown:</span></span>

``` syntax
void Analyze([in, out, string, size_is(STRSIZE)] char  achInOut[]);
```

<span data-ttu-id="1d573-106">Cet exemple est similaire à celui qui a utilisé une chaîne à comptage unique pour l’entrée et la sortie.</span><span class="sxs-lookup"><span data-stu-id="1d573-106">This example is similar to the one that employed a single-counted string for both input and output.</span></span> <span data-ttu-id="1d573-107">Comme avec cet exemple, la \[ [**taille \_ est**](/windows/desktop/Midl/size-is) l' \] attribut qui détermine le nombre d’éléments alloués sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="1d573-107">As with that example, the \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute determines the number of elements allocated on the server.</span></span> <span data-ttu-id="1d573-108">L' \[ attribut de [**chaîne**](/windows/desktop/Midl/string) \] indique au stub d’appeler **strlen** pour déterminer le nombre d’éléments transmis.</span><span class="sxs-lookup"><span data-stu-id="1d573-108">The \[[**string**](/windows/desktop/Midl/string)\] attribute directs the stub to call **strlen** to determine the number of transmitted elements.</span></span>

<span data-ttu-id="1d573-109">Le client alloue toute la mémoire avant l’appel en tant que :</span><span class="sxs-lookup"><span data-stu-id="1d573-109">The client allocates all memory before the call as:</span></span>

``` syntax
/* client */
char achInOut[STRSIZE];
...
gets_s(achInOut, STRSIZE);            // get patient input
Analyze(achInOut);
printf("%s\n", achInOut);  // display doctor response
```

<span data-ttu-id="1d573-110">Notez que la fonction Analyze ne doit plus calculer la longueur de la chaîne de retour comme dans l’exemple compté de chaîne où l’attribut de **\[ chaîne \]** n’a pas été utilisé.</span><span class="sxs-lookup"><span data-stu-id="1d573-110">Note that the Analyze function no longer must calculate the length of the return string as it did in the counted-string example where the **\[string\]** attribute was not used.</span></span> <span data-ttu-id="1d573-111">À présent, les stubs calculent la longueur comme indiqué :</span><span class="sxs-lookup"><span data-stu-id="1d573-111">Now the stubs calculate the length as shown:</span></span>

``` syntax
/* server */
void Analyze(char *pchInOut)
{
   ...
   Respond(response, pchInOut); // don't need to call strlen
   return;                      // stubs handle size
}
```

 

 