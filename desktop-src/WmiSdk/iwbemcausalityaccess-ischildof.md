---
description: La méthode IsChildOf détermine si une demande est un enfant d’une demande spécifiée (pId).
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess :: IsChildOf, méthode (Wbemint. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203957"
---
# <a name="iwbemcausalityaccessischildof-method"></a><span data-ttu-id="f76d2-103">IWbemCausalityAccess :: IsChildOf, méthode</span><span class="sxs-lookup"><span data-stu-id="f76d2-103">IWbemCausalityAccess::IsChildOf method</span></span>

<span data-ttu-id="f76d2-104">La méthode **IsChildOf** détermine si une demande est un enfant d’une demande spécifiée (PID).</span><span class="sxs-lookup"><span data-stu-id="f76d2-104">The **IsChildOf** method determines if a request is a child of a specified request (pId).</span></span> <span data-ttu-id="f76d2-105">Une requête parent peut avoir plusieurs demandes enfants.</span><span class="sxs-lookup"><span data-stu-id="f76d2-105">A parent request can have multiple child requests.</span></span> <span data-ttu-id="f76d2-106">Chaque requête est identifiée par un identificateur global unique (GUID) et peut avoir une requête parente ou peut être une requête principale.</span><span class="sxs-lookup"><span data-stu-id="f76d2-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="f76d2-107">Un GUID est un nombre 128 bits unique.</span><span class="sxs-lookup"><span data-stu-id="f76d2-107">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="f76d2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f76d2-108">Syntax</span></span>


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a><span data-ttu-id="f76d2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f76d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f76d2-110">*PID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f76d2-110">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f76d2-111">Valeur GUID qui identifie de façon unique une demande.</span><span class="sxs-lookup"><span data-stu-id="f76d2-111">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="f76d2-112">Par exemple, 5b2fc63a-8AF4-44cb-960C-aefdced908d6.</span><span class="sxs-lookup"><span data-stu-id="f76d2-112">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f76d2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f76d2-113">Return value</span></span>

<span data-ttu-id="f76d2-114">Retourne la valeur Successful si la requête spécifiée est un enfant de la demande appelant la méthode **IsChildOf** .</span><span class="sxs-lookup"><span data-stu-id="f76d2-114">Returns successful if the specified request is a child of the request calling the **IsChildOf** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f76d2-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f76d2-115">Requirements</span></span>



| <span data-ttu-id="f76d2-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f76d2-116">Requirement</span></span> | <span data-ttu-id="f76d2-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f76d2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f76d2-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f76d2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f76d2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f76d2-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f76d2-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f76d2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f76d2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f76d2-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f76d2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="f76d2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f76d2-123"><dt>Wbemint. h</dt></span><span class="sxs-lookup"><span data-stu-id="f76d2-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="f76d2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="f76d2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f76d2-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f76d2-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f76d2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f76d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76d2-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="f76d2-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




