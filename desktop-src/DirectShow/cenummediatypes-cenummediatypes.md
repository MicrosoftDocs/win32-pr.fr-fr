---
description: Méthode de constructeur.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Constructeur CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541613"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="70b14-103">Constructeur CEnumMediaTypes. CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="70b14-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="70b14-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="70b14-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="70b14-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70b14-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="70b14-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70b14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70b14-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="70b14-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="70b14-108">Pointeur vers le code confidentiel sur lequel l’énumération doit être exécutée.</span><span class="sxs-lookup"><span data-stu-id="70b14-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="70b14-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="70b14-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="70b14-110">Pointeur vers l’interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) d’un énumérateur à cloner, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="70b14-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="70b14-111">Notes</span><span class="sxs-lookup"><span data-stu-id="70b14-111">Remarks</span></span>

<span data-ttu-id="70b14-112">Si *pEnumMediaTypes* a la **valeur null**, cette méthode initialise l’énumérateur au début de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="70b14-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="70b14-113">Sinon, elle duplique l’état interne de l’énumérateur spécifié par *pEnumMediaTypes*.</span><span class="sxs-lookup"><span data-stu-id="70b14-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="70b14-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70b14-114">Requirements</span></span>



| <span data-ttu-id="70b14-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70b14-115">Requirement</span></span> | <span data-ttu-id="70b14-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="70b14-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70b14-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="70b14-117">Header</span></span><br/>  | <dl> <span data-ttu-id="70b14-118"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70b14-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="70b14-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70b14-119">Library</span></span><br/> | <dl> <span data-ttu-id="70b14-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="70b14-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70b14-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70b14-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b14-122">**CEnumMediaTypes, classe**</span><span class="sxs-lookup"><span data-stu-id="70b14-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




