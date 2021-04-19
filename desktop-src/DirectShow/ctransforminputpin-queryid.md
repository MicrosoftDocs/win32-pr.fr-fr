---
description: 'La méthode QueryId récupère un identificateur pour le code confidentiel. Cette méthode implémente la méthode IPin :: QueryId.'
ms.assetid: 91fde383-0288-4307-9ca8-e117b6111769
title: CTransformInputPin. QueryId, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daae425e82bbc89cfbc863baea1924e36e63f122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528811"
---
# <a name="ctransforminputpinqueryid-method"></a><span data-ttu-id="80dcf-104">CTransformInputPin. QueryId, méthode</span><span class="sxs-lookup"><span data-stu-id="80dcf-104">CTransformInputPin.QueryId method</span></span>

<span data-ttu-id="80dcf-105">La `QueryId` méthode récupère un identificateur pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="80dcf-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="80dcf-106">Cette méthode implémente la méthode [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="80dcf-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80dcf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80dcf-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="80dcf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80dcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80dcf-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="80dcf-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="80dcf-110">Reçoit une chaîne contenant l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="80dcf-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80dcf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80dcf-111">Return value</span></span>

<span data-ttu-id="80dcf-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="80dcf-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="80dcf-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="80dcf-113">Return code</span></span>                                                                                   | <span data-ttu-id="80dcf-114">Description</span><span class="sxs-lookup"><span data-stu-id="80dcf-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="80dcf-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80dcf-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="80dcf-116">Succès</span><span class="sxs-lookup"><span data-stu-id="80dcf-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="80dcf-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="80dcf-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="80dcf-118">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="80dcf-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="80dcf-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="80dcf-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="80dcf-120">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="80dcf-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80dcf-121">Notes</span><span class="sxs-lookup"><span data-stu-id="80dcf-121">Remarks</span></span>

<span data-ttu-id="80dcf-122">L’identificateur de code confidentiel est utilisé pour la persistance des graphiques.</span><span class="sxs-lookup"><span data-stu-id="80dcf-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="80dcf-123">L’identificateur de code confidentiel de cette classe se trouve dans.</span><span class="sxs-lookup"><span data-stu-id="80dcf-123">The pin identifier for this class is In.</span></span> <span data-ttu-id="80dcf-124">Cette classe remplace le comportement de la classe [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="80dcf-124">This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="80dcf-125">Dans la classe **CBasePin** , l’identificateur de code confidentiel est le même que le nom du code confidentiel, spécifié dans le constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="80dcf-125">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="80dcf-126">Dans la classe **CTransformInputPin** , l’identificateur de code confidentiel et le nom du code confidentiel ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="80dcf-126">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="80dcf-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80dcf-127">Requirements</span></span>



| <span data-ttu-id="80dcf-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80dcf-128">Requirement</span></span> | <span data-ttu-id="80dcf-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="80dcf-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dcf-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="80dcf-130">Header</span></span><br/>  | <dl> <span data-ttu-id="80dcf-131"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80dcf-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="80dcf-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80dcf-132">Library</span></span><br/> | <dl> <span data-ttu-id="80dcf-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="80dcf-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




