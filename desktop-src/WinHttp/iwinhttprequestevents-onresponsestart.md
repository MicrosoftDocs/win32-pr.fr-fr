---
description: Se produit lorsque les données de réponse commencent à être reçues.
ms.assetid: 7245725b-40dd-4282-b681-f0b2c191db94
title: 'Événement IWinHttpRequestEvents :: OnResponseStart'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a299c535dd854bff07f2c24989096f7b9e49fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534603"
---
# <a name="iwinhttprequesteventsonresponsestart-event"></a><span data-ttu-id="303bb-103">Événement IWinHttpRequestEvents :: OnResponseStart</span><span class="sxs-lookup"><span data-stu-id="303bb-103">IWinHttpRequestEvents::OnResponseStart event</span></span>

<span data-ttu-id="303bb-104">L’événement **OnResponseStart** se produit lorsque les données de réponse commencent à être reçues.</span><span class="sxs-lookup"><span data-stu-id="303bb-104">The **OnResponseStart** event occurs when the response data starts to be received.</span></span>

## <a name="syntax"></a><span data-ttu-id="303bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="303bb-105">Syntax</span></span>


```C++
void OnResponseStart(
  [in] long Status,
  [in] BSTR ContentType
);
```



## <a name="parameters"></a><span data-ttu-id="303bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="303bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303bb-107">*État* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="303bb-107">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303bb-108">Reçoit le code d’état standard retourné avec les données de réponse.</span><span class="sxs-lookup"><span data-stu-id="303bb-108">Receives the standard status code returned with the response data.</span></span> <span data-ttu-id="303bb-109">Les codes d’État sont définis dans le [document RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="303bb-109">Status codes are defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

</dd> <dt>

<span data-ttu-id="303bb-110">*ContentType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="303bb-110">*ContentType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="303bb-111">Spécifie le type de contenu reçu, par exemple « text/html » ou « image/GIF ».</span><span class="sxs-lookup"><span data-stu-id="303bb-111">Specifies the type of content received, such as "text/html" or "image/gif".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303bb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="303bb-112">Return value</span></span>

<span data-ttu-id="303bb-113">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="303bb-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="303bb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="303bb-114">Remarks</span></span>

<span data-ttu-id="303bb-115">Pour que cet événement se produise, utilisez [**Open**](iwinhttprequest-open.md) pour envoyer une connexion http en mode asynchrone et utilisez [**Send**](iwinhttprequest-send.md) pour envoyer une demande de données à un serveur Internet.</span><span class="sxs-lookup"><span data-stu-id="303bb-115">For this event to occur, use [**Open**](iwinhttprequest-open.md) to send an HTTP connection in asynchronous mode and use [**Send**](iwinhttprequest-send.md) to send a data request to an Internet server.</span></span>

<span data-ttu-id="303bb-116">Il s’agit du premier événement WinHTTP qui se produit après l' [**envoi**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="303bb-116">This is the first WinHTTP event to occur after the [**Send**](iwinhttprequest-send.md).</span></span>

> [!Note]  
> <span data-ttu-id="303bb-117">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="303bb-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="303bb-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="303bb-118">Requirements</span></span>



| <span data-ttu-id="303bb-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="303bb-119">Requirement</span></span> | <span data-ttu-id="303bb-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="303bb-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="303bb-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="303bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="303bb-122">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="303bb-122">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="303bb-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="303bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="303bb-124">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="303bb-124">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="303bb-125">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="303bb-125">Redistributable</span></span><br/>          | <span data-ttu-id="303bb-126">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="303bb-126">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="303bb-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="303bb-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="303bb-128"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="303bb-128"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="303bb-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="303bb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="303bb-130">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="303bb-130">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="303bb-131">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="303bb-131">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="303bb-132">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="303bb-132">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




