---
title: RPC_MGR_EPV (rpcdce. h)
description: Le type de données \_ EPV redirecteur RPC \_ définit un vecteur de point d’entrée de gestionnaire.
ms.assetid: 396e76de-065f-471e-ade9-34770b16a958
keywords:
- RPC_MGR_EPV RPC
topic_type:
- apiref
api_name:
- RPC_MGR_EPV
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549ca4b5245b12bda07b46407041a01175955693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740213"
---
# <a name="rpc_mgr_epv"></a><span data-ttu-id="a6798-104">\_EPV du gestionnaire RPC \_</span><span class="sxs-lookup"><span data-stu-id="a6798-104">RPC\_MGR\_EPV</span></span>

<span data-ttu-id="a6798-105">Le type de **données \_ \_ EPV redirecteur RPC** définit un vecteur de point d’entrée de gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="a6798-105">The data type **RPC\_MGR\_EPV** defines a manager entry-point vector.</span></span>

``` syntax
typedef void RPC_MGR_EPV;
typedef _if-name_SERVER-EPV {
  return-type (* Functionname)  (param-list);
...  //one entry for each function in IDL file
} if-name_SERVER_EPV:
```

## <a name="members"></a><span data-ttu-id="a6798-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a6798-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a6798-107"><span id="if-name"></span><span id="IF-NAME"></span>**If-Name**</span><span class="sxs-lookup"><span data-stu-id="a6798-107"><span id="if-name"></span><span id="IF-NAME"></span>**if-name**</span></span>
</dt> <dd>

<span data-ttu-id="a6798-108">Spécifie le nom de l’interface</span><span class="sxs-lookup"><span data-stu-id="a6798-108">Specifies the name of the interface</span></span>

</dd> <dt>

<span data-ttu-id="a6798-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**type de retour**</span><span class="sxs-lookup"><span data-stu-id="a6798-109"><span id="return-type"></span><span id="RETURN-TYPE"></span>**return-type**</span></span>
</dt> <dd>

<span data-ttu-id="a6798-110">Spécifie le type retourné par la fonction **nomfonction** indiquée dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-110">Specifies the type returned by the function **Functionname** indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="a6798-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**FunctionName**</span><span class="sxs-lookup"><span data-stu-id="a6798-111"><span id="Functionname"></span><span id="functionname"></span><span id="FUNCTIONNAME"></span>**Functionname**</span></span>
</dt> <dd>

<span data-ttu-id="a6798-112">Spécifie le nom de la fonction indiquée dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-112">Specifies the name of the function indicated in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="a6798-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**Param-liste**</span><span class="sxs-lookup"><span data-stu-id="a6798-113"><span id="param-list"></span><span id="PARAM-LIST"></span>**param-list**</span></span>
</dt> <dd>

<span data-ttu-id="a6798-114">Spécifie les paramètres indiqués pour la fonction **nomfonction** dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-114">Specifies the parameters indicated for the function **Functionname** in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a6798-115">Notes</span><span class="sxs-lookup"><span data-stu-id="a6798-115">Remarks</span></span>

<span data-ttu-id="a6798-116">Le vecteur de point d’entrée du gestionnaire (EPV) est un tableau de pointeurs de fonction.</span><span class="sxs-lookup"><span data-stu-id="a6798-116">The manager entry-point vector (EPV) is an array of function pointers.</span></span> <span data-ttu-id="a6798-117">Le tableau contient des pointeurs vers les implémentations des fonctions spécifiées dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-117">The array contains pointers to the implementations of the functions specified in the IDL file.</span></span> <span data-ttu-id="a6798-118">Le nombre d’éléments dans le tableau est défini sur le nombre de fonctions spécifiées dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-118">The number of elements in the array is set to the number of functions specified in the IDL file.</span></span> <span data-ttu-id="a6798-119">Une application peut également avoir plusieurs EPVs, représentant plusieurs implémentations des fonctions spécifiées dans l’interface.</span><span class="sxs-lookup"><span data-stu-id="a6798-119">An application can also have multiple EPVs, representing multiple implementations of the functions specified in the interface.</span></span>

<span data-ttu-id="a6798-120">Le compilateur MIDL génère un type de données **EPV** par défaut nommé \* if-name \***\_ Server \_ EPV**, où *-Name* spécifie l’identificateur d’interface dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-120">The MIDL compiler generates a default **EPV** data type named \*if-name\***\_SERVER\_EPV**, where *if-name* specifies the interface identifier in the IDL file.</span></span> <span data-ttu-id="a6798-121">Le compilateur MIDL Initialise ce **EPV** par défaut pour contenir des pointeurs fonction pour chacune des procédures spécifiées dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-121">The MIDL compiler initializes this default **EPV** to contain function pointers for each of the procedures specified in the IDL file.</span></span>

<span data-ttu-id="a6798-122">Lorsque le serveur offre plusieurs implémentations de la même interface, l’application serveur doit déclarer et initialiser une variable de type *If-name \* \* \* \_ Server \_ EPV*\* pour chaque implémentation de l’interface.</span><span class="sxs-lookup"><span data-stu-id="a6798-122">When the server offers multiple implementations of the same interface, the server application must declare and initialize one variable of type *if-name\*\*\*\_SERVER\_EPV*\* for each implementation of the interface.</span></span> <span data-ttu-id="a6798-123">Chaque **EPV** doit contenir un point d’entrée (pointeur de fonction) pour chaque procédure définie dans le fichier IDL.</span><span class="sxs-lookup"><span data-stu-id="a6798-123">Each **EPV** must contain one entry point (function pointer) for each procedure defined in the IDL file.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6798-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6798-124">Requirements</span></span>



| <span data-ttu-id="a6798-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6798-125">Requirement</span></span> | <span data-ttu-id="a6798-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6798-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6798-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6798-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a6798-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6798-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a6798-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6798-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a6798-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6798-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a6798-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a6798-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6798-132"><dt>Rpcdce. h (inclure RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6798-132"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6798-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6798-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6798-134">**RpcServerRegisterIf**</span><span class="sxs-lookup"><span data-stu-id="a6798-134">**RpcServerRegisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> <dt>

[<span data-ttu-id="a6798-135">**RpcServerRegisterIf2**</span><span class="sxs-lookup"><span data-stu-id="a6798-135">**RpcServerRegisterIf2**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2)
</dt> <dt>

[<span data-ttu-id="a6798-136">**RpcServerRegisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="a6798-136">**RpcServerRegisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)
</dt> <dt>

[<span data-ttu-id="a6798-137">**RpcServerUnregisterIf**</span><span class="sxs-lookup"><span data-stu-id="a6798-137">**RpcServerUnregisterIf**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)
</dt> <dt>

[<span data-ttu-id="a6798-138">**RpcServerUnregisterIfEx**</span><span class="sxs-lookup"><span data-stu-id="a6798-138">**RpcServerUnregisterIfEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)
</dt> </dl>

 

 





