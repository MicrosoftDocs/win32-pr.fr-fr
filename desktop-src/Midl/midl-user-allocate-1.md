---
title: attribut midl_user_allocate
description: La \_ \_ fonction d’allocation utilisateur MIDL est une fonction que les applications client et serveur fournissent pour allouer de la mémoire.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate MIDL de l’attribut
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315060"
---
# <a name="midl_user_allocate-attribute"></a><span data-ttu-id="0b8aa-104">attribut d’allocation de l' \_ utilisateur MIDL \_</span><span class="sxs-lookup"><span data-stu-id="0b8aa-104">midl\_user\_allocate attribute</span></span>

<span data-ttu-id="0b8aa-105">La fonction d' **\_ \_ allocation utilisateur MIDL** est une fonction que les applications client et serveur fournissent pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-105">The **midl\_user\_allocate** function is a function that client and server applications provide to allocate memory.</span></span>

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a><span data-ttu-id="0b8aa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b8aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b8aa-107">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="0b8aa-107">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="0b8aa-108">Spécifie le nombre d’octets à allouer.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-108">Specifies the count of bytes to allocate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0b8aa-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0b8aa-109">Remarks</span></span>

<span data-ttu-id="0b8aa-110">Les applications clientes et les applications serveur doivent implémenter la fonction d' **\_ \_ allocation utilisateur MIDL** , sauf si vous compilez en mode de compatibilité OSF ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="0b8aa-110">Both client applications and server applications must implement the **midl\_user\_allocate** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="0b8aa-111">Les applications et les stubs générés appellent **MIDL \_ User \_ allocate** lors du traitement d’objets référencés par des pointeurs :</span><span class="sxs-lookup"><span data-stu-id="0b8aa-111">Applications and generated stubs call **midl\_user\_allocate** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="0b8aa-112">L’application serveur doit appeler **MIDL \_ User \_ allocate** pour allouer de la mémoire pour le application, par exemple, lors de la création d’un nouveau nœud.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-112">The server application should call **midl\_user\_allocate** to allocate memory for the applicationâ€”for example, when creating a new node.</span></span>
-   <span data-ttu-id="0b8aa-113">Le stub serveur appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données pointant vers l’espace d’adressage du serveur.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-113">The server stub calls **midl\_user\_allocate** when unmarshaling pointed-at data into the server address space.</span></span>
-   <span data-ttu-id="0b8aa-114">Le stub client appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données à partir du serveur qui est référencé par un pointeur de [**sortie**](out-idl.md) .</span><span class="sxs-lookup"><span data-stu-id="0b8aa-114">The client stub calls **midl\_user\_allocate** when unmarshaling data from the server that is referenced by an [**out**](out-idl.md) pointer.</span></span> <span data-ttu-id="0b8aa-115">Notez que pour les **\[** [](in.md) **\]** pointeurs in, **\[ \] out** et **\[** [**unique**](unique.md) **\]** , le stub client appelle l’allocation de l' **\_ utilisateur \_ MIDL** uniquement si la valeur de pointeur **\[ unique \]** était **null** en entrée et que les modifications apportées à une valeur non **null** au cours de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-115">Note that for **\[**[**in**](in.md)**\]**, **\[out\]**, and **\[**[**unique**](unique.md)**\]** pointers, the client stub calls **midl\_user\_allocate** only if the **\[unique\]** pointer value was **NULL** on input and changes to a non-**NULL** value during the call.</span></span> <span data-ttu-id="0b8aa-116">Si le pointeur **\[ \] unique** n’était pas **null** en entrée, le stub client écrit les données associées dans la mémoire existante.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-116">If the **\[unique\]** pointer was non-**NULL** on input, the client stub writes the associated data into existing memory.</span></span>

<span data-ttu-id="0b8aa-117">Si **l' \_ \_ allocation d’utilisateur MIDL** échoue pour allouer de la mémoire, elle doit retourner un pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="0b8aa-117">If **midl\_user\_allocate** fails to allocate memory, it must return a **NULL** pointer.</span></span>

<span data-ttu-id="0b8aa-118">Il est recommandé que **l' \_ \_ allocation d’utilisateur MIDL** retourne un pointeur de 8 octets alignés.</span><span class="sxs-lookup"><span data-stu-id="0b8aa-118">It is recommended that **midl\_user\_allocate** return a pointer that is 8 bytes aligned.</span></span>

## <a name="examples"></a><span data-ttu-id="0b8aa-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b8aa-119">Examples</span></span>


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a><span data-ttu-id="0b8aa-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b8aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b8aa-121">**lui**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-121">**allocate**</span></span>](allocate.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-122">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-122">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-123">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="0b8aa-123">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="0b8aa-124">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="0b8aa-124">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-125">**in**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-125">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-126">**\_utilisateur \_ gratuit MIDL**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-126">**midl\_user\_free**</span></span>](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[<span data-ttu-id="0b8aa-127">**/osf**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-127">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-128">**à**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-128">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-129">**ptr**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-129">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-130">**ref**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-130">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="0b8aa-131">**unique**</span><span class="sxs-lookup"><span data-stu-id="0b8aa-131">**unique**</span></span>](unique.md)
</dt> </dl>

 

 