---
title: " in, out, size_is prototype"
description: '\ in, out, size \_ is \ prototype utilise un tableau de caractères à un seul comptage qui est passé du client au serveur et du serveur au client.'
ms.assetid: bce9a36f-9f7c-4438-9b5a-15b8877f74c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37829ce0d5a4bb44fefa038e9ce71773f9c4c9bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315372"
---
# <a name="in-out-size_is-prototype"></a><span data-ttu-id="27867-103">\[in, out, la taille \_ est un \] prototype</span><span class="sxs-lookup"><span data-stu-id="27867-103">\[in, out, size\_is\] Prototype</span></span>

<span data-ttu-id="27867-104">Le prototype de fonction suivant utilise un tableau de caractères à un seul comptage qui reçoit les deux manières : du client au serveur et du serveur au client :</span><span class="sxs-lookup"><span data-stu-id="27867-104">The following function prototype uses a single-counted character array that is passed both ways: from client to server and from server to client:</span></span>

``` syntax
#define STRSIZE 500 //maximum string length

void Analyze(
    [in, out, length_is(*pcbSize), size_is(STRSIZE)] char  achInOut[],
    [in, out]  long *pcbSize);
```

<span data-ttu-id="27867-105">En tant que \[ [](/windows/desktop/Midl/in) \] paramètre in, *achInOut* doit pointer vers un stockage valide côté client.</span><span class="sxs-lookup"><span data-stu-id="27867-105">As an \[[**in**](/windows/desktop/Midl/in)\] parameter, *achInOut* must point to valid storage on the client side.</span></span> <span data-ttu-id="27867-106">Le développeur alloue de la mémoire associée au tableau côté client avant d’effectuer l’appel de procédure distante.</span><span class="sxs-lookup"><span data-stu-id="27867-106">The developer allocates memory associated with the array on the client side before making the remote procedure call.</span></span>

<span data-ttu-id="27867-107">Les stubs utilisent la \[ [**\_ taille**](/windows/desktop/Midl/size-is) du \] paramètre *strsize* pour allouer de la mémoire sur le serveur, puis la longueur est le paramètre de la valeur de la fonction \[ [**\_**](/windows/desktop/Midl/length-is) \] de paramètre pour transmettre les éléments du tableau dans cette mémoire. </span><span class="sxs-lookup"><span data-stu-id="27867-107">The stubs use the \[[**size\_is**](/windows/desktop/Midl/size-is)\] parameter *strsize* to allocate memory on the server and then use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] parameter *pcbSize* to transmit the array elements into this memory.</span></span> <span data-ttu-id="27867-108">Le développeur doit s’assurer que le code client définit que la **\[ longueur \_ est \]** variable avant d’appeler la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="27867-108">The developer must make sure the client code sets the **\[length\_is\]** variable before calling the remote procedure.</span></span>

<span data-ttu-id="27867-109">Dans certains cas, l’utilisation de paramètres distincts au lieu d’une chaîne unique pour l’entrée et la sortie est plus efficace et offre une certaine flexibilité.</span><span class="sxs-lookup"><span data-stu-id="27867-109">In some situations, using separate parameters instead of a single string for the input and output is more efficient and provides flexibility.</span></span> <span data-ttu-id="27867-110">Cela est illustré dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="27867-110">This is demonstrated in the next example:</span></span>

``` syntax
/* client */ 
char achInOut[STRSIZE];
long cbSize;
...
gets_s(achInOut, STRSIZE);       // get patient input
cbSize = strlen(achInOut) + 1;   // transmit '\0' too
Analyze(achInOut, &cbSize);
```

<span data-ttu-id="27867-111">Dans l’exemple précédent, le tableau de caractères achInOut est également utilisé comme \[ paramètre de [**sortie**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="27867-111">In the previous example, the character array achInOut is also used as an \[[**out**](/windows/desktop/Midl/out-idl)\] parameter.</span></span> <span data-ttu-id="27867-112">En C, le nom du tableau est équivalent à l’utilisation d’un pointeur.</span><span class="sxs-lookup"><span data-stu-id="27867-112">In C, the name of the array is equivalent to the use of a pointer.</span></span> <span data-ttu-id="27867-113">Par défaut, tous les pointeurs de niveau supérieur sont des pointeurs de référence, ils ne changent pas dans la valeur et pointent vers la même zone de mémoire sur le client avant et après l’appel.</span><span class="sxs-lookup"><span data-stu-id="27867-113">By default, all top-level pointers are reference pointers — they do not change in value and they point to the same area of memory on the client before and after the call.</span></span> <span data-ttu-id="27867-114">Toute la mémoire à laquelle la procédure distante accède doit correspondre à la taille que le client spécifie avant l’appel, ou les stubs génèrent une exception.</span><span class="sxs-lookup"><span data-stu-id="27867-114">All memory that the remote procedure accesses must fit the size that the client specifies before the call, or the stubs will generate an exception.</span></span>

<span data-ttu-id="27867-115">Avant de retourner, la fonction analyze sur le serveur doit réinitialiser le paramètre *PCB* pour indiquer le nombre d’éléments que le serveur transmet au client comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="27867-115">Before returning, the Analyze function on the server must reset the *pcbSize* parameter to indicate the number of elements that the server will transmit to the client as shown:</span></span>

``` syntax
/* server */ 
Analyze(char * str, long * pcbSize)
{
   ...
   *pcbSize = strlen(str) + 1; // transmit '\0' too
   return;
}
```

 

 