---
description: 'La méthode GetPointer récupère un pointeur de lecture/écriture vers la mémoire tampon. Cette méthode implémente la méthode IMediaSample :: GetPointer.'
ms.assetid: dd797ad5-6066-4366-a56f-621132f2e6ea
title: Méthode CMediaSample. GetPointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe8d8785bd52fbe601d9980f8fc146a2c6f41e40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528064"
---
# <a name="cmediasamplegetpointer-method"></a><span data-ttu-id="12384-104">Méthode CMediaSample. GetPointer</span><span class="sxs-lookup"><span data-stu-id="12384-104">CMediaSample.GetPointer method</span></span>

<span data-ttu-id="12384-105">La `GetPointer` méthode récupère un pointeur en lecture/écriture vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="12384-105">The `GetPointer` method retrieves a read/write pointer to the buffer.</span></span> <span data-ttu-id="12384-106">Cette méthode implémente la méthode [**IMediaSample :: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) .</span><span class="sxs-lookup"><span data-stu-id="12384-106">This method implements the [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12384-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12384-107">Syntax</span></span>


```C++
HRESULT GetPointer(
   BYTE **ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="12384-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12384-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12384-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="12384-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="12384-110">Adresse d’une variable qui reçoit un pointeur vers la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="12384-110">Address of a variable that receives a pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12384-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="12384-111">Return value</span></span>

<span data-ttu-id="12384-112">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12384-112">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="12384-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12384-113">Requirements</span></span>



| <span data-ttu-id="12384-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12384-114">Requirement</span></span> | <span data-ttu-id="12384-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="12384-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12384-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="12384-116">Header</span></span><br/>  | <dl> <span data-ttu-id="12384-117"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12384-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="12384-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="12384-118">Library</span></span><br/> | <dl> <span data-ttu-id="12384-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="12384-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12384-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12384-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12384-121">**CMediaSample, classe**</span><span class="sxs-lookup"><span data-stu-id="12384-121">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




