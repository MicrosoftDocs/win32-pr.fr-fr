---
description: Méthode de constructeur.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Constructeur CSourceStream. CSourceStream (source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520882"
---
# <a name="csourcestreamcsourcestream-constructor"></a><span data-ttu-id="b4271-103">Constructeur CSourceStream. CSourceStream</span><span class="sxs-lookup"><span data-stu-id="b4271-103">CSourceStream.CSourceStream constructor</span></span>

<span data-ttu-id="b4271-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="b4271-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4271-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4271-105">Syntax</span></span>


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="b4271-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4271-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4271-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="b4271-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="b4271-108">Pointeur vers une chaîne contenant le nom de débogage du pin.</span><span class="sxs-lookup"><span data-stu-id="b4271-108">Pointer to a string containing the debug name of the pin.</span></span>

</dd> <dt>

<span data-ttu-id="b4271-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="b4271-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b4271-110">Pointeur vers une variable qui reçoit une valeur **HRESULT** indiquant la réussite ou l’échec de la méthode.</span><span class="sxs-lookup"><span data-stu-id="b4271-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="b4271-111">Initialisez la valeur sur \_ OK avant de créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4271-111">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="b4271-112">La valeur est modifiée uniquement si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="b4271-112">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="b4271-113">*PMS*</span><span class="sxs-lookup"><span data-stu-id="b4271-113">*pms*</span></span> 
</dt> <dd>

<span data-ttu-id="b4271-114">Pointeur vers le filtre [**CSource**](csource.md) qui a créé ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="b4271-114">Pointer to the [**CSource**](csource.md) filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="b4271-115">*pName*</span><span class="sxs-lookup"><span data-stu-id="b4271-115">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b4271-116">Pointeur vers une chaîne qui contient le nom du code PIN.</span><span class="sxs-lookup"><span data-stu-id="b4271-116">Pointer to a string that contains the name of the pin.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b4271-117">Notes</span><span class="sxs-lookup"><span data-stu-id="b4271-117">Remarks</span></span>

<span data-ttu-id="b4271-118">La chaîne spécifiée dans le paramètre *pObjectName* est utilisée uniquement à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="b4271-118">The string given in the *pObjectName* parameter is used only for debugging purposes.</span></span> <span data-ttu-id="b4271-119">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="b4271-119">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

<span data-ttu-id="b4271-120">La chaîne spécifiée dans le paramètre *pname* est le nom retourné par la méthode [**IPIN :: QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) .</span><span class="sxs-lookup"><span data-stu-id="b4271-120">The string given in the *pName* parameter is the name returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="b4271-121">La `CSourceStream` classe n’utilise pas ce nom pour l’identificateur de code confidentiel retourné par la méthode [**CSourceStream :: QueryId**](csourcestream-queryid.md) .</span><span class="sxs-lookup"><span data-stu-id="b4271-121">The `CSourceStream` class does not use this name for the pin identifier returned by the [**CSourceStream::QueryId**](csourcestream-queryid.md) method.</span></span> <span data-ttu-id="b4271-122">Au lieu de cela, **QueryId** calcule un identificateur de code confidentiel en fonction du numéro de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="b4271-122">Instead, **QueryId** calculates a pin identifier based on the pin number.</span></span> <span data-ttu-id="b4271-123">(Les identificateurs pin prennent en charge la persistance Graph.</span><span class="sxs-lookup"><span data-stu-id="b4271-123">(Pin identifiers support graph persistence.</span></span> <span data-ttu-id="b4271-124">Pour plus d’informations, consultez [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span><span class="sxs-lookup"><span data-stu-id="b4271-124">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).)</span></span>

<span data-ttu-id="b4271-125">Le constructeur ajoute automatiquement le code confidentiel au filtre propriétaire, en appelant [**CSource :: AddPin**](csource-addpin.md).</span><span class="sxs-lookup"><span data-stu-id="b4271-125">The constructor automatically adds the pin to the owning filter, by calling [**CSource::AddPin**](csource-addpin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4271-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4271-126">Requirements</span></span>



| <span data-ttu-id="b4271-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4271-127">Requirement</span></span> | <span data-ttu-id="b4271-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4271-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4271-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4271-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b4271-130"><dt>Source. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4271-130"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b4271-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4271-131">Library</span></span><br/> | <dl> <span data-ttu-id="b4271-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b4271-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4271-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4271-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4271-134">**CSourceStream, classe**</span><span class="sxs-lookup"><span data-stu-id="b4271-134">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




