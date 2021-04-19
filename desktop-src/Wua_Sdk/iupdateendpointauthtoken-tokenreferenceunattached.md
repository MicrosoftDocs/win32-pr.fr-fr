---
description: Obtient le format XML d’une référence non attachée au jeton.
ms.assetid: D5D61ED7-68FB-4FC0-9C2A-90D3B1219351
title: 'IUpdateEndpointAuthToken :: TokenReferenceUnattached, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenReferenceUnattached
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: 7f9a25c444cf1ba8421d3787a9ead242750e5756
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513435"
---
# <a name="iupdateendpointauthtokentokenreferenceunattached-method"></a><span data-ttu-id="da625-103">IUpdateEndpointAuthToken :: TokenReferenceUnattached, méthode</span><span class="sxs-lookup"><span data-stu-id="da625-103">IUpdateEndpointAuthToken::TokenReferenceUnattached method</span></span>

<span data-ttu-id="da625-104">Obtient le format XML d’une référence non attachée au jeton.</span><span class="sxs-lookup"><span data-stu-id="da625-104">Gets the XML format of an unattached reference to the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="da625-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da625-105">Syntax</span></span>


```C++
HRESULT TokenReferenceUnattached(
  [out] BSTR *pszTokenReference
);
```



## <a name="parameters"></a><span data-ttu-id="da625-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da625-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da625-107">*pszTokenReference* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="da625-107">*pszTokenReference* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da625-108">Pointeur vers la référence du jeton non attaché.</span><span class="sxs-lookup"><span data-stu-id="da625-108">Pointer to the unattached token reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da625-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da625-109">Return value</span></span>

<span data-ttu-id="da625-110">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="da625-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="da625-111">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="da625-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da625-112">Notes</span><span class="sxs-lookup"><span data-stu-id="da625-112">Remarks</span></span>

<span data-ttu-id="da625-113">Une référence non attachée fait référence à un referece (tel que le signature qui utilise le jeton) qui n’est pas dans le message où réside le jeton.</span><span class="sxs-lookup"><span data-stu-id="da625-113">An unattached reference refers a referece (such as the signiture that is using the token) that is not in the message where the token resides.</span></span>

## <a name="requirements"></a><span data-ttu-id="da625-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da625-114">Requirements</span></span>



| <span data-ttu-id="da625-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da625-115">Requirement</span></span> | <span data-ttu-id="da625-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="da625-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da625-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da625-117">Minimum supported client</span></span><br/> | <span data-ttu-id="da625-118">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da625-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="da625-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da625-119">Minimum supported server</span></span><br/> | <span data-ttu-id="da625-120">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da625-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="da625-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="da625-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="da625-122"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="da625-122"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="da625-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="da625-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da625-124"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da625-124"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="da625-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="da625-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="da625-126"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da625-126"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="da625-127">DLL</span><span class="sxs-lookup"><span data-stu-id="da625-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da625-128"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da625-128"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da625-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da625-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da625-130">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="da625-130">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




