---
description: Se produit lorsque des données sont disponibles à partir de la réponse.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Événement IWinHttpRequestEvents :: OnResponseDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519378"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a><span data-ttu-id="95328-103">Événement IWinHttpRequestEvents :: OnResponseDataAvailable</span><span class="sxs-lookup"><span data-stu-id="95328-103">IWinHttpRequestEvents::OnResponseDataAvailable event</span></span>

<span data-ttu-id="95328-104">L’événement **OnResponseDataAvailable** se produit lorsque des données sont disponibles à partir de la réponse.</span><span class="sxs-lookup"><span data-stu-id="95328-104">The **OnResponseDataAvailable** event occurs when data is available from the response.</span></span>

## <a name="syntax"></a><span data-ttu-id="95328-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95328-105">Syntax</span></span>


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a><span data-ttu-id="95328-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95328-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95328-107">*Données* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="95328-107">*Data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95328-108">Tableau de base zéro d’octets qui reçoit les données de réponse reçues par les services HTTP Microsoft Windows (WinHTTP) jusqu’au point que cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="95328-108">A zero-based array of bytes that receives the response data received by Microsoft Windows HTTP Services (WinHTTP) up to the point that this event occurs.</span></span> <span data-ttu-id="95328-109">Il s’agit d’une **variante** de type VT \_ array \| VT \_ UI1.</span><span class="sxs-lookup"><span data-stu-id="95328-109">This is a **VARIANT** of type VT\_ARRAY \| VT\_UI1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95328-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="95328-110">Return value</span></span>

<span data-ttu-id="95328-111">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="95328-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95328-112">Notes</span><span class="sxs-lookup"><span data-stu-id="95328-112">Remarks</span></span>

<span data-ttu-id="95328-113">Comme les données sont en octets, elles doivent être converties en caractères larges lorsqu’elles sont placées dans une chaîne à caractères larges (Unicode).</span><span class="sxs-lookup"><span data-stu-id="95328-113">Because data is in bytes, it must be converted to wide characters when placed in a wide character (Unicode) string.</span></span>

> [!Note]  
> <span data-ttu-id="95328-114">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="95328-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95328-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95328-115">Requirements</span></span>



| <span data-ttu-id="95328-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95328-116">Requirement</span></span> | <span data-ttu-id="95328-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="95328-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="95328-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95328-118">Minimum supported client</span></span><br/> | <span data-ttu-id="95328-119">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95328-119">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="95328-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="95328-120">Minimum supported server</span></span><br/> | <span data-ttu-id="95328-121">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="95328-121">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="95328-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="95328-122">Redistributable</span></span><br/>          | <span data-ttu-id="95328-123">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="95328-123">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="95328-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="95328-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="95328-125"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="95328-125"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95328-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95328-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95328-127">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="95328-127">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="95328-128">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="95328-128">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="95328-129">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="95328-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




