---
description: La méthode SetAbortSignal définit un indicateur qui indique s’il faut arrêter le rendu et rejeter d’autres exemples.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Méthode CBaseRenderer. SetAbortSignal (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530329"
---
# <a name="cbaserenderersetabortsignal-method"></a><span data-ttu-id="af6d0-103">Méthode CBaseRenderer. SetAbortSignal</span><span class="sxs-lookup"><span data-stu-id="af6d0-103">CBaseRenderer.SetAbortSignal method</span></span>

<span data-ttu-id="af6d0-104">La `SetAbortSignal` méthode définit un indicateur qui indique s’il faut arrêter le rendu et rejeter d’autres exemples.</span><span class="sxs-lookup"><span data-stu-id="af6d0-104">The `SetAbortSignal` method sets a flag which indicates whether to stop rendering and reject further samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af6d0-105">Syntax</span></span>


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a><span data-ttu-id="af6d0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af6d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af6d0-107">*bAbort*</span><span class="sxs-lookup"><span data-stu-id="af6d0-107">*bAbort*</span></span> 
</dt> <dd>

<span data-ttu-id="af6d0-108">Valeur booléenne indiquant s’il faut arrêter le rendu.</span><span class="sxs-lookup"><span data-stu-id="af6d0-108">Boolean value indicating whether to stop rendering.</span></span> <span data-ttu-id="af6d0-109">Si la **valeur est true**, le filtre n’affiche plus d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="af6d0-109">If **TRUE**, the filter will not render any more samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af6d0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af6d0-110">Return value</span></span>

<span data-ttu-id="af6d0-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="af6d0-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af6d0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="af6d0-112">Remarks</span></span>

<span data-ttu-id="af6d0-113">Cette méthode définit l’indicateur [**CBaseRenderer :: m \_ bAbort**](cbaserenderer-m-babort.md) .</span><span class="sxs-lookup"><span data-stu-id="af6d0-113">This method sets the [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6d0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af6d0-114">Requirements</span></span>



| <span data-ttu-id="af6d0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af6d0-115">Requirement</span></span> | <span data-ttu-id="af6d0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="af6d0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af6d0-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="af6d0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="af6d0-118"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="af6d0-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af6d0-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="af6d0-119">Library</span></span><br/> | <dl> <span data-ttu-id="af6d0-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="af6d0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af6d0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af6d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af6d0-122">**CBaseRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="af6d0-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




