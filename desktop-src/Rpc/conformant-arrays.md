---
title: Tableaux conformes
description: La taille d’un tableau conforme peut varier ou se conformer chaque fois que le client le transmet à une procédure distante sur le serveur.
ms.assetid: b4aaec77-b7ae-495d-8666-4702017e675f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6f1491354f9cd26ef6100ab8d21f2ace3133f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031691"
---
# <a name="conformant-arrays"></a><span data-ttu-id="fd040-103">Tableaux conformes</span><span class="sxs-lookup"><span data-stu-id="fd040-103">Conformant Arrays</span></span>

<span data-ttu-id="fd040-104">La taille d’un tableau conforme peut varier ou se conformer chaque fois que le client le transmet à une procédure distante sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="fd040-104">The size of a conformant array can vary or conform each time the client passes it to a remote procedure on the server.</span></span> <span data-ttu-id="fd040-105">La définition d’interface dans le fichier MIDL de l’application permet au client de spécifier la taille du tableau chaque fois qu’il appelle la procédure distante.</span><span class="sxs-lookup"><span data-stu-id="fd040-105">The interface definition in the application's MIDL file enables the client to specify the size of the array each time it invokes the remote procedure.</span></span> <span data-ttu-id="fd040-106">Utilisez des crochets vides ( \[ \] ) ou un astérisque entre crochets ( \[ \* \] ) dans la définition du tableau pour indiquer un tableau conforme.</span><span class="sxs-lookup"><span data-stu-id="fd040-106">Use empty square brackets (\[ \]) or an asterisk in the square brackets (\[\*\]) in the array definition to indicate a conformant array.</span></span>

<span data-ttu-id="fd040-107">L’exemple suivant contient la définition d’une procédure distante dans une interface d’un fichier MIDL.</span><span class="sxs-lookup"><span data-stu-id="fd040-107">The following sample contains the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="fd040-108">Le client spécifie la taille du tableau qu’il transmet au serveur à l’aide du paramètre *arraySize*.</span><span class="sxs-lookup"><span data-stu-id="fd040-108">The client specifies the size of the array that it passes to the server by the parameter *arraySize*.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    MyRemoteProc(
         long lArraySize,
         [size_is(lArraySize)] char achArray[*]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="fd040-109">La définition d’interface utilise la \[ [**taille \_**](/windows/desktop/Midl/size-is) d’attribut MIDL \] pour spécifier la taille du tableau que le client transmet au serveur.</span><span class="sxs-lookup"><span data-stu-id="fd040-109">The interface definition uses the MIDL attribute \[[**size\_is**](/windows/desktop/Midl/size-is)\] to specify the size of the array that the client passes to the server.</span></span> <span data-ttu-id="fd040-110">Si vous préférez indiquer la valeur maximale des numéros d’index du tableau, utilisez plutôt l' \[ attribut [**Max \_ is**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="fd040-110">If you would rather indicate the maximum value of the array's index numbers, use the \[[**max\_is**](/windows/desktop/Midl/max-is)\] attribute instead.</span></span> <span data-ttu-id="fd040-111">Pour plus d’informations sur ces attributs MIDL, consultez [attributs de tableau](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="fd040-111">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="fd040-112">Le fragment de code suivant montre comment un client peut appeler la procédure distante définie dans le fichier MIDL précédent.</span><span class="sxs-lookup"><span data-stu-id="fd040-112">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lArrayLength = 20;
char achCharArray[20], achAnotherCharArray[200];

// Code to store 20 chars in achCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achCharArray);

lArrayLength = 200;

// Code to store 200 chars in achAnotherCharArray goes here.

MyRemoteProc(
    lArrayLength ,
    achAnotherCharArray);
```



<span data-ttu-id="fd040-113">Ce fragment appelle à deux reprises la procédure distante MyRemoteProc.</span><span class="sxs-lookup"><span data-stu-id="fd040-113">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="fd040-114">Lors du premier appel, il passe un tableau de 20 éléments.</span><span class="sxs-lookup"><span data-stu-id="fd040-114">On the first invocation it passes an array of 20 elements.</span></span> <span data-ttu-id="fd040-115">Lors du deuxième appel, le client passe un tableau de 200 éléments.</span><span class="sxs-lookup"><span data-stu-id="fd040-115">On the second call, the client passes an array of 200 elements.</span></span>

 

 