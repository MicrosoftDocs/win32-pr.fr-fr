---
description: Se produit lorsque les données de réponse sont terminées.
ms.assetid: 0df2031e-826f-436e-a689-201fa8b5c38f
title: 'Événement IWinHttpRequestEvents :: OnResponseFinished'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d3a596e23028cec0401a21a1ee866ef6e51d9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530876"
---
# <a name="iwinhttprequesteventsonresponsefinished-event"></a><span data-ttu-id="35c03-103">Événement IWinHttpRequestEvents :: OnResponseFinished</span><span class="sxs-lookup"><span data-stu-id="35c03-103">IWinHttpRequestEvents::OnResponseFinished event</span></span>

<span data-ttu-id="35c03-104">L’événement **OnResponseFinished** se produit lorsque les données de réponse sont terminées.</span><span class="sxs-lookup"><span data-stu-id="35c03-104">The **OnResponseFinished** event occurs when the response data is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c03-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35c03-105">Syntax</span></span>


```C++
void OnResponseFinished();
```



## <a name="parameters"></a><span data-ttu-id="35c03-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35c03-106">Parameters</span></span>

<span data-ttu-id="35c03-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="35c03-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="35c03-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35c03-108">Return value</span></span>

<span data-ttu-id="35c03-109">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="35c03-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35c03-110">Notes</span><span class="sxs-lookup"><span data-stu-id="35c03-110">Remarks</span></span>

<span data-ttu-id="35c03-111">Cet événement signale que toutes les données de réponse relatives à la demande la plus récente ont été reçues.</span><span class="sxs-lookup"><span data-stu-id="35c03-111">This event signals that all of the response data that pertains to the most recent request has been received.</span></span> <span data-ttu-id="35c03-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) ne se reproduit pas jusqu’à la requête suivante.</span><span class="sxs-lookup"><span data-stu-id="35c03-112">[**OnResponseDataAvailable**](iwinhttprequestevents-onresponsedataavailable.md) does not occur again until the next request.</span></span>

> [!Note]  
> <span data-ttu-id="35c03-113">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="35c03-113">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35c03-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35c03-114">Requirements</span></span>



| <span data-ttu-id="35c03-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35c03-115">Requirement</span></span> | <span data-ttu-id="35c03-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="35c03-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c03-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35c03-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35c03-118">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35c03-118">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="35c03-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35c03-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35c03-120">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35c03-120">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="35c03-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="35c03-121">Redistributable</span></span><br/>          | <span data-ttu-id="35c03-122">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="35c03-122">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="35c03-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="35c03-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="35c03-124"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="35c03-124"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35c03-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35c03-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c03-126">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="35c03-126">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="35c03-127">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="35c03-127">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="35c03-128">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="35c03-128">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




