---
description: La méthode Receive est appelée lorsque l’objet reçoit un échantillon de support à partir de la broche de sortie. La classe dérivée doit implémenter cette méthode.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: CPullPin. Receive, méthode (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541357"
---
# <a name="cpullpinreceive-method"></a><span data-ttu-id="a7933-104">CPullPin. Receive, méthode</span><span class="sxs-lookup"><span data-stu-id="a7933-104">CPullPin.Receive method</span></span>

<span data-ttu-id="a7933-105">La `Receive` méthode est appelée lorsque l’objet reçoit un échantillon de média à partir de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="a7933-105">The `Receive` method is called when the object receives a media sample from the output pin.</span></span> <span data-ttu-id="a7933-106">La classe dérivée doit implémenter cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a7933-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7933-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7933-107">Syntax</span></span>


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="a7933-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7933-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7933-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="a7933-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="a7933-110">Pointeur vers l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) de l’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="a7933-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7933-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7933-111">Return value</span></span>

<span data-ttu-id="a7933-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7933-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a7933-113">Le retour d’une valeur autre que S \_ OK arrête le thread d’extraction de données.</span><span class="sxs-lookup"><span data-stu-id="a7933-113">Returning a value other than S\_OK will stop the data-pulling thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7933-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a7933-114">Remarks</span></span>

<span data-ttu-id="a7933-115">Cette méthode est appelée chaque fois qu’un nouvel exemple arrive à partir de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="a7933-115">This method is called whenever a new sample arrives from the output pin.</span></span> <span data-ttu-id="a7933-116">Écrivez cette méthode de la même manière que la méthode [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="a7933-116">Write this method in the same manner as the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

<span data-ttu-id="a7933-117">Les horodatages de l’échantillon spécifient les décalages d’octets par rapport à la position de début d’origine qui a été spécifiée dans la méthode [**CPullPin :: Seek**](cpullpin-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="a7933-117">The time stamps on the sample specify the byte offsets, relative to the original start position that was specified in [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span>

<span data-ttu-id="a7933-118">La position de début est arrondie à la limite d’alignement la plus proche et la position d’arrêt est arrondie à la limite d’alignement la plus proche.</span><span class="sxs-lookup"><span data-stu-id="a7933-118">The start position is rounded down to the nearest alignment boundary, and the stop position is rounded up to the nearest alignment boundary.</span></span> <span data-ttu-id="a7933-119">En outre, si la position d’arrêt dépasse la durée totale, la durée est utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="a7933-119">Also, if the stop position exceeds the total duration, the duration is used instead.</span></span>

<span data-ttu-id="a7933-120">Tous les horodatages sont fournis sous la forme d’un décalage d’octet multiplié par 10 millions, défini comme unités constantes.</span><span class="sxs-lookup"><span data-stu-id="a7933-120">All time stamps are given as a byte offset multiplied by 10,000,000, defined as the constant UNITS.</span></span> <span data-ttu-id="a7933-121">Par conséquent, une seconde est un octet.</span><span class="sxs-lookup"><span data-stu-id="a7933-121">Thus, notionally one second is one byte.</span></span> <span data-ttu-id="a7933-122">Pour rechercher les décalages d’octets réels, appelez [**IMediaSample :: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) et divisez les résultats par unités.</span><span class="sxs-lookup"><span data-stu-id="a7933-122">To find the actual byte offsets, call [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) and divide the results by UNITS.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7933-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7933-123">Requirements</span></span>



| <span data-ttu-id="a7933-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7933-124">Requirement</span></span> | <span data-ttu-id="a7933-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7933-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7933-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7933-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a7933-127"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7933-127"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="a7933-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a7933-128">Library</span></span><br/> | <dl> <span data-ttu-id="a7933-129"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a7933-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7933-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7933-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7933-131">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="a7933-131">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




