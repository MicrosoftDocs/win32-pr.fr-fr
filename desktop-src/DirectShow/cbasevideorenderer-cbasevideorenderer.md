---
description: Méthode constructeur CBaseVideoRenderer. CBaseVideoRenderer.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Constructeur CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095837"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="547ec-103">Constructeur CBaseVideoRenderer. CBaseVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="547ec-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="547ec-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="547ec-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="547ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="547ec-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="547ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="547ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="547ec-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="547ec-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="547ec-108">Identificateur de classe pour ce convertisseur.</span><span class="sxs-lookup"><span data-stu-id="547ec-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="547ec-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="547ec-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="547ec-110">Pointeur vers une description utilisée à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="547ec-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="547ec-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="547ec-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="547ec-112">Pointeur vers l’objet propriétaire agrégé.</span><span class="sxs-lookup"><span data-stu-id="547ec-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="547ec-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="547ec-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="547ec-114">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="547ec-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="547ec-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="547ec-115">Requirements</span></span>



| <span data-ttu-id="547ec-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="547ec-116">Requirement</span></span> | <span data-ttu-id="547ec-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="547ec-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="547ec-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="547ec-118">Header</span></span><br/>  | <dl> <span data-ttu-id="547ec-119"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="547ec-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="547ec-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="547ec-120">Library</span></span><br/> | <dl> <span data-ttu-id="547ec-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="547ec-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="547ec-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="547ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="547ec-123">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="547ec-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




