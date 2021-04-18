---
description: La méthode NotifyMediaType informe l’objet du type de média actuel.
ms.assetid: 6fb708ff-e968-4867-baca-ebe2515c9fab
title: Méthode CImageAllocator. NotifyMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.NotifyMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9261884b8940b571876502741fcc52e1c40a33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533406"
---
# <a name="cimageallocatornotifymediatype-method"></a><span data-ttu-id="1feab-103">Méthode CImageAllocator. NotifyMediaType</span><span class="sxs-lookup"><span data-stu-id="1feab-103">CImageAllocator.NotifyMediaType method</span></span>

<span data-ttu-id="1feab-104">La `NotifyMediaType` méthode informe l’objet du type de média actuel.</span><span class="sxs-lookup"><span data-stu-id="1feab-104">The `NotifyMediaType` method informs the object of the current media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1feab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1feab-105">Syntax</span></span>


```C++
void NotifyMediaType(
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="1feab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1feab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1feab-107">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="1feab-107">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="1feab-108">Pointeur vers un objet [**CMediaType**](cmediatype.md) , ou **null** pour effacer le type de média.</span><span class="sxs-lookup"><span data-stu-id="1feab-108">Pointer to a [**CMediaType**](cmediatype.md) object, or **NULL** to clear the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1feab-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1feab-109">Return value</span></span>

<span data-ttu-id="1feab-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1feab-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1feab-111">Notes</span><span class="sxs-lookup"><span data-stu-id="1feab-111">Remarks</span></span>

<span data-ttu-id="1feab-112">Le filtre propriétaire doit appeler cette méthode chaque fois que le type de média change.</span><span class="sxs-lookup"><span data-stu-id="1feab-112">The owning filter should call this method whenever the media type changes.</span></span> <span data-ttu-id="1feab-113">En général, cela se produit lorsque le code confidentiel se connecte pour la première fois et après une modification de format dynamique.</span><span class="sxs-lookup"><span data-stu-id="1feab-113">Typically this occurs when the pin first connects, and after a dynamic format change.</span></span> <span data-ttu-id="1feab-114">L’allocateur utilise le type de média pour valider les propriétés d’allocateur proposées, ainsi que lors de la création d’exemples de supports.</span><span class="sxs-lookup"><span data-stu-id="1feab-114">The allocator uses the media type to validate proposed allocator properties, and also when it creates media samples.</span></span>

<span data-ttu-id="1feab-115">L’objet **CImageAllocator** stocke le pointeur *pMediaType* dans la variable membre **m \_ pMediaType** .</span><span class="sxs-lookup"><span data-stu-id="1feab-115">The **CImageAllocator** object stores the *pMediaType* pointer in the **m\_pMediaType** member variable.</span></span> <span data-ttu-id="1feab-116">Par conséquent, si l’appelant doit libérer l’objet **CMediaType** , il doit mettre à jour l’allocateur en appelant à nouveau cette méthode, soit avec un nouveau pointeur, soit avec une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="1feab-116">Therefore, if the caller needs to release the **CMediaType** object, it should update the allocator by calling this method again, either with a new pointer or with a **NULL** value.</span></span> <span data-ttu-id="1feab-117">Dans le cas contraire, une erreur peut se produire lorsque l’allocateur tente de référencer l’ancien pointeur.</span><span class="sxs-lookup"><span data-stu-id="1feab-117">Otherwise, an error can occur when the allocator attempts to reference the old pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="1feab-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1feab-118">Requirements</span></span>



| <span data-ttu-id="1feab-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1feab-119">Requirement</span></span> | <span data-ttu-id="1feab-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="1feab-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1feab-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="1feab-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1feab-122"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1feab-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1feab-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1feab-123">Library</span></span><br/> | <dl> <span data-ttu-id="1feab-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1feab-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1feab-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1feab-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1feab-126">**CImageAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="1feab-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




