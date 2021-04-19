---
description: La méthode Init Initialise l’objet.
ms.assetid: a919adfa-0ffb-4241-b709-ad0e8d55476a
title: Méthode CSeekingPassThru.Init (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.Init
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78176a6966f379240b5b7edd1ef5b73d7fa75b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539515"
---
# <a name="cseekingpassthruinit-method"></a><span data-ttu-id="9211e-103">Méthode CSeekingPassThru.Init</span><span class="sxs-lookup"><span data-stu-id="9211e-103">CSeekingPassThru.Init method</span></span>

<span data-ttu-id="9211e-104">La `Init` méthode initialise l’objet.</span><span class="sxs-lookup"><span data-stu-id="9211e-104">The `Init` method initializes the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9211e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9211e-105">Syntax</span></span>


```C++
HRESULT Init(
  [in] BOOL bSupportRendering,
       IPin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="9211e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9211e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9211e-107">*bSupportRendering* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9211e-107">*bSupportRendering* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9211e-108">Valeur booléenne qui spécifie si le filtre est un convertisseur.</span><span class="sxs-lookup"><span data-stu-id="9211e-108">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="9211e-109">Utilisez la valeur **true** si le filtre est un convertisseur, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9211e-109">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="9211e-110">*pPin*</span><span class="sxs-lookup"><span data-stu-id="9211e-110">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9211e-111">Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) sur la broche d’entrée du filtre.</span><span class="sxs-lookup"><span data-stu-id="9211e-111">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9211e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9211e-112">Return value</span></span>

<span data-ttu-id="9211e-113">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9211e-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="9211e-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9211e-114">Return code</span></span>                                                                                   | <span data-ttu-id="9211e-115">Description</span><span class="sxs-lookup"><span data-stu-id="9211e-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="9211e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9211e-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9211e-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="9211e-117">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="9211e-118"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="9211e-118"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="9211e-119">L’objet a déjà été initialisé.</span><span class="sxs-lookup"><span data-stu-id="9211e-119">Object was already initialized.</span></span><br/>         |
| <dl> <span data-ttu-id="9211e-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="9211e-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9211e-121">Mémoire insuffisante pour créer l’objet.</span><span class="sxs-lookup"><span data-stu-id="9211e-121">Not enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9211e-122">Notes</span><span class="sxs-lookup"><span data-stu-id="9211e-122">Remarks</span></span>

<span data-ttu-id="9211e-123">Si la valeur de *bSupportRendering* est **true**, cette méthode crée une instance de la classe [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="9211e-123">If the value of *bSupportRendering* is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="9211e-124">Sinon, elle crée une instance de la classe [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="9211e-124">Otherwise, it creates an instance of the [**CPosPassThru**](cpospassthru.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="9211e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9211e-125">Requirements</span></span>



| <span data-ttu-id="9211e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9211e-126">Requirement</span></span> | <span data-ttu-id="9211e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9211e-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9211e-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9211e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9211e-129"><dt>Seekpt. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9211e-129"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9211e-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9211e-130">Library</span></span><br/> | <dl> <span data-ttu-id="9211e-131"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9211e-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9211e-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9211e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9211e-133">**CSeekingPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="9211e-133">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




