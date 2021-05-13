---
description: Obtient l’état du compte de l’utilisateur.
title: DIDiskQuotaUser. AccountStatus, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841650"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="56d6a-103">DIDiskQuotaUser. AccountStatus, propriété</span><span class="sxs-lookup"><span data-stu-id="56d6a-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="56d6a-104">Obtient l’état du compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="56d6a-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="56d6a-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="56d6a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d6a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56d6a-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="56d6a-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="56d6a-107">Property value</span></span>

<span data-ttu-id="56d6a-108">Cette propriété peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="56d6a-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="56d6a-109">Statut</span><span class="sxs-lookup"><span data-stu-id="56d6a-109">Status</span></span>            | <span data-ttu-id="56d6a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="56d6a-110">Value</span></span> | <span data-ttu-id="56d6a-111">Description</span><span class="sxs-lookup"><span data-stu-id="56d6a-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="56d6a-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="56d6a-112">dqAcctResolved</span></span>    | <span data-ttu-id="56d6a-113">0</span><span class="sxs-lookup"><span data-stu-id="56d6a-113">0</span></span>     | <span data-ttu-id="56d6a-114">Les informations de compte sont résolues.</span><span class="sxs-lookup"><span data-stu-id="56d6a-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="56d6a-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="56d6a-115">dqAcctUnavailable</span></span> | <span data-ttu-id="56d6a-116">1</span><span class="sxs-lookup"><span data-stu-id="56d6a-116">1</span></span>     | <span data-ttu-id="56d6a-117">Les informations de compte ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="56d6a-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="56d6a-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="56d6a-118">dqAcctDeleted</span></span>     | <span data-ttu-id="56d6a-119">2</span><span class="sxs-lookup"><span data-stu-id="56d6a-119">2</span></span>     | <span data-ttu-id="56d6a-120">Le compte a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="56d6a-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="56d6a-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="56d6a-121">dqAcctInvalid</span></span>     | <span data-ttu-id="56d6a-122">3</span><span class="sxs-lookup"><span data-stu-id="56d6a-122">3</span></span>     | <span data-ttu-id="56d6a-123">Le compte n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="56d6a-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="56d6a-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="56d6a-124">dqAcctUnknown</span></span>     | <span data-ttu-id="56d6a-125">4</span><span class="sxs-lookup"><span data-stu-id="56d6a-125">4</span></span>     | <span data-ttu-id="56d6a-126">Le compte est introuvable.</span><span class="sxs-lookup"><span data-stu-id="56d6a-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="56d6a-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="56d6a-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="56d6a-128">5</span><span class="sxs-lookup"><span data-stu-id="56d6a-128">5</span></span>     | <span data-ttu-id="56d6a-129">Les informations de compte ne sont pas résolues.</span><span class="sxs-lookup"><span data-stu-id="56d6a-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="56d6a-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="56d6a-130">Requirements</span></span>



| <span data-ttu-id="56d6a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56d6a-131">Requirement</span></span> | <span data-ttu-id="56d6a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="56d6a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56d6a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56d6a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="56d6a-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56d6a-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="56d6a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56d6a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="56d6a-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56d6a-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="56d6a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="56d6a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56d6a-138"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="56d6a-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56d6a-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56d6a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d6a-140">**Objet DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="56d6a-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




