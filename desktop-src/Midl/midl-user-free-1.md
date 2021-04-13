---
title: attribut midl_user_free
description: La \_ fonction gratuite de l’utilisateur MIDL \_ est fournie par les applications client et serveur pour libérer de la mémoire allouée dynamiquement.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free MIDL de l’attribut
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53819035f700a948c9ca45c565310d7796516147
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314903"
---
# <a name="midl_user_free-attribute"></a><span data-ttu-id="4c781-104">\_ \_ attribut gratuit de l’utilisateur MIDL</span><span class="sxs-lookup"><span data-stu-id="4c781-104">midl\_user\_free attribute</span></span>

<span data-ttu-id="4c781-105">La **fonction \_ \_ gratuite de l’utilisateur MIDL** est fournie par les applications client et serveur pour libérer de la mémoire allouée dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="4c781-105">The **midl\_user\_free** function is provided by client and server applications to deallocate dynamically allocated memory.</span></span>

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a><span data-ttu-id="4c781-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c781-107">*p*</span><span class="sxs-lookup"><span data-stu-id="4c781-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="4c781-108">Pointeur vers le bloc de mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="4c781-108">A pointer to the memory block to be freed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c781-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4c781-109">Remarks</span></span>

<span data-ttu-id="4c781-110">L’application cliente et l’application serveur doivent implémenter la fonction **\_ \_ gratuite utilisateur MIDL** , sauf si vous compilez en mode de compatibilité OSF ([**/OSF**](-osf.md)).</span><span class="sxs-lookup"><span data-stu-id="4c781-110">Both client application and server application must implement the **midl\_user\_free** function, unless you are compiling in OSF-compatibility ([**/osf**](-osf.md)) mode.</span></span> <span data-ttu-id="4c781-111">La **fonction \_ \_ gratuite de l’utilisateur MIDL** doit pouvoir libérer tout le stockage alloué par l’allocation de l' [**\_ utilisateur \_ MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span><span class="sxs-lookup"><span data-stu-id="4c781-111">The **midl\_user\_free** function must be able to free all storage allocated by [**midl\_user\_allocate**](/windows/desktop/Rpc/the-midl-user-allocate-function).</span></span>

<span data-ttu-id="4c781-112">Les applications et les stubs appellent **MIDL \_ \_ sans utilisateur** lors de la gestion d’objets référencés par des pointeurs :</span><span class="sxs-lookup"><span data-stu-id="4c781-112">Applications and stubs call **midl\_user\_free** when dealing with objects referenced by pointers:</span></span>

-   <span data-ttu-id="4c781-113">L’application serveur doit appeler **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire allouée par le application, par exemple, lors de la suppression d’un nœud spécifié.</span><span class="sxs-lookup"><span data-stu-id="4c781-113">The server application should call **midl\_user\_free** to free memory allocated by the applicationâ€”for example, when deleting a specified node.</span></span>
-   <span data-ttu-id="4c781-114">Le stub serveur appelle **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire sur le serveur après avoir marshalé tous les **\[** arguments [**out**](out-idl.md) **\]** , les arguments out, les **\[** arguments **out \]** et la valeur de retour. [](in.md)</span><span class="sxs-lookup"><span data-stu-id="4c781-114">The server stub calls **midl\_user\_free** to release memory on the server after marshaling all **\[**[**out**](out-idl.md)**\]** arguments, **\[**[**in**](in.md), **out\]** arguments, and the return value.</span></span>

## <a name="examples"></a><span data-ttu-id="4c781-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="4c781-115">Examples</span></span>


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a><span data-ttu-id="4c781-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c781-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c781-117">**tableaux**</span><span class="sxs-lookup"><span data-stu-id="4c781-117">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="4c781-118">Tableaux et pointeurs</span><span class="sxs-lookup"><span data-stu-id="4c781-118">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="4c781-119">Attributs de tableau et de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="4c781-119">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c781-120">**in**</span><span class="sxs-lookup"><span data-stu-id="4c781-120">**in**</span></span>](in.md)
</dt> <dt>

[<span data-ttu-id="4c781-121">**allouer un \_ utilisateur MIDL \_**</span><span class="sxs-lookup"><span data-stu-id="4c781-121">**midl\_user\_allocate**</span></span>](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[<span data-ttu-id="4c781-122">**/osf**</span><span class="sxs-lookup"><span data-stu-id="4c781-122">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="4c781-123">**à**</span><span class="sxs-lookup"><span data-stu-id="4c781-123">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="4c781-124">**unique**</span><span class="sxs-lookup"><span data-stu-id="4c781-124">**unique**</span></span>](unique.md)
</dt> </dl>

 

 