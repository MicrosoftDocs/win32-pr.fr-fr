---
title: Pointeurs uniques
description: Dans les programmes C, plusieurs pointeurs peuvent contenir l’adresse des données.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031276"
---
# <a name="unique-pointers"></a><span data-ttu-id="12ab2-103">Pointeurs uniques</span><span class="sxs-lookup"><span data-stu-id="12ab2-103">Unique Pointers</span></span>

<span data-ttu-id="12ab2-104">Dans les programmes C, plusieurs pointeurs peuvent contenir l’adresse des données.</span><span class="sxs-lookup"><span data-stu-id="12ab2-104">In C programs, more than one pointer can contain the address of data.</span></span> <span data-ttu-id="12ab2-105">Les pointeurs sont dits pour créer un [*alias*](a-glos.md) pour les données.</span><span class="sxs-lookup"><span data-stu-id="12ab2-105">The pointers are said to create an [*alias*](a-glos.md) for the data.</span></span> <span data-ttu-id="12ab2-106">Les alias sont également créés lorsque des pointeurs pointent vers des variables déclarées.</span><span class="sxs-lookup"><span data-stu-id="12ab2-106">Aliases are also created when pointers point at declared variables.</span></span> <span data-ttu-id="12ab2-107">Le fragment de code suivant illustre ces deux méthodes d’alias :</span><span class="sxs-lookup"><span data-stu-id="12ab2-107">The following code fragment illustrates both of these methods of aliasing:</span></span>


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



<span data-ttu-id="12ab2-108">Dans un programme C standard, vous pouvez spécifier une arborescence binaire à l’aide de la définition suivante :</span><span class="sxs-lookup"><span data-stu-id="12ab2-108">In a typical C program, you might specify a binary tree using the following definition:</span></span>


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



<span data-ttu-id="12ab2-109">Plusieurs pointeurs peuvent accéder au contenu d’un nœud d’arbre.</span><span class="sxs-lookup"><span data-stu-id="12ab2-109">More than one pointer can access the contents of a tree node.</span></span> <span data-ttu-id="12ab2-110">Cela est généralement parfait pour les applications non distribuées.</span><span class="sxs-lookup"><span data-stu-id="12ab2-110">This is generally fine for nondistributed applications.</span></span> <span data-ttu-id="12ab2-111">Toutefois, ce style de programmation génère du code de prise en charge RPC plus complexe.</span><span class="sxs-lookup"><span data-stu-id="12ab2-111">However, this style of programming generates more complicated RPC support code.</span></span> <span data-ttu-id="12ab2-112">Les stubs client et serveur requièrent le code supplémentaire pour gérer les données et les pointeurs.</span><span class="sxs-lookup"><span data-stu-id="12ab2-112">The client and server stubs require the additional code to manage the data and the pointers.</span></span> <span data-ttu-id="12ab2-113">Le code stub sous-jacent doit résoudre les différents pointeurs vers les adresses et déterminer la copie des données qui représente la version la plus récente.</span><span class="sxs-lookup"><span data-stu-id="12ab2-113">The underlying stub code must resolve the various pointers to the addresses and determine which copy of the data represents the most recent version.</span></span>

<span data-ttu-id="12ab2-114">La quantité de traitement peut être réduite si vous vous assurez que votre pointeur est la seule façon dont l’application peut accéder à cette zone de mémoire.</span><span class="sxs-lookup"><span data-stu-id="12ab2-114">The amount of processing can be reduced if you guarantee that your pointer is the only way the application can access that area of memory.</span></span> <span data-ttu-id="12ab2-115">Le pointeur peut toujours avoir la plupart des fonctionnalités d’un pointeur C.</span><span class="sxs-lookup"><span data-stu-id="12ab2-115">The pointer can still have many of the features of a C pointer.</span></span> <span data-ttu-id="12ab2-116">Par exemple, elle peut être modifiée entre les valeurs **null** et non **null** , ou rester inchangée.</span><span class="sxs-lookup"><span data-stu-id="12ab2-116">For example, it can change between **null** and non-**null** values or stay the same.</span></span> <span data-ttu-id="12ab2-117">L'exemple suivant illustre ce comportement.</span><span class="sxs-lookup"><span data-stu-id="12ab2-117">The following example illustrates this.</span></span> <span data-ttu-id="12ab2-118">Le pointeur est **null** avant l’appel et pointe vers une chaîne valide après l’appel :</span><span class="sxs-lookup"><span data-stu-id="12ab2-118">The pointer is **null** before the call and points to a valid string after the call:</span></span>

![modification du pointeur entre les valeurs NULL et non null](images/prog-a01.png)

<span data-ttu-id="12ab2-120">Par défaut, le compilateur MIDL applique l' \[ [](/windows/desktop/Midl/unique) \] attribut de pointeur unique à tous les pointeurs qui ne sont pas des paramètres.</span><span class="sxs-lookup"><span data-stu-id="12ab2-120">By default, the MIDL compiler applies the \[ [unique](/windows/desktop/Midl/unique)\] pointer attribute to all pointers that are not parameters.</span></span> <span data-ttu-id="12ab2-121">Ce paramètre par défaut peut être modifié à l’aide de l' \[ attribut [ \_ par défaut du pointeur](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="12ab2-121">This default setting can be changed with the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] attribute.</span></span>

<span data-ttu-id="12ab2-122">Un pointeur unique présente les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="12ab2-122">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="12ab2-123">Elle peut avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="12ab2-123">It can have the value **null**.</span></span>
-   <span data-ttu-id="12ab2-124">Elle peut passer de **null** à non **null** pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="12ab2-124">It can change from **null** to non-**null** during the call.</span></span> <span data-ttu-id="12ab2-125">Lorsque la valeur devient non **null**, une nouvelle mémoire est allouée au retour.</span><span class="sxs-lookup"><span data-stu-id="12ab2-125">When the value changes to non-**null**, new memory is allocated on return.</span></span>
-   <span data-ttu-id="12ab2-126">Elle peut passer d’une valeur non **null** à une **valeur null** pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="12ab2-126">It can change from non-**null** to **null** during the call.</span></span> <span data-ttu-id="12ab2-127">Lorsque la valeur est remplacée par **null**, l’application est responsable de la libération de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="12ab2-127">When the value changes to **NULL**, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="12ab2-128">La valeur peut passer d’une valeur non **null** à une autre.</span><span class="sxs-lookup"><span data-stu-id="12ab2-128">The value can change from one non-**null** value to another.</span></span>
-   <span data-ttu-id="12ab2-129">Le stockage vers lequel pointe un pointeur unique est inaccessible par tout autre pointeur ou nom dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="12ab2-129">The storage that a unique pointer points to cannot be accessed by any other pointer or name in the operation.</span></span>
-   <span data-ttu-id="12ab2-130">Les données de retour sont écrites dans le stockage existant si le pointeur n’a pas la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="12ab2-130">Return data is written into existing storage if the pointer does not have the value **null**.</span></span>

<span data-ttu-id="12ab2-131">L’exemple suivant montre comment définir un pointeur unique.</span><span class="sxs-lookup"><span data-stu-id="12ab2-131">The following example demonstrates how to define a unique pointer.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

<span data-ttu-id="12ab2-132">Dans cet exemple, le paramètre *ach* est un pointeur unique vers des données caractères qui est envoyé à un serveur à traiter avec la routine RemoteFn.</span><span class="sxs-lookup"><span data-stu-id="12ab2-132">In this example, the parameter *ach* is a unique pointer to character data that is sent to a server to be processed with the RemoteFn routine.</span></span>

 

 