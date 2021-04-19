---
description: 'Indicateur de remplacement du traitement par lots. L’affectation de la valeur TRUE à cet indicateur remplace l’indicateur COutputQueue :: m \_ bBatchExact et remet tous les exemples en attente.'
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: 'Membre COutputQueue :: m_bSendAnyway (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57019ee8844f73fdb6cf6e7943e7e22f72d2c98b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537965"
---
# <a name="coutputqueuem_bsendanyway-member"></a><span data-ttu-id="dd7a2-104">COutputQueue :: m \_ bSendAnyway, membre</span><span class="sxs-lookup"><span data-stu-id="dd7a2-104">COutputQueue::m\_bSendAnyway member</span></span>

<span data-ttu-id="dd7a2-105">Indicateur de remplacement du traitement par lots.</span><span class="sxs-lookup"><span data-stu-id="dd7a2-105">Flag to override batch processing.</span></span> <span data-ttu-id="dd7a2-106">L’affectation de la **valeur true** à cet indicateur remplace l’indicateur [**COutputQueue :: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) et remet tous les exemples en attente.</span><span class="sxs-lookup"><span data-stu-id="dd7a2-106">Setting this flag to **TRUE** overrides the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) flag and delivers all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd7a2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd7a2-107">Syntax</span></span>


```C++
BOOL m_bSendAnyway;
```



## <a name="requirements"></a><span data-ttu-id="dd7a2-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd7a2-108">Requirements</span></span>



| <span data-ttu-id="dd7a2-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd7a2-109">Requirement</span></span> | <span data-ttu-id="dd7a2-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd7a2-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7a2-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd7a2-111">Header</span></span><br/>  | <dl> <span data-ttu-id="dd7a2-112"><dt>Outputq. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd7a2-112"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd7a2-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd7a2-113">Library</span></span><br/> | <dl> <span data-ttu-id="dd7a2-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dd7a2-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd7a2-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd7a2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd7a2-116">**COutputQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="dd7a2-116">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




