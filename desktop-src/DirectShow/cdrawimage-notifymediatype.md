---
description: La méthode NotifyMediaType avertit l’objet CDrawImage du type de média actuel.
ms.assetid: 419d516f-4b96-47aa-80cc-ac785e65af8b
title: Méthode CDrawImage. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e3af4d926bd0ca8db5ef11839dd0ca84523c374
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533197"
---
# <a name="cdrawimagenotifymediatype-method"></a><span data-ttu-id="1c832-103">Méthode CDrawImage. NotifyMediaType</span><span class="sxs-lookup"><span data-stu-id="1c832-103">CDrawImage.NotifyMediaType method</span></span>

<span data-ttu-id="1c832-104">La `NotifyMediaType` méthode notifie l’objet **CDrawImage** du type de média actuel.</span><span class="sxs-lookup"><span data-stu-id="1c832-104">The `NotifyMediaType` method notifies the **CDrawImage** object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c832-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c832-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="1c832-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c832-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c832-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="1c832-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="1c832-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) , ou **null** pour effacer le type de média.</span><span class="sxs-lookup"><span data-stu-id="1c832-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c832-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c832-109">Return value</span></span>

<span data-ttu-id="1c832-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1c832-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c832-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1c832-111">Remarks</span></span>

<span data-ttu-id="1c832-112">Le filtre propriétaire doit appeler cette méthode chaque fois que le type de média change.</span><span class="sxs-lookup"><span data-stu-id="1c832-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="1c832-113">En général, cela se produit lorsque le code confidentiel se connecte pour la première fois et après une modification de format dynamique.</span><span class="sxs-lookup"><span data-stu-id="1c832-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span>

<span data-ttu-id="1c832-114">L’objet **CDrawImage** stocke le pointeur *pMediaType* dans la variable membre **m \_ pMediaType** .</span><span class="sxs-lookup"><span data-stu-id="1c832-114">The **CDrawImage** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="1c832-115">Par conséquent, si l’appelant doit libérer l’objet **CMediaType** , il doit mettre à jour l’objet **CDrawImage** en appelant à nouveau cette méthode, soit avec un nouveau pointeur, soit avec une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="1c832-115">Therefore, if the caller needs to release the **CMediaType** object, it should update the **CDrawImage** object by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="1c832-116">Dans le cas contraire, une erreur peut se produire lorsque l’objet **CDrawImage** tente de faire référence à l’ancien pointeur.</span><span class="sxs-lookup"><span data-stu-id="1c832-116">Otherwise, an error can occur when the **CDrawImage** object attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c832-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c832-117">Requirements</span></span>



| <span data-ttu-id="1c832-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c832-118">Requirement</span></span> | <span data-ttu-id="1c832-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c832-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c832-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c832-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1c832-121"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c832-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c832-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c832-122">Library</span></span><br/> | <dl> <span data-ttu-id="1c832-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c832-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c832-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c832-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c832-125">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="1c832-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




