---
title: Attributs de tableau
description: Il existe une relation étroite entre les tableaux et les pointeurs dans le langage C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729436"
---
# <a name="array-attributes"></a><span data-ttu-id="6db8c-103">Attributs de tableau</span><span class="sxs-lookup"><span data-stu-id="6db8c-103">Array Attributes</span></span>

<span data-ttu-id="6db8c-104">Il existe une relation étroite entre les tableaux et les pointeurs dans le langage C.</span><span class="sxs-lookup"><span data-stu-id="6db8c-104">There is a close relationship between arrays and pointers in the C language.</span></span> <span data-ttu-id="6db8c-105">Lorsqu’il est passé en tant que paramètre à une fonction, un nom de tableau est traité comme un pointeur vers le premier élément du tableau, comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="6db8c-105">When passed as a parameter to a function, an array name is treated as a pointer to the first element of the array, as shown in the following example:</span></span>


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



<span data-ttu-id="6db8c-106">Dans un appel local, vous pouvez utiliser le paramètre de pointeur à mars par le biais de la mémoire et examiner le contenu d’autres adresses :</span><span class="sxs-lookup"><span data-stu-id="6db8c-106">In a local call, you can use the pointer parameter to march through memory and examine the contents of other addresses:</span></span>


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



<span data-ttu-id="6db8c-107">Lorsqu’un client passe un pointeur vers une procédure distante, le stub client transmet à la fois le pointeur et les données vers lesquelles il pointe.</span><span class="sxs-lookup"><span data-stu-id="6db8c-107">When a client passes a pointer to a remote procedure, the client stub transmits both the pointer and the data it points to.</span></span> <span data-ttu-id="6db8c-108">À moins que le pointeur ne soit limité à ses données correspondantes, toute la mémoire du client doit être transmise avec chaque appel distant.</span><span class="sxs-lookup"><span data-stu-id="6db8c-108">Unless the pointer is restricted to its corresponding data, all the client's memory must be transmitted with every remote call.</span></span> <span data-ttu-id="6db8c-109">En appliquant le typage fort dans la définition de l’interface, MIDL limite le traitement du stub client aux données qui correspondent au pointeur spécifié.</span><span class="sxs-lookup"><span data-stu-id="6db8c-109">By enforcing strong typing in the interface definition, MIDL limits client-stub processing to the data that corresponds to the specified pointer.</span></span>

<span data-ttu-id="6db8c-110">La taille du tableau et la plage d’éléments de tableau transmis à l’ordinateur distant peuvent être des constantes ou des variables.</span><span class="sxs-lookup"><span data-stu-id="6db8c-110">The size of the array and the range of array elements transmitted to the remote computer can be constant or variable.</span></span> <span data-ttu-id="6db8c-111">Lorsque ces valeurs sont variables et, par conséquent, déterminées au moment de l’exécution, vous devez utiliser des attributs dans le fichier IDL pour spécifier le nombre d’éléments de tableau à transmettre.</span><span class="sxs-lookup"><span data-stu-id="6db8c-111">When these values are variable, and thus determined at run time, you must use attributes in the IDL file to specify how many array elements to transmit.</span></span> <span data-ttu-id="6db8c-112">Les attributs MIDL suivants prennent en charge les limites de tableau.</span><span class="sxs-lookup"><span data-stu-id="6db8c-112">The following MIDL attributes support array bounds.</span></span>



| <span data-ttu-id="6db8c-113">Attribut</span><span class="sxs-lookup"><span data-stu-id="6db8c-113">Attribute</span></span>                             | <span data-ttu-id="6db8c-114">Description</span><span class="sxs-lookup"><span data-stu-id="6db8c-114">Description</span></span>                                             | <span data-ttu-id="6db8c-115">Default</span><span class="sxs-lookup"><span data-stu-id="6db8c-115">Default</span></span> |
|---------------------------------------|---------------------------------------------------------|---------|
| <span data-ttu-id="6db8c-116">\[[ **tout \_ d’abord** ,](/windows/desktop/Midl/first-is)\]</span><span class="sxs-lookup"><span data-stu-id="6db8c-116">\[ [**first\_is**](/windows/desktop/Midl/first-is)\]</span></span>   | <span data-ttu-id="6db8c-117">Index du premier élément de tableau transmis.</span><span class="sxs-lookup"><span data-stu-id="6db8c-117">Index of the first array element transmitted.</span></span>           | <span data-ttu-id="6db8c-118">0</span><span class="sxs-lookup"><span data-stu-id="6db8c-118">0</span></span>       |
| <span data-ttu-id="6db8c-119">\[la [ **dernière \_ est**](/windows/desktop/Midl/last-is)\]</span><span class="sxs-lookup"><span data-stu-id="6db8c-119">\[ [**last\_is**](/windows/desktop/Midl/last-is)\]</span></span>     | <span data-ttu-id="6db8c-120">Index du dernier élément de tableau transmis.</span><span class="sxs-lookup"><span data-stu-id="6db8c-120">Index of the last array element transmitted.</span></span>            | \-      |
| <span data-ttu-id="6db8c-121">\[la [ **longueur \_ est**](/windows/desktop/Midl/length-is)\]</span><span class="sxs-lookup"><span data-stu-id="6db8c-121">\[ [**length\_is**](/windows/desktop/Midl/length-is)\]</span></span> | <span data-ttu-id="6db8c-122">Nombre total d’éléments de tableau transmis.</span><span class="sxs-lookup"><span data-stu-id="6db8c-122">Total number of array elements transmitted.</span></span>             | \-      |
| <span data-ttu-id="6db8c-123">\[le [ **nombre maximal \_ est**](/windows/desktop/Midl/max-is)\]</span><span class="sxs-lookup"><span data-stu-id="6db8c-123">\[ [**max\_is**](/windows/desktop/Midl/max-is)\]</span></span>       | <span data-ttu-id="6db8c-124">Valeur d’index de tableau valide la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="6db8c-124">Highest valid array index value.</span></span>                        | \-      |
| <span data-ttu-id="6db8c-125">\[[ **Min \_ est**](/windows/desktop/Midl/min-is)\]</span><span class="sxs-lookup"><span data-stu-id="6db8c-125">\[ [**min\_is**](/windows/desktop/Midl/min-is)\]</span></span>       | <span data-ttu-id="6db8c-126">Valeur d’index de tableau valide la plus basse.</span><span class="sxs-lookup"><span data-stu-id="6db8c-126">Lowest valid array index value.</span></span>                         | <span data-ttu-id="6db8c-127">0</span><span class="sxs-lookup"><span data-stu-id="6db8c-127">0</span></span>       |
| <span data-ttu-id="6db8c-128">\[la [ **taille \_ est**](/windows/desktop/Midl/size-is)\]</span><span class="sxs-lookup"><span data-stu-id="6db8c-128">\[ [**size\_is**](/windows/desktop/Midl/size-is)\]</span></span>     | <span data-ttu-id="6db8c-129">Nombre total d’éléments de tableau alloués pour le tableau.</span><span class="sxs-lookup"><span data-stu-id="6db8c-129">Total number of array elements allocated for the array.</span></span> | \-      |



 

> [!Note]  
> <span data-ttu-id="6db8c-130">L’attribut **Min \_ is** n’est pas implémenté dans RPC.</span><span class="sxs-lookup"><span data-stu-id="6db8c-130">The **min\_is** attribute is not implemented in RPC.</span></span> <span data-ttu-id="6db8c-131">L’index de tableau minimal est toujours traité comme zéro.</span><span class="sxs-lookup"><span data-stu-id="6db8c-131">The minimum array index is always treated as zero.</span></span>

 

 

 