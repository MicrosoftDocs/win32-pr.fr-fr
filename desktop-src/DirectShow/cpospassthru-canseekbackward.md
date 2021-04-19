---
description: 'La méthode CanSeekBackward détermine si le flux peut être recherché en arrière. Cette méthode implémente la méthode IMediaPosition :: CanSeekBackward.'
ms.assetid: 6443980f-6863-4941-b2dd-4a31257b5810
title: Méthode CPosPassThru. CanSeekBackward (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CanSeekBackward
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a016f5cfeea7ca1e63bb4d0e603784b8f95a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540203"
---
# <a name="cpospassthrucanseekbackward-method"></a><span data-ttu-id="08758-104">Méthode CPosPassThru. CanSeekBackward</span><span class="sxs-lookup"><span data-stu-id="08758-104">CPosPassThru.CanSeekBackward method</span></span>

<span data-ttu-id="08758-105">La `CanSeekBackward` méthode détermine si le flux peut être recherché en arrière.</span><span class="sxs-lookup"><span data-stu-id="08758-105">The `CanSeekBackward` method determines whether the stream can be seeked backward.</span></span> <span data-ttu-id="08758-106">Cette méthode implémente la méthode [**IMediaPosition :: CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) .</span><span class="sxs-lookup"><span data-stu-id="08758-106">This method implements the [**IMediaPosition::CanSeekBackward**](/windows/desktop/api/Control/nf-control-imediaposition-canseekbackward) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="08758-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08758-107">Syntax</span></span>


```C++
HRESULT CanSeekBackward(
   LONG *pCanSeekBackward
);
```



## <a name="parameters"></a><span data-ttu-id="08758-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08758-109">*pCanSeekBackward*</span><span class="sxs-lookup"><span data-stu-id="08758-109">*pCanSeekBackward*</span></span> 
</dt> <dd>

<span data-ttu-id="08758-110">Pointeur vers une variable qui reçoit la valeur OATRUE si le filtre peut effectuer une recherche vers l’arrière, ou OAFALSE dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="08758-110">Pointer to a variable that receives the value OATRUE if the filter can seek backward, or OAFALSE otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08758-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08758-111">Return value</span></span>

<span data-ttu-id="08758-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="08758-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="08758-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08758-113">Requirements</span></span>



| <span data-ttu-id="08758-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08758-114">Requirement</span></span> | <span data-ttu-id="08758-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="08758-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08758-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="08758-116">Header</span></span><br/>  | <dl> <span data-ttu-id="08758-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08758-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="08758-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="08758-118">Library</span></span><br/> | <dl> <span data-ttu-id="08758-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="08758-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08758-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08758-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08758-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="08758-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




