---
title: Tableaux variables
description: Dans MIDL, les tableaux variables ont une taille fixe. Ils permettent aux clients de transmettre différentes parties de tableaux des clients aux serveurs. La taille de la partie de tableau peut varier d’un appel à l’appel. Toutefois, la taille du tableau global est fixe.
ms.assetid: 31c4bc63-de55-4937-832e-8dde9bcc47b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b2d79ee37f3e366bbf232b362306f78ca6ada4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463526"
---
# <a name="varying-arrays"></a><span data-ttu-id="b6723-106">Tableaux variables</span><span class="sxs-lookup"><span data-stu-id="b6723-106">Varying Arrays</span></span>

<span data-ttu-id="b6723-107">Dans MIDL, les tableaux variables ont une taille fixe.</span><span class="sxs-lookup"><span data-stu-id="b6723-107">In MIDL, varying arrays are fixed in size.</span></span> <span data-ttu-id="b6723-108">Ils permettent aux clients de transmettre différentes parties de tableaux des clients aux serveurs.</span><span class="sxs-lookup"><span data-stu-id="b6723-108">They allow clients to pass different portions of arrays from clients to servers.</span></span> <span data-ttu-id="b6723-109">La taille de la partie de tableau peut varier d’un appel à l’appel.</span><span class="sxs-lookup"><span data-stu-id="b6723-109">The size of the array portion can vary from invocation to invocation.</span></span> <span data-ttu-id="b6723-110">Toutefois, la taille du tableau global est fixe.</span><span class="sxs-lookup"><span data-stu-id="b6723-110">However, the size of the overall array is fixed.</span></span>

<span data-ttu-id="b6723-111">Par exemple, l’exemple suivant illustre la définition d’une procédure distante dans une interface dans un fichier MIDL.</span><span class="sxs-lookup"><span data-stu-id="b6723-111">For instance, the following example shows the definition of a remote procedure in an interface in a MIDL file.</span></span> <span data-ttu-id="b6723-112">La taille du tableau que le client transmet au serveur est fixe par la taille de tableau constante \_ .</span><span class="sxs-lookup"><span data-stu-id="b6723-112">The size of the array that the client passes to the server is fixed by the constant ARRAY\_SIZE.</span></span> <span data-ttu-id="b6723-113">L’interface spécifie la partie du tableau que le client transmet au serveur dans les paramètres firstElement et chunkSize.</span><span class="sxs-lookup"><span data-stu-id="b6723-113">The interface specifies the portion of the array that the client passes to the server in the parameters firstElement and chunkSize.</span></span>

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(
        [in] long lFirstElement,
        [in] long lChunkSize,
        [in, first_is(lFirstElement), 
          length_is(lChunkSize)] char achArray[ARRAY_SIZE]
    );

    /* Other interface procedures are defined here. */
}
```

<span data-ttu-id="b6723-114">La définition d’interface utilise \[ [**tout d’abord \_**](/windows/desktop/Midl/first-is) l’attribut MIDL pour \] spécifier le numéro d’index du premier élément de la partie du tableau que le client transmet au serveur.</span><span class="sxs-lookup"><span data-stu-id="b6723-114">The interface definition uses the MIDL attribute \[[**first\_is**](/windows/desktop/Midl/first-is)\] to specify the index number of the first element in the portion of the array that the client passes to the server.</span></span> <span data-ttu-id="b6723-115">La \[ [**longueur \_ est**](/windows/desktop/Midl/length-is) \] attribute spécifie le nombre total d’éléments de tableau que le client passe.</span><span class="sxs-lookup"><span data-stu-id="b6723-115">The \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute specifies the total number of array elements that the client passes.</span></span> <span data-ttu-id="b6723-116">Pour plus d’informations sur ces attributs MIDL, consultez [attributs de tableau](array-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b6723-116">For more information on these MIDL attributes, see [Array Attributes](array-attributes.md).</span></span>

<span data-ttu-id="b6723-117">Le fragment de code suivant montre comment un client peut appeler la procédure distante définie dans le fichier MIDL précédent.</span><span class="sxs-lookup"><span data-stu-id="b6723-117">The following code fragment illustrates how a client might invoke the remote procedure defined in the preceding MIDL file.</span></span>


```C++
long lFirstArrayElementNumber = 20;
long lTotalElementsPassed = 100;
char achCharArray[ARRAY_SIZE];

// Code to store chars in the array goes here.

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);

firstArrayElementNumber = 120;
totalElementsPassed = 200;

MyRemoteProc(
    lFirstArrayElementNumber ,
    lTotalElementsPassed , 
    achCharArray);
```



<span data-ttu-id="b6723-118">Ce fragment appelle à deux reprises la procédure distante MyRemoteProc.</span><span class="sxs-lookup"><span data-stu-id="b6723-118">This fragment calls the remote procedure MyRemoteProc twice.</span></span> <span data-ttu-id="b6723-119">Lors du premier appel, il transmet les éléments de tableau numérotés de 20 à 119, comme indiqué par les valeurs des variables firstArrayElementNumber et totalElementsPassed.</span><span class="sxs-lookup"><span data-stu-id="b6723-119">On the first invocation it passes the array elements numbered 20 through 119, as indicated by the values in the variables firstArrayElementNumber and totalElementsPassed.</span></span> <span data-ttu-id="b6723-120">Lors du deuxième appel, le client passe les éléments de tableau numérotés de 120 à 319.</span><span class="sxs-lookup"><span data-stu-id="b6723-120">On the second call, the client passes the array elements numbered 120 through 319.</span></span>

 

 