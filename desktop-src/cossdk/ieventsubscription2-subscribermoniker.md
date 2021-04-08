---
description: Moniker des abonnés.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: Propriété IEventSubscription2SubscriberMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748301"
---
# <a name="ieventsubscription2subscribermoniker-property"></a><span data-ttu-id="b5c45-103">IEventSubscription2 :: SubscriberMoniker, propriété</span><span class="sxs-lookup"><span data-stu-id="b5c45-103">IEventSubscription2::SubscriberMoniker property</span></span>

<span data-ttu-id="b5c45-104">Moniker de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="b5c45-104">The subscriber's moniker.</span></span>

<span data-ttu-id="b5c45-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b5c45-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5c45-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5c45-106">Syntax</span></span>


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a><span data-ttu-id="b5c45-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b5c45-107">Property value</span></span>

<span data-ttu-id="b5c45-108">Chaîne de moniker spécifiant l’abonné.</span><span class="sxs-lookup"><span data-stu-id="b5c45-108">A moniker string specifying the subscriber.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5c45-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b5c45-109">Error codes</span></span>

<span data-ttu-id="b5c45-110">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5c45-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5c45-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5c45-111">Requirements</span></span>



| <span data-ttu-id="b5c45-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5c45-112">Requirement</span></span> | <span data-ttu-id="b5c45-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5c45-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b5c45-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5c45-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b5c45-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5c45-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b5c45-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5c45-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b5c45-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5c45-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b5c45-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5c45-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c45-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="b5c45-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




