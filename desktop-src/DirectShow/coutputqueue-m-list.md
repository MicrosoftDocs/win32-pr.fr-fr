---
description: File d’attente de l’exemple de support.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Membre COutputQueue :: m_List (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537513"
---
# <a name="coutputqueuem_list-member"></a><span data-ttu-id="f00ef-103">COutputQueue :: m \_ List, membre</span><span class="sxs-lookup"><span data-stu-id="f00ef-103">COutputQueue::m\_List member</span></span>

<span data-ttu-id="f00ef-104">File d’attente de l’exemple de support.</span><span class="sxs-lookup"><span data-stu-id="f00ef-104">Media sample queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="f00ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f00ef-105">Syntax</span></span>


```C++
CSampleList *m_List;
```



## <a name="remarks"></a><span data-ttu-id="f00ef-106">Notes</span><span class="sxs-lookup"><span data-stu-id="f00ef-106">Remarks</span></span>

<span data-ttu-id="f00ef-107">Cette variable membre est un pointeur vers un objet [**CGenericList**](cgenericlist.md) qui contient des pointeurs [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="f00ef-107">This member variable is a pointer to a [**CGenericList**](cgenericlist.md) object that holds [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointers.</span></span> <span data-ttu-id="f00ef-108">Le type **CSampleList** est défini comme suit :</span><span class="sxs-lookup"><span data-stu-id="f00ef-108">The **CSampleList** type is defined as follows:</span></span>

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a><span data-ttu-id="f00ef-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f00ef-109">Requirements</span></span>



| <span data-ttu-id="f00ef-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f00ef-110">Requirement</span></span> | <span data-ttu-id="f00ef-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f00ef-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f00ef-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="f00ef-112">Header</span></span><br/>  | <dl> <span data-ttu-id="f00ef-113"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f00ef-113"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f00ef-114">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f00ef-114">Library</span></span><br/> | <dl> <span data-ttu-id="f00ef-115"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f00ef-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f00ef-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f00ef-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f00ef-117">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="f00ef-117">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




