---
title: Attributs directionnels (paramètre)
description: Les attributs directionnels décrivent si les données sont transmises du client au serveur, du serveur au client, ou les deux.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Appel de procédure distante RPC, décrit, attributs directionnels
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101989"
---
# <a name="directional-parameter-attributes"></a><span data-ttu-id="f2932-106">Attributs directionnels (paramètre)</span><span class="sxs-lookup"><span data-stu-id="f2932-106">Directional (Parameter) Attributes</span></span>

<span data-ttu-id="f2932-107">Les attributs directionnels décrivent si les données sont transmises du client au serveur, du serveur au client, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="f2932-107">Directional attributes describe whether the data is transmitted from client to server, server to client, or both.</span></span> <span data-ttu-id="f2932-108">Tous les paramètres du prototype de fonction doivent être associés à des attributs directionnels.</span><span class="sxs-lookup"><span data-stu-id="f2932-108">All parameters in the function prototype must be associated with directional attributes.</span></span> <span data-ttu-id="f2932-109">Les trois combinaisons possibles d’attributs directionnels sont : 1) \[ [**dans**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] et 3) \[ **dans**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="f2932-109">The three possible combinations of directional attributes are: 1) \[[**in**](/windows/desktop/Midl/in)\], 2) \[[**out**](/windows/desktop/Midl/out-idl)\], and 3) \[**in**, **out**\].</span></span> <span data-ttu-id="f2932-110">Ils décrivent la manière dont les paramètres sont transmis entre les appels et les procédures appelées.</span><span class="sxs-lookup"><span data-stu-id="f2932-110">These describe the way parameters are passed between calling and called procedures.</span></span> <span data-ttu-id="f2932-111">Quand vous compilez en mode par défaut (Microsoft-Extended) et que vous omettez un attribut directionnel pour un paramètre, le compilateur MIDL utilise une valeur par défaut \[ **dans** \] .</span><span class="sxs-lookup"><span data-stu-id="f2932-111">When you compile in the default (Microsoft-extended mode) and you omit a directional attribute for a parameter, the MIDL compiler assumes a default value of \[**in**\].</span></span>

<span data-ttu-id="f2932-112">Un \[ [](/windows/desktop/Midl/out-idl) \] paramètre de sortie doit être un pointeur.</span><span class="sxs-lookup"><span data-stu-id="f2932-112">An \[[**out**](/windows/desktop/Midl/out-idl)\] parameter must be a pointer.</span></span> <span data-ttu-id="f2932-113">En fait, l' \[ attribut **out** \] n’est pas significatif lorsqu’il est appliqué à des paramètres qui n’agissent pas comme des pointeurs, car les paramètres de fonction C sont passés par valeur.</span><span class="sxs-lookup"><span data-stu-id="f2932-113">In fact, the \[**out**\] attribute is not meaningful when applied to parameters that do not act as pointers because C function parameters are passed by value.</span></span> <span data-ttu-id="f2932-114">En C, la fonction appelée reçoit une copie privée de la valeur de paramètre ; elle ne peut pas modifier la valeur de la fonction appelante pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2932-114">In C, the called function receives a private copy of the parameter value; it cannot change the calling function's value for that parameter.</span></span> <span data-ttu-id="f2932-115">Toutefois, si le paramètre agit comme un pointeur, il peut être utilisé pour accéder à la mémoire et le modifier.</span><span class="sxs-lookup"><span data-stu-id="f2932-115">If the parameter acts as a pointer, however, it can be used to access and modify memory.</span></span> <span data-ttu-id="f2932-116">L' \[ attribut **out** \] indique que la fonction serveur doit retourner la valeur à la fonction d’appel du client, et que la mémoire associée au pointeur doit être retournée conformément aux attributs assignés au pointeur.</span><span class="sxs-lookup"><span data-stu-id="f2932-116">The \[**out**\] attribute indicates that the server function should return the value to the client's calling function, and that memory associated with the pointer should be returned in accordance with the attributes assigned to the pointer.</span></span>

<span data-ttu-id="f2932-117">L’interface suivante montre les trois combinaisons possibles d’attributs directionnels qui peuvent être appliquées à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="f2932-117">The following interface demonstrates the three possible combinations of directional attributes that can be applied to a parameter.</span></span> <span data-ttu-id="f2932-118">La fonction **InOutProc** est définie dans le fichier IDL comme suit :</span><span class="sxs-lookup"><span data-stu-id="f2932-118">The function **InOutProc** is defined in the IDL file as:</span></span>

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

<span data-ttu-id="f2932-119">Le premier paramètre, *S1*, est \[ [**dans**](/windows/desktop/Midl/in) \] uniquement.</span><span class="sxs-lookup"><span data-stu-id="f2932-119">The first parameter, *s1*, is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="f2932-120">Sa valeur est transmise à l’ordinateur distant, mais n’est pas retournée à la procédure d’appel.</span><span class="sxs-lookup"><span data-stu-id="f2932-120">Its value is transmitted to the remote computer, but is not returned to the calling procedure.</span></span> <span data-ttu-id="f2932-121">Bien que l’application serveur puisse modifier sa valeur pour *S1*, la valeur *S1* sur le client est identique avant et après l’appel.</span><span class="sxs-lookup"><span data-stu-id="f2932-121">Although the server application can change its value for *s1*, the value of *s1* on the client is the same before and after the call.</span></span>

<span data-ttu-id="f2932-122">Le deuxième paramètre, *PS2*, est défini dans le prototype de fonction en tant que pointeur avec les deux \[ attributs [**in**](/windows/desktop/Midl/in) \] et \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="f2932-122">The second parameter, *ps2*, is defined in the function prototype as a pointer with both \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] attributes.</span></span> <span data-ttu-id="f2932-123">L' \[ attribut **in** \] indique que la valeur du paramètre est passée du client au serveur.</span><span class="sxs-lookup"><span data-stu-id="f2932-123">The \[**in**\] attribute indicates that the value of the parameter is passed from the client to the server.</span></span> <span data-ttu-id="f2932-124">L' \[ attribut **out** \] indique que la valeur désignée par *PS2* est retournée au client.</span><span class="sxs-lookup"><span data-stu-id="f2932-124">The \[**out**\] attribute indicates that the value pointed to by *ps2* is returned to the client.</span></span>

<span data-ttu-id="f2932-125">Le troisième paramètre est \[ uniquement [**sortant**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="f2932-125">The third parameter is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="f2932-126">L’espace est alloué pour le paramètre sur le serveur, mais la valeur n’est pas définie à l’entrée.</span><span class="sxs-lookup"><span data-stu-id="f2932-126">Space is allocated for the parameter on the server, but the value is undefined on entry.</span></span> <span data-ttu-id="f2932-127">Comme indiqué ci-dessus, tous les paramètres de \[ **sortie** \] doivent être des pointeurs.</span><span class="sxs-lookup"><span data-stu-id="f2932-127">As mentioned above, all \[**out**\] parameters must be pointers.</span></span>

<span data-ttu-id="f2932-128">La procédure distante modifie la valeur des trois paramètres, mais seules les nouvelles valeurs des \[ [](/windows/desktop/Midl/out-idl) \] paramètres out et \[ [**in**](/windows/desktop/Midl/in) \] sont disponibles pour le client.</span><span class="sxs-lookup"><span data-stu-id="f2932-128">The remote procedure changes the value of all three parameters, but only the new values of the \[[**out**](/windows/desktop/Midl/out-idl)\] and \[[**in**](/windows/desktop/Midl/in)\] parameters are available to the client.</span></span>


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



<span data-ttu-id="f2932-129">Au retour de l’appel à **InOutProc**, les deuxième et troisième paramètres sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="f2932-129">On return from the call to **InOutProc**, the second and third parameters are modified.</span></span> <span data-ttu-id="f2932-130">Le premier paramètre, qui est \[ uniquement [**dans**](/windows/desktop/Midl/in) \] , est inchangé.</span><span class="sxs-lookup"><span data-stu-id="f2932-130">The first parameter, which is \[[**in**](/windows/desktop/Midl/in)\] only, is unchanged.</span></span>

![paramètres in](images/prog-a22.png)

![out (paramètres)](images/prog-a23.png)

![paramètres en sortie](images/prog-a21.png)

 

 