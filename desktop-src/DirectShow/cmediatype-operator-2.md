---
description: Cet opérateur surcharge l’opérateur d’assignation pour copier un type de média.
ms.assetid: 5b94191d-b5e4-42b2-b0c5-8c2da2483c54
title: 'CMediaType. CMediaType :: Operator =, méthode (mtype. h)-mtype, paramètre'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa577c8c8cfcdbcb0b62287a80cd998ab8775c6
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "106541574"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh"></a><span data-ttu-id="23ade-103">CMediaType. CMediaType :: Operator =, méthode (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="23ade-103">CMediaType.CMediaType::operator= method (Mtype.h)</span></span>

<span data-ttu-id="23ade-104">Cet opérateur surcharge l’opérateur d’assignation pour copier un type de média.</span><span class="sxs-lookup"><span data-stu-id="23ade-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="23ade-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23ade-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="23ade-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23ade-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23ade-107">*mtype* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="23ade-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="23ade-108">Référence à une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="23ade-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23ade-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23ade-109">Return value</span></span>

<span data-ttu-id="23ade-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="23ade-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="23ade-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23ade-111">Requirements</span></span>



| <span data-ttu-id="23ade-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23ade-112">Requirement</span></span> | <span data-ttu-id="23ade-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="23ade-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23ade-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="23ade-114">Header</span></span><br/>  | <dl> <span data-ttu-id="23ade-115"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23ade-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="23ade-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="23ade-116">Library</span></span><br/> | <dl> <span data-ttu-id="23ade-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="23ade-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ade-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23ade-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ade-119">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="23ade-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




