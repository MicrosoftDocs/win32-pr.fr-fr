---
description: La méthode Abort interrompt une méthode d’envoi WinHTTP.
ms.assetid: 8326feef-8611-4441-b52d-74855e6acfff
title: 'IWinHttpRequest :: Abort, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Abort
- WinHttpRequest.Abort
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 56290dfc16f9986cb7d7596c098bb53c207efebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952780"
---
# <a name="iwinhttprequestabort-method"></a><span data-ttu-id="044a6-103">IWinHttpRequest :: Abort, méthode</span><span class="sxs-lookup"><span data-stu-id="044a6-103">IWinHttpRequest::Abort method</span></span>

<span data-ttu-id="044a6-104">La méthode **Abort** interrompt une méthode d' [**envoi**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="044a6-104">The **Abort** method aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="044a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="044a6-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="044a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="044a6-106">Parameters</span></span>

<span data-ttu-id="044a6-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="044a6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="044a6-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="044a6-108">Return value</span></span>

<span data-ttu-id="044a6-109">La valeur de retour est **S \_ OK** en cas de réussite ou une valeur d’erreur dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="044a6-109">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="044a6-110">Notes</span><span class="sxs-lookup"><span data-stu-id="044a6-110">Remarks</span></span>

<span data-ttu-id="044a6-111">Vous pouvez abandonner à la fois les méthodes d' [**envoi**](iwinhttprequest-send.md) asynchrones et synchrones.</span><span class="sxs-lookup"><span data-stu-id="044a6-111">You can abort both asynchronous and synchronous [**Send**](iwinhttprequest-send.md) methods.</span></span> <span data-ttu-id="044a6-112">Pour abandonner une méthode d' [**envoi**](iwinhttprequest-send.md) synchrone, vous devez appeler **Abort** à partir d’un événement [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="044a6-112">To abort a synchronous [**Send**](iwinhttprequest-send.md) method, you must call **Abort** from within an [**IWinHttpRequestEvents**](iwinhttprequestevents-interface.md) event.</span></span>

> [!Note]  
> <span data-ttu-id="044a6-113">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="044a6-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="044a6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="044a6-114">Requirements</span></span>



| <span data-ttu-id="044a6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="044a6-115">Requirement</span></span> | <span data-ttu-id="044a6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="044a6-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="044a6-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="044a6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="044a6-118">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="044a6-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="044a6-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="044a6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="044a6-120">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="044a6-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="044a6-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="044a6-121">Redistributable</span></span><br/>          | <span data-ttu-id="044a6-122">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="044a6-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="044a6-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="044a6-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="044a6-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="044a6-124"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="044a6-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="044a6-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="044a6-126"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="044a6-126"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="044a6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="044a6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="044a6-128"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="044a6-128"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="044a6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="044a6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044a6-130">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="044a6-130">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="044a6-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="044a6-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="044a6-132">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="044a6-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




