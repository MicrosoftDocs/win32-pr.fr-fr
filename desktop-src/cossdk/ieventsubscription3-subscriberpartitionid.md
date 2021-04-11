---
description: GUID de la partition de l’abonné.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'IEventSubscription3 :: SubscriberPartitionID, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201122"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a><span data-ttu-id="4b361-103">IEventSubscription3 :: SubscriberPartitionID, propriété</span><span class="sxs-lookup"><span data-stu-id="4b361-103">IEventSubscription3::SubscriberPartitionID property</span></span>

<span data-ttu-id="4b361-104">GUID de la partition de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="4b361-104">The partition GUID of the subscriber.</span></span>

<span data-ttu-id="4b361-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4b361-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b361-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b361-106">Syntax</span></span>


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="4b361-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4b361-107">Property value</span></span>

<span data-ttu-id="4b361-108">Chaîne contenant le GUID de la partition de l’abonné.</span><span class="sxs-lookup"><span data-stu-id="4b361-108">A string containing the GUID of the subscriber partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b361-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4b361-109">Error codes</span></span>

<span data-ttu-id="4b361-110">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4b361-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b361-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b361-111">Requirements</span></span>



| <span data-ttu-id="4b361-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b361-112">Requirement</span></span> | <span data-ttu-id="4b361-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b361-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4b361-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b361-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4b361-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b361-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4b361-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4b361-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4b361-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4b361-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4b361-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b361-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b361-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="4b361-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




