---
description: La fonction d’exportation de désinscription libère les ressources utilisées pour créer la base de données de propriétés de protocole. La DLL de l’analyseur doit implémenter l’annulation de l’inscription.
ms.assetid: 80852aed-07aa-440f-a537-f6cce461292e
title: Annuler l’inscription de la fonction de rappel (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Deregister
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 9458ff74f29cd8eb7a75da0a3628a2dd1519ba43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202727"
---
# <a name="deregister-callback-function"></a><span data-ttu-id="cbf7b-104">Annuler l’inscription de la fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="cbf7b-104">Deregister callback function</span></span>

<span data-ttu-id="cbf7b-105">La fonction d’exportation de **désinscription** libère les ressources utilisées pour créer la [*base de données de propriétés de*](p.md)protocole.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-105">The **Deregister** export function frees the resources used to create the protocol [*property database*](p.md).</span></span> <span data-ttu-id="cbf7b-106">La DLL de l’analyseur doit implémenter l’annulation de l' **inscription**.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-106">The parser DLL must implement **Deregister**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf7b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cbf7b-107">Syntax</span></span>


```C++
VOID Deregister(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="cbf7b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cbf7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf7b-109">*hProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cbf7b-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf7b-110">Handle du protocole pour une base de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-110">Handle of the protocol for a specific database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf7b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cbf7b-111">Return value</span></span>

<span data-ttu-id="cbf7b-112">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbf7b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cbf7b-113">Remarks</span></span>

<span data-ttu-id="cbf7b-114">Moniteur réseau appelle la **désinscription** après avoir transmis toutes les informations de capture à la dll de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-114">Network Monitor calls **Deregister** after passing all the capture information to the parser DLL.</span></span> <span data-ttu-id="cbf7b-115">La DLL de l’analyseur doit implémenter une fonction de **désinscription** pour chaque protocole pris en charge par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-115">The parser DLL must implement a **Deregister** function for each protocol that the parser supports.</span></span>

<span data-ttu-id="cbf7b-116">Lors de l’implémentation de l’annulation de l' **inscription**, la dll de l’analyseur doit appeler la fonction [DestroyPropertyDatabase](destroypropertydatabase.md) pour libérer les ressources [*de la base de données de propriétés*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="cbf7b-116">When implementing **Deregister**, the parser DLL must call the [DestroyPropertyDatabase](destroypropertydatabase.md) function to release the [*property database*](p.md) resources.</span></span>



| <span data-ttu-id="cbf7b-117">Pour plus d’informations sur</span><span class="sxs-lookup"><span data-stu-id="cbf7b-117">For information on</span></span>                                        | <span data-ttu-id="cbf7b-118">Consultez</span><span class="sxs-lookup"><span data-stu-id="cbf7b-118">See</span></span>                                                    |
|-----------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="cbf7b-119">Ce que sont les analyseurs et comment ils fonctionnent avec Moniteur réseau.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-119">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="cbf7b-120">Analyseurs</span><span class="sxs-lookup"><span data-stu-id="cbf7b-120">Parsers</span></span>](parsers.md)                                 |
| <span data-ttu-id="cbf7b-121">Les points d’entrée inclus dans la DLL de l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-121">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="cbf7b-122">Architecture des DLL de l’analyseur</span><span class="sxs-lookup"><span data-stu-id="cbf7b-122">Parser DLL Architecture</span></span>](parser-dll-architecture.md) |
| <span data-ttu-id="cbf7b-123">La procédure d’implémentation de l’annulation de l' **inscription**  comprend un exemple.</span><span class="sxs-lookup"><span data-stu-id="cbf7b-123">How to implement **Deregister**  includes an example.</span></span>     | [<span data-ttu-id="cbf7b-124">Implémentation de l’annulation de l’inscription</span><span class="sxs-lookup"><span data-stu-id="cbf7b-124">Implementing Deregister</span></span>](implementing-deregister.md) |



 

## <a name="requirements"></a><span data-ttu-id="cbf7b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cbf7b-125">Requirements</span></span>



| <span data-ttu-id="cbf7b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cbf7b-126">Requirement</span></span> | <span data-ttu-id="cbf7b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbf7b-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf7b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbf7b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf7b-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbf7b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cbf7b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbf7b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf7b-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cbf7b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cbf7b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="cbf7b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbf7b-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbf7b-133"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbf7b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cbf7b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf7b-135">DestroyPropertyDatabase</span><span class="sxs-lookup"><span data-stu-id="cbf7b-135">DestroyPropertyDatabase</span></span>](destroypropertydatabase.md)
</dt> </dl>

 

 




