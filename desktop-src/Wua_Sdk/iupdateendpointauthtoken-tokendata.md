---
description: Obtient les données XML (envoyées sur le réseau) qui représentent le jeton.
ms.assetid: 52EC991A-0499-4182-AC4F-512BAFB4F896
title: 'IUpdateEndpointAuthToken :: TokenData, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenData
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: e75df7f5b13eaf36854cf7ed9abc5988b02462ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512992"
---
# <a name="iupdateendpointauthtokentokendata-method"></a><span data-ttu-id="1763a-103">IUpdateEndpointAuthToken :: TokenData, méthode</span><span class="sxs-lookup"><span data-stu-id="1763a-103">IUpdateEndpointAuthToken::TokenData method</span></span>

<span data-ttu-id="1763a-104">Obtient les données XML (envoyées sur le réseau) qui représentent le jeton.</span><span class="sxs-lookup"><span data-stu-id="1763a-104">Gets the XML data (sent over the wire) that represents the token.</span></span>

## <a name="syntax"></a><span data-ttu-id="1763a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1763a-105">Syntax</span></span>


```C++
HRESULT TokenData(
  [out] BSTR *pszTokenData
);
```



## <a name="parameters"></a><span data-ttu-id="1763a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1763a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1763a-107">*pszTokenData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1763a-107">*pszTokenData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1763a-108">Données XML (envoyées sur le réseau) qui représentent le jeton.</span><span class="sxs-lookup"><span data-stu-id="1763a-108">The XML data (sent over the wire) that represents the token.</span></span> <span data-ttu-id="1763a-109">Par exemple, les données d’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1 est le code SAML qui est ajouté à la requête.</span><span class="sxs-lookup"><span data-stu-id="1763a-109">For example, the data for a WS-Security SAML (Security Assertion Markup Language) 1.1 token is the SAML code that is added to the request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1763a-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1763a-110">Return value</span></span>

<span data-ttu-id="1763a-111">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="1763a-111">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="1763a-112">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="1763a-112">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1763a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1763a-113">Requirements</span></span>



| <span data-ttu-id="1763a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1763a-114">Requirement</span></span> | <span data-ttu-id="1763a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1763a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1763a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1763a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1763a-117">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1763a-117">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="1763a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1763a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1763a-119">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1763a-119">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="1763a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1763a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1763a-121"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="1763a-121"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="1763a-122">MIDL</span><span class="sxs-lookup"><span data-stu-id="1763a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1763a-123"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1763a-123"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="1763a-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1763a-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1763a-125"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1763a-125"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="1763a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1763a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1763a-127"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1763a-127"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1763a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1763a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1763a-129">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="1763a-129">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




