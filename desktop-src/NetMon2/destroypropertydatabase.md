---
description: La fonction DestroyPropertyDatabase libère les ressources utilisées pour créer la base de données de propriétés de protocole.
ms.assetid: a0d1c416-8b08-47ca-a88e-e70588574376
title: DestroyPropertyDatabase, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyPropertyDatabase
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: baedae22e948b38d9ff162942269ac4529896826
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952887"
---
# <a name="destroypropertydatabase-function"></a><span data-ttu-id="50c66-103">DestroyPropertyDatabase fonction)</span><span class="sxs-lookup"><span data-stu-id="50c66-103">DestroyPropertyDatabase function</span></span>

<span data-ttu-id="50c66-104">La fonction **DestroyPropertyDatabase** libère les ressources utilisées pour créer la [*base de données de propriétés de*](p.md)protocole.</span><span class="sxs-lookup"><span data-stu-id="50c66-104">The **DestroyPropertyDatabase** function releases the resources used to create the protocol [*property database*](p.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="50c66-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50c66-105">Syntax</span></span>


```C++
DWORD WINAPI DestroyPropertyDatabase(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="50c66-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50c66-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50c66-107">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50c66-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50c66-108">Handle de la base de données de propriétés à détruire.</span><span class="sxs-lookup"><span data-stu-id="50c66-108">Handle to the property database to be destroyed.</span></span> <span data-ttu-id="50c66-109">Le descripteur est passé à la DLL de l’analyseur quand Moniteur réseau appelle la fonction de [désinscription](deregister.md) .</span><span class="sxs-lookup"><span data-stu-id="50c66-109">The handle is passed to the parser DLL when Network Monitor calls the [Deregister](deregister.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50c66-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50c66-110">Return value</span></span>

<span data-ttu-id="50c66-111">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="50c66-111">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="50c66-112">Si la fonction échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="50c66-112">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="50c66-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="50c66-113">Return code</span></span>                                                                                              | <span data-ttu-id="50c66-114">Description</span><span class="sxs-lookup"><span data-stu-id="50c66-114">Description</span></span>                                |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="50c66-115"><dt>**\_erreur interne \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="50c66-115"><dt>**NMERR\_INTERNAL\_ERROR**</dt></span></span> </dl>    | <span data-ttu-id="50c66-116">Une erreur interne s’est produite.</span><span class="sxs-lookup"><span data-stu-id="50c66-116">An internal error occurred.</span></span> <br/>    |
| <dl> <span data-ttu-id="50c66-117"><dt>**NMERR \_ non valide \_ HPROTOCOL**</dt></span><span class="sxs-lookup"><span data-stu-id="50c66-117"><dt>**NMERR\_INVALID\_HPROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="50c66-118">Handle non valide dans *hProtocol*.</span><span class="sxs-lookup"><span data-stu-id="50c66-118">Invalid handle in *hProtocol*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="50c66-119">Notes</span><span class="sxs-lookup"><span data-stu-id="50c66-119">Remarks</span></span>

<span data-ttu-id="50c66-120">La fonction **DestroyPropertyDatabase** doit être appelée uniquement lors de l’implémentation de la fonction d’exportation de [désinscription](deregister.md) pour le protocole.</span><span class="sxs-lookup"><span data-stu-id="50c66-120">The **DestroyPropertyDatabase** function should be called only when implementing the [Deregister](deregister.md) export function for the protocol.</span></span> <span data-ttu-id="50c66-121">Pour les dll de l’analyseur qui prennent en charge plusieurs protocoles, la fonction **DestroyPropertyDatabase** est appelée pour chaque implémentation de l’annulation de l' **inscription**.</span><span class="sxs-lookup"><span data-stu-id="50c66-121">For parser DLLs that support multiple protocols, the **DestroyPropertyDatabase** function is called for each implementation of **Deregister**.</span></span>



| <span data-ttu-id="50c66-122">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="50c66-122">For information on</span></span>                                        | <span data-ttu-id="50c66-123">Consultez</span><span class="sxs-lookup"><span data-stu-id="50c66-123">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="50c66-124">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="50c66-124">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="50c66-125">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="50c66-125">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="50c66-126">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="50c66-126">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="50c66-127">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="50c66-127">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="50c66-128">La procédure d’implémentation de l’annulation de l' **inscription**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="50c66-128">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="50c66-129">Implémentation de l’annulation de l’inscription</span><span class="sxs-lookup"><span data-stu-id="50c66-129">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="50c66-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50c66-130">Requirements</span></span>



| <span data-ttu-id="50c66-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50c66-131">Requirement</span></span> | <span data-ttu-id="50c66-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="50c66-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="50c66-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50c66-133">Minimum supported client</span></span><br/> | <span data-ttu-id="50c66-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50c66-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="50c66-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50c66-135">Minimum supported server</span></span><br/> | <span data-ttu-id="50c66-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50c66-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="50c66-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="50c66-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="50c66-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="50c66-138"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="50c66-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50c66-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="50c66-140"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50c66-140"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="50c66-141">DLL</span><span class="sxs-lookup"><span data-stu-id="50c66-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50c66-142"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50c66-142"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50c66-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50c66-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c66-144">Désinscrire</span><span class="sxs-lookup"><span data-stu-id="50c66-144">Deregister</span></span>](deregister.md)
</dt> </dl>

 

 




