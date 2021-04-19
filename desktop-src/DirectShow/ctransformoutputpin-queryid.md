---
description: 'La méthode QueryId récupère un identificateur pour le code confidentiel. Cette méthode implémente la méthode IPin :: QueryId.'
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: CTransformOutputPin. QueryId, méthode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e8e5fbc4b4da7b38853df5b4dcf3580a8c198d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541419"
---
# <a name="ctransformoutputpinqueryid-method"></a><span data-ttu-id="48410-104">CTransformOutputPin. QueryId, méthode</span><span class="sxs-lookup"><span data-stu-id="48410-104">CTransformOutputPin.QueryId method</span></span>

<span data-ttu-id="48410-105">La `QueryId` méthode récupère un identificateur pour le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="48410-105">The `QueryId` method retrieves an identifier for the pin.</span></span> <span data-ttu-id="48410-106">Cette méthode implémente la méthode [**IPIN :: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) .</span><span class="sxs-lookup"><span data-stu-id="48410-106">This method implements the [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="48410-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48410-107">Syntax</span></span>


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a><span data-ttu-id="48410-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48410-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48410-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="48410-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="48410-110">Reçoit une chaîne contenant l’identificateur de code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="48410-110">Receives a string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48410-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48410-111">Return value</span></span>

<span data-ttu-id="48410-112">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="48410-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="48410-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="48410-113">Return code</span></span>                                                                                   | <span data-ttu-id="48410-114">Description</span><span class="sxs-lookup"><span data-stu-id="48410-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="48410-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48410-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="48410-116">Succès</span><span class="sxs-lookup"><span data-stu-id="48410-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="48410-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="48410-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="48410-118">Mémoire insuffisante</span><span class="sxs-lookup"><span data-stu-id="48410-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="48410-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="48410-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="48410-120">Argument de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="48410-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="48410-121">Notes</span><span class="sxs-lookup"><span data-stu-id="48410-121">Remarks</span></span>

<span data-ttu-id="48410-122">L’identificateur de code confidentiel est utilisé pour la persistance des graphiques.</span><span class="sxs-lookup"><span data-stu-id="48410-122">The pin identifier is used for graph persistence.</span></span> <span data-ttu-id="48410-123">L’identificateur de code confidentiel pour cette classe est out. Cette classe remplace le comportement de la classe [**CBasePin**](cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="48410-123">The pin identifier for this class is Out. This class overrides the behavior of the [**CBasePin**](cbasepin.md) class.</span></span> <span data-ttu-id="48410-124">Dans la classe **CBasePin** , l’identificateur de code confidentiel est le même que le nom du code confidentiel, spécifié dans le constructeur de classe.</span><span class="sxs-lookup"><span data-stu-id="48410-124">In the **CBasePin** class, the pin identifier is the same as the pin name, specified in the class constructor.</span></span> <span data-ttu-id="48410-125">Dans la classe **CTransformInputPin** , l’identificateur de code confidentiel et le nom du code confidentiel ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="48410-125">In the **CTransformInputPin** class, the pin identifier and the pin name are not the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="48410-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48410-126">Requirements</span></span>



| <span data-ttu-id="48410-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48410-127">Requirement</span></span> | <span data-ttu-id="48410-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="48410-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48410-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="48410-129">Header</span></span><br/>  | <dl> <span data-ttu-id="48410-130"><dt>Transfrm. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48410-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="48410-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48410-131">Library</span></span><br/> | <dl> <span data-ttu-id="48410-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="48410-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




