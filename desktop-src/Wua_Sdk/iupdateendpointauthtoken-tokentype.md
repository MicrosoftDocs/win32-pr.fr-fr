---
description: Obtient le type du jeton de point de terminaison, tel qu’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1.
ms.assetid: 1C6FFAD7-DC80-4957-96B4-FA0D954786DD
title: 'IUpdateEndpointAuthToken :: TokenType, méthode (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointAuthToken.TokenType
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bc2373c5dd49a3bf01d39b63360a3cf9df9f57d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526679"
---
# <a name="iupdateendpointauthtokentokentype-method"></a><span data-ttu-id="bd12e-103">IUpdateEndpointAuthToken :: TokenType, méthode</span><span class="sxs-lookup"><span data-stu-id="bd12e-103">IUpdateEndpointAuthToken::TokenType method</span></span>

<span data-ttu-id="bd12e-104">Obtient le type du jeton de point de terminaison, tel qu’un jeton WS-Security SAML (Security Assertion Markup Language) 1,1.</span><span class="sxs-lookup"><span data-stu-id="bd12e-104">Gets the type of the endpoint token, such as a WS-Security SAML (Security Assertion Markup Language) 1.1 token.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd12e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd12e-105">Syntax</span></span>


```C++
HRESULT TokenType(
  [out] UpdateEndpointAuthTokenType *pTokenType
);
```



## <a name="parameters"></a><span data-ttu-id="bd12e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bd12e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd12e-107">*pTokenType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bd12e-107">*pTokenType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd12e-108">Type du jeton de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="bd12e-108">The type of the endpoint token.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd12e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bd12e-109">Return value</span></span>

<span data-ttu-id="bd12e-110">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="bd12e-110">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="bd12e-111">Sinon, retourne un code d’erreur COM ou Windows.</span><span class="sxs-lookup"><span data-stu-id="bd12e-111">Otherwise, returns a COM or Windows error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd12e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd12e-112">Requirements</span></span>



| <span data-ttu-id="bd12e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd12e-113">Requirement</span></span> | <span data-ttu-id="bd12e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd12e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd12e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd12e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bd12e-116">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd12e-116">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="bd12e-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd12e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bd12e-118">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd12e-118">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="bd12e-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd12e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd12e-120"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd12e-120"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd12e-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="bd12e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd12e-122"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd12e-122"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd12e-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bd12e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd12e-124"><dt>UpdateEndpointAuth. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd12e-124"><dt>UpdateEndpointAuth.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd12e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bd12e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd12e-126"><dt>UpdateEndpointAuth.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd12e-126"><dt>UpdateEndpointAuth.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd12e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd12e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd12e-128">**IUpdateEndpointAuthToken**</span><span class="sxs-lookup"><span data-stu-id="bd12e-128">**IUpdateEndpointAuthToken**</span></span>](iupdateendpointauthtoken.md)
</dt> </dl>

 

 




