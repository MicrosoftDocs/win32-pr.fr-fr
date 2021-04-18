---
description: GUID de la partition de l’objet de classe d’événements.
ms.assetid: 154849ac-350c-4b2f-bb51-ac6973f0a8fa
title: 'IEventSubscription3 :: EventClassPartitionID, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.EventClassPartitionID
- IEventSubscription3.get_EventClassPartitionID
- IEventSubscription3.put_EventClassPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: d41d3e2a170deffb73f1f533226421d88f150c01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524204"
---
# <a name="ieventsubscription3eventclasspartitionid-property"></a><span data-ttu-id="3ff7c-103">IEventSubscription3 :: EventClassPartitionID, propriété</span><span class="sxs-lookup"><span data-stu-id="3ff7c-103">IEventSubscription3::EventClassPartitionID property</span></span>

<span data-ttu-id="3ff7c-104">GUID de la partition de l’objet de classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="3ff7c-104">The partition GUID of the event class object.</span></span>

<span data-ttu-id="3ff7c-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3ff7c-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ff7c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ff7c-106">Syntax</span></span>


```C++
HRESULT put_EventClassPartitionID(
  [in]          BSTR bstrEventClassPartitionID
);

HRESULT get_EventClassPartitionID(
  [out, retval] BSTR *pbstrEventClassPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="3ff7c-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3ff7c-107">Property value</span></span>

<span data-ttu-id="3ff7c-108">Chaîne contenant le GUID de la partition de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="3ff7c-108">A string containing the GUID of the event class partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3ff7c-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="3ff7c-109">Error codes</span></span>

<span data-ttu-id="3ff7c-110">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inattendue, e \_ Fail et S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3ff7c-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ff7c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ff7c-111">Requirements</span></span>



| <span data-ttu-id="3ff7c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ff7c-112">Requirement</span></span> | <span data-ttu-id="3ff7c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ff7c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3ff7c-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ff7c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3ff7c-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ff7c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3ff7c-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ff7c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3ff7c-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ff7c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3ff7c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ff7c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ff7c-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="3ff7c-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




