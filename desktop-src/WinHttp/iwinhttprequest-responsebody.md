---
description: Récupère le corps d’entité de réponse sous la forme d’un tableau d’octets non signés.
ms.assetid: 557913e0-9f19-42fc-bfca-9ed248972b4b
title: 'IWinHttpRequest :: ResponseBody, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseBody
- IWinHttpRequest.get_ResponseBody
- WinHttpRequest.ResponseBody
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5a608f2744ad2880ecf7c4862b03821afcef9630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528348"
---
# <a name="iwinhttprequestresponsebody-property"></a><span data-ttu-id="4b198-103">IWinHttpRequest :: ResponseBody, propriété</span><span class="sxs-lookup"><span data-stu-id="4b198-103">IWinHttpRequest::ResponseBody property</span></span>

<span data-ttu-id="4b198-104">La propriété **ResponseBody** récupère le corps d’entité de réponse sous la forme d’un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="4b198-104">The **ResponseBody** property retrieves the response entity body as an array of unsigned bytes.</span></span>

<span data-ttu-id="4b198-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="4b198-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b198-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b198-106">Syntax</span></span>


```C++
HRESULT get_ResponseBody(
  [out, retval] VARIANT *Body
);
```


```JScript

vtResponseBody = WinHttpRequest.ResponseBody
```





## <a name="property-value"></a><span data-ttu-id="4b198-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4b198-107">Property value</span></span>

<span data-ttu-id="4b198-108">Valeur de **type Variant** qui reçoit le corps d’entité de réponse sous la forme d’un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="4b198-108">A **Variant** value that receives the response entity body as an array of unsigned bytes.</span></span> <span data-ttu-id="4b198-109">Ce tableau contient les données brutes telles qu’elles ont été reçues directement à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="4b198-109">This array contains the raw data as received directly from the server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b198-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4b198-110">Error codes</span></span>

<span data-ttu-id="4b198-111">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4b198-111">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b198-112">Notes</span><span class="sxs-lookup"><span data-stu-id="4b198-112">Remarks</span></span>

<span data-ttu-id="4b198-113">Cette propriété retourne les données de réponse dans un tableau d’octets non signés.</span><span class="sxs-lookup"><span data-stu-id="4b198-113">This property returns the response data in an array of unsigned bytes.</span></span> <span data-ttu-id="4b198-114">Si la réponse n’a pas de corps de réponse, un variant vide est retourné.</span><span class="sxs-lookup"><span data-stu-id="4b198-114">If the response does not have a response body, an empty variant is returned.</span></span> <span data-ttu-id="4b198-115">Cette propriété ne peut être appelée qu’une fois que la méthode [**Send**](iwinhttprequest-send.md) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="4b198-115">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="4b198-116">Pour plus d’informations sur l’implémentation de pour Windows XP et Windows 2000, consultez [Configuration requise](winhttp-start-page.md)pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="4b198-116">For more information about implementation for Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b198-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b198-117">Requirements</span></span>



| <span data-ttu-id="4b198-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b198-118">Requirement</span></span> | <span data-ttu-id="4b198-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b198-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b198-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b198-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4b198-121">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b198-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="4b198-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b198-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4b198-123">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b198-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="4b198-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4b198-124">Redistributable</span></span><br/>          | <span data-ttu-id="4b198-125">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="4b198-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="4b198-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="4b198-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b198-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b198-127"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="4b198-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b198-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="4b198-129"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b198-129"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="4b198-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4b198-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b198-131"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b198-131"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="4b198-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b198-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b198-133">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4b198-133">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="4b198-134">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="4b198-134">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="4b198-135">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="4b198-135">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="4b198-136">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="4b198-136">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)
</dt> <dt>

[<span data-ttu-id="4b198-137">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="4b198-137">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




