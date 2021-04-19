---
description: 'La méthode CheckCapabilities interroge si un flux a spécifié des fonctionnalités de recherche. Cette méthode implémente la méthode IMediaSeeking :: CheckCapabilities.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Méthode CPosPassThru. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528863"
---
# <a name="cpospassthrucheckcapabilities-method"></a><span data-ttu-id="9a4d1-104">Méthode CPosPassThru. CheckCapabilities</span><span class="sxs-lookup"><span data-stu-id="9a4d1-104">CPosPassThru.CheckCapabilities method</span></span>

<span data-ttu-id="9a4d1-105">La `CheckCapabilities` méthode interroge si un flux a spécifié des fonctionnalités de recherche.</span><span class="sxs-lookup"><span data-stu-id="9a4d1-105">The `CheckCapabilities` method queries whether a stream has specified seeking capabilities.</span></span> <span data-ttu-id="9a4d1-106">Cette méthode implémente la méthode [**IMediaSeeking :: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="9a4d1-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a4d1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a4d1-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="9a4d1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a4d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a4d1-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="9a4d1-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="9a4d1-110">Pointeur vers une combinaison d’opérations de bits d’un ou de plusieurs attributs de [**\_ \_ \_ capacités de recherche**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) de recherche.</span><span class="sxs-lookup"><span data-stu-id="9a4d1-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span> <span data-ttu-id="9a4d1-111">Lorsque la méthode retourne, la valeur indique quels attributs sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="9a4d1-111">When the method returns, the value indicates which of those attributes are available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a4d1-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a4d1-112">Return value</span></span>

<span data-ttu-id="9a4d1-113">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="9a4d1-113">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a4d1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a4d1-114">Requirements</span></span>



| <span data-ttu-id="9a4d1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a4d1-115">Requirement</span></span> | <span data-ttu-id="9a4d1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a4d1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a4d1-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a4d1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9a4d1-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a4d1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9a4d1-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a4d1-119">Library</span></span><br/> | <dl> <span data-ttu-id="9a4d1-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9a4d1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a4d1-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a4d1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a4d1-122">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="9a4d1-122">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




