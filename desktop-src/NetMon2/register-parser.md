---
description: La fonction d’exportation de registre doit être implémentée dans toutes les dll de l’analyseur. L’implémentation d’un registre crée et remplit une base de données de propriétés pour un protocole. Moniteur réseau utilise la base de données pour déterminer les propriétés prises en charge par le protocole.
ms.assetid: b8a2752d-30a6-48f2-90b3-b1430ae983d2
title: Enregistrer la fonction de rappel de l’analyseur (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Register
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: bc49cc083cf6ba46594473a041d9a1ad138efa22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517014"
---
# <a name="register-parser-callback-function"></a><span data-ttu-id="8c1a8-105">Enregistrer la fonction de rappel de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="8c1a8-105">Register Parser callback function</span></span>

<span data-ttu-id="8c1a8-106">La fonction d’exportation de **Registre** doit être implémentée dans toutes les dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-106">The **Register** export function must be implemented in all parser DLLs.</span></span> <span data-ttu-id="8c1a8-107">L’implémentation d’un **Registre** crée et remplit une [*base de données de propriétés*](p.md) pour un protocole.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-107">The implementation of **Register** creates and fills-in a [*property database*](p.md) for a protocol.</span></span> <span data-ttu-id="8c1a8-108">Moniteur réseau utilise la base de données pour déterminer les propriétés prises en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-108">Network Monitor uses the database to determine which properties the protocol supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c1a8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c1a8-109">Syntax</span></span>


```C++
VOID Register(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="8c1a8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c1a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c1a8-111">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c1a8-111">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c1a8-112">Handle du protocole que Moniteur réseau fournit lors de l’appel de **Register**.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-112">The handle of the protocol that Network Monitor provides when calling **Register**.</span></span> <span data-ttu-id="8c1a8-113">Le descripteur *hProtocol* est nécessaire lors de l’appel des fonctions d’assistance d’exportation.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-113">The *hProtocol* handle is needed when calling export helper functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c1a8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c1a8-114">Return value</span></span>

<span data-ttu-id="8c1a8-115">Aucun.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-115">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c1a8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="8c1a8-116">Remarks</span></span>

<span data-ttu-id="8c1a8-117">Moniteur réseau démarre l’appel de la fonction **Register** dès qu’une capture est chargée.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-117">Network Monitor starts calling the **Register** function as soon as a capture is loaded.</span></span> <span data-ttu-id="8c1a8-118">Moniteur réseau appelle la fonction **Register** pour chaque protocole qu’il peut identifier.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-118">Network Monitor calls the **Register** function for each protocol it can identify.</span></span> <span data-ttu-id="8c1a8-119">La fonction [CreateProtocol](createprotocol.md) passe un pointeur vers la fonction **Register** .</span><span class="sxs-lookup"><span data-stu-id="8c1a8-119">The [CreateProtocol](createprotocol.md) function passes a pointer to the **Register** function.</span></span>

<span data-ttu-id="8c1a8-120">L’implémentation de **Register** comprend des appels aux fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-120">The implementation of **Register** includes calls to the following functions.</span></span>

-   <span data-ttu-id="8c1a8-121">Un appel aux fonctions [CreatePropertyDatabase](createpropertydatabase.md) et [AddProperty](/previous-versions/bb251873(v=msdn.10)) pour créer une base de données de toutes les propriétés prises en charge par le protocole.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-121">A call to the [CreatePropertyDatabase](createpropertydatabase.md) and [AddProperty](/previous-versions/bb251873(v=msdn.10)) functions to create a database of all the properties that the protocol supports.</span></span>
-   <span data-ttu-id="8c1a8-122">Un appel à la fonction [CreateHandoffTable](createhandofftable.md) est requis si le protocole utilise un [*jeu de remise*](h.md).</span><span class="sxs-lookup"><span data-stu-id="8c1a8-122">A call to the [CreateHandoffTable](createhandofftable.md) function is required if the protocol uses a [*handoff set*](h.md).</span></span>

<span data-ttu-id="8c1a8-123">Si la DLL de l’analyseur contient plusieurs analyseurs et que l’analyseur peut détecter plusieurs protocoles, vous devez implémenter une fonction d' **inscription** pour chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-123">If the parser DLL contains multiple parsers, and the parser can detect more than one protocol, you must implement a **Register** function for each protocol.</span></span>



| <span data-ttu-id="8c1a8-124">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="8c1a8-124">For Information on</span></span>                                        | <span data-ttu-id="8c1a8-125">Consultez</span><span class="sxs-lookup"><span data-stu-id="8c1a8-125">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="8c1a8-126">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-126">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="8c1a8-127">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="8c1a8-127">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="8c1a8-128">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-128">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="8c1a8-129">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="8c1a8-129">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="8c1a8-130">La procédure d’implémentation de **Register**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="8c1a8-130">How to implement **Register**  includes an example.</span></span>       | [<span data-ttu-id="8c1a8-131">Implémentation du Registre</span><span class="sxs-lookup"><span data-stu-id="8c1a8-131">Implementing Register</span></span>](implementing-register.md)     |



 

## <a name="requirements"></a><span data-ttu-id="8c1a8-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c1a8-132">Requirements</span></span>



| <span data-ttu-id="8c1a8-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c1a8-133">Requirement</span></span> | <span data-ttu-id="8c1a8-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c1a8-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8c1a8-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c1a8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8c1a8-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c1a8-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8c1a8-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c1a8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8c1a8-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c1a8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8c1a8-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c1a8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c1a8-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c1a8-140"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c1a8-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c1a8-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="8c1a8-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="8c1a8-142">[AddProperty](/previous-versions/bb251873(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="8c1a8-143">CreateHandoffTable</span><span class="sxs-lookup"><span data-stu-id="8c1a8-143">CreateHandoffTable</span></span>](createhandofftable.md)
</dt> <dt>

[<span data-ttu-id="8c1a8-144">CreatePropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="8c1a8-144">CreatePropertyDatabase</span></span>](createpropertydatabase.md)
</dt> <dt>

[<span data-ttu-id="8c1a8-145">CreateProtocol</span><span class="sxs-lookup"><span data-stu-id="8c1a8-145">CreateProtocol</span></span>](createprotocol.md)
</dt> </dl>

 

