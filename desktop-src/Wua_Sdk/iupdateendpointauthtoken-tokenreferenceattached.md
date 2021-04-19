---
description: Obtient le format XML d’une référence jointe au jeton.
ms.assetid: F4329A2E-61FD-40E0-9E24-87C9A4585E55
title: 'IUpdateEndpointAuthToken :: TokenReferenceAttached, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceAttached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 9582c54c42e2416d5d7a98e85eba3151fd6769a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514843"
---
# <a name="iupdateendpointauthtokentokenreferenceattached-method"></a><span data-ttu-id="e389f-103">IUpdateEndpointAuthToken :: TokenReferenceAttached, méthode</span><span class="sxs-lookup"><span data-stu-id="e389f-103">IUpdateEndpointAuthToken::TokenReferenceAttached method</span></span>

<span data-ttu-id="e389f-104">Obtient le format XML d’une référence jointe au jeton.</span><span class="sxs-lookup"><span data-stu-id="e389f-104">Gets the XML format of an attached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="e389f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e389f-105">Syntax</span></span>


```C++
HRESULT TokenReferenceAttached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="e389f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e389f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e389f-107">*pszTokenReference* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e389f-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e389f-108">Pointeur vers la référence du jeton attaché.</span><span class="sxs-lookup"><span data-stu-id="e389f-108">Pointer to the attached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e389f-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e389f-109">Return value</span></span>

<span data-ttu-id="e389f-110">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e389f-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="e389f-111">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="e389f-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e389f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e389f-112">Remarks</span></span>

<span data-ttu-id="e389f-113">Une référence jointe fait référence à un referece (tel que le signature qui utilise le jeton) qui se trouve dans le même message que celui où se trouve le jeton.</span><span class="sxs-lookup"><span data-stu-id="e389f-113">An attached reference refers a referece (such as the signiture that is using the token) that is in the same message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="e389f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e389f-114">Requirements</span></span>



| <span data-ttu-id="e389f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e389f-115">Requirement</span></span> | <span data-ttu-id="e389f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e389f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e389f-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e389f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e389f-118">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e389f-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="e389f-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e389f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e389f-120">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e389f-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="e389f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e389f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e389f-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="e389f-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="e389f-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="e389f-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e389f-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e389f-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="e389f-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e389f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e389f-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e389f-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="e389f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e389f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e389f-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e389f-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e389f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e389f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e389f-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="e389f-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




