---
description: Critères de filtre régissant l’abonnement.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'IEventSubscription2 :: FilterCriteria, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111291"
---
# <a name="ieventsubscription2filtercriteria-property"></a><span data-ttu-id="8b383-103">IEventSubscription2 :: FilterCriteria, propriété</span><span class="sxs-lookup"><span data-stu-id="8b383-103">IEventSubscription2::FilterCriteria property</span></span>

<span data-ttu-id="8b383-104">Critères de filtre régissant l’abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b383-104">The filter criteria governing the subscription.</span></span>

<span data-ttu-id="8b383-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8b383-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b383-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b383-106">Syntax</span></span>


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a><span data-ttu-id="8b383-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8b383-107">Property value</span></span>

<span data-ttu-id="8b383-108">Les critères de filtre ou le CLSID d’une classe qui implémente [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span><span class="sxs-lookup"><span data-stu-id="8b383-108">The filter criteria or the CLSID for a class implementing [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b383-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8b383-109">Error codes</span></span>

<span data-ttu-id="8b383-110">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8b383-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b383-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b383-111">Requirements</span></span>



| <span data-ttu-id="8b383-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b383-112">Requirement</span></span> | <span data-ttu-id="8b383-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b383-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8b383-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b383-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8b383-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b383-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8b383-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b383-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8b383-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b383-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8b383-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b383-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b383-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="8b383-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




