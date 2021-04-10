---
description: GUID de l’application de l’abonné.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: 'IEventSubscription3 :: SubscriberApplicationID, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200957"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a><span data-ttu-id="7caf9-103">IEventSubscription3 :: SubscriberApplicationID, propriété</span><span class="sxs-lookup"><span data-stu-id="7caf9-103">IEventSubscription3::SubscriberApplicationID property</span></span>

<span data-ttu-id="7caf9-104">GUID de l’application de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="7caf9-104">The application GUID of the subscriber.</span></span>

<span data-ttu-id="7caf9-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7caf9-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7caf9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7caf9-106">Syntax</span></span>


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="7caf9-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="7caf9-107">Property value</span></span>

<span data-ttu-id="7caf9-108">Chaîne contenant le GUID de l’application de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="7caf9-108">A string containing the GUID of the subscriber application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7caf9-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7caf9-109">Error codes</span></span>

<span data-ttu-id="7caf9-110">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7caf9-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="7caf9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7caf9-111">Requirements</span></span>



| <span data-ttu-id="7caf9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7caf9-112">Requirement</span></span> | <span data-ttu-id="7caf9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7caf9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7caf9-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7caf9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7caf9-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7caf9-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7caf9-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7caf9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7caf9-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7caf9-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7caf9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7caf9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7caf9-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="7caf9-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




