---
description: Se produit lorsqu’une erreur d’exécution se produit dans l’application.
ms.assetid: d99400a4-3661-4162-bfd6-8c2a27e0f328
title: 'IWinHttpRequestEvents :: OnError, événement'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8582deec90eb6bfc2985460f3127d5c7ee9c01b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952939"
---
# <a name="iwinhttprequesteventsonerror-event"></a><span data-ttu-id="816b8-103">IWinHttpRequestEvents :: OnError, événement</span><span class="sxs-lookup"><span data-stu-id="816b8-103">IWinHttpRequestEvents::OnError event</span></span>

<span data-ttu-id="816b8-104">L’événement **OnError** se produit lorsqu’une erreur d’exécution se produit dans l’application.</span><span class="sxs-lookup"><span data-stu-id="816b8-104">The **OnError** event occurs when there is a run-time error in the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="816b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="816b8-105">Syntax</span></span>


```C++
void OnError(
  [in] long ErrorNumber,
  [in] BSTR ErrorDescription
);
```



## <a name="parameters"></a><span data-ttu-id="816b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="816b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="816b8-107">*Errornumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="816b8-107">*ErrorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="816b8-108">Reçoit la valeur numérique de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="816b8-108">Receives the numerical value of the error.</span></span> <span data-ttu-id="816b8-109">Les 16 bits inférieurs de ce numéro d’erreur correspondent à l’une des erreurs figurant dans les [**messages d’erreur**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="816b8-109">The lower 16 bits of this error number corresponds to one of the errors listed in [**Error Messages**](error-messages.md).</span></span>

</dd> <dt>

<span data-ttu-id="816b8-110">*ErrorDescription* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="816b8-110">*ErrorDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="816b8-111">Spécifie une brève description de l’erreur qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="816b8-111">Specifies a short description of the error which occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="816b8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="816b8-112">Return value</span></span>

<span data-ttu-id="816b8-113">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="816b8-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="816b8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="816b8-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="816b8-115">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="816b8-115">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="816b8-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="816b8-116">Requirements</span></span>



| <span data-ttu-id="816b8-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="816b8-117">Requirement</span></span> | <span data-ttu-id="816b8-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="816b8-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="816b8-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="816b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="816b8-120">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="816b8-120">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="816b8-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="816b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="816b8-122">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="816b8-122">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="816b8-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="816b8-123">Redistributable</span></span><br/>          | <span data-ttu-id="816b8-124">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="816b8-124">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="816b8-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="816b8-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="816b8-126"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="816b8-126"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="816b8-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="816b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="816b8-128">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="816b8-128">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="816b8-129">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="816b8-129">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="816b8-130">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="816b8-130">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




