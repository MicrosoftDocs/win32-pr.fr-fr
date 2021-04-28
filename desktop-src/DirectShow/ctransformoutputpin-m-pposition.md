---
description: 'CTransformOutputPin :: m_pPosition objet d’assistance de membre pour passer les commandes de recherche en amont.'
ms.assetid: 2ca9bae7-a133-4e09-8aa7-1c4601ec5db0
title: 'Membre CTransformOutputPin :: m_pPosition (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pPosition
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9c5a1b5d5ced7a9f3985ceebdd2bdcb8e491d2e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084857"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="95155-103">CTransformOutputPin :: m \_ pPosition, membre</span><span class="sxs-lookup"><span data-stu-id="95155-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="95155-104">Objet d’assistance pour passer les commandes de recherche en amont.</span><span class="sxs-lookup"><span data-stu-id="95155-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="95155-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95155-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="95155-106">Notes </span><span class="sxs-lookup"><span data-stu-id="95155-106">Remarks</span></span>

<span data-ttu-id="95155-107">Lorsque le code PIN est demandé pour la première fois pour l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) ou [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , il crée et agrège un objet d’assistance [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="95155-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="95155-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95155-108">Requirements</span></span>



| <span data-ttu-id="95155-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95155-109">Requirement</span></span> | <span data-ttu-id="95155-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="95155-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95155-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="95155-111">Header</span></span><br/>  | <dl> <span data-ttu-id="95155-112"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95155-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95155-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95155-113">Library</span></span><br/> | <dl> <span data-ttu-id="95155-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="95155-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




