---
description: Objet d’assistance pour passer les commandes de recherche en amont.
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
ms.openlocfilehash: dc98e439d7f6a2d6c6392ffb665b04e502047eb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531023"
---
# <a name="ctransformoutputpinm_pposition-member"></a><span data-ttu-id="71b91-103">CTransformOutputPin :: m \_ pPosition, membre</span><span class="sxs-lookup"><span data-stu-id="71b91-103">CTransformOutputPin::m\_pPosition member</span></span>

<span data-ttu-id="71b91-104">Objet d’assistance pour passer les commandes de recherche en amont.</span><span class="sxs-lookup"><span data-stu-id="71b91-104">Helper object to pass seek commands upstream.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b91-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71b91-105">Syntax</span></span>


```C++
IUnknown *m_pPosition;
```



## <a name="remarks"></a><span data-ttu-id="71b91-106">Notes</span><span class="sxs-lookup"><span data-stu-id="71b91-106">Remarks</span></span>

<span data-ttu-id="71b91-107">Lorsque le code PIN est demandé pour la première fois pour l’interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) ou [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , il crée et agrège un objet d’assistance [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="71b91-107">When the pin is first queried for the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) or [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, it creates and aggregates a [**CPosPassThru**](cpospassthru.md) helper object.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b91-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71b91-108">Requirements</span></span>



| <span data-ttu-id="71b91-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71b91-109">Requirement</span></span> | <span data-ttu-id="71b91-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="71b91-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71b91-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="71b91-111">Header</span></span><br/>  | <dl> <span data-ttu-id="71b91-112"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="71b91-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71b91-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71b91-113">Library</span></span><br/> | <dl> <span data-ttu-id="71b91-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="71b91-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




