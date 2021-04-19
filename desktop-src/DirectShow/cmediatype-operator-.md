---
description: 'La méthode CMediaType. CMediaType :: Operator = (mtype. h) surcharge l’opérateur d’assignation pour copier un type de média.'
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'CMediaType. CMediaType :: Operator =, méthode (mtype. h)-paramètre cmtype'
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
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "106545319"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a><span data-ttu-id="a56a3-103">CMediaType. CMediaType :: Operator =, méthode (mtype. h)-paramètre cmtype</span><span class="sxs-lookup"><span data-stu-id="a56a3-103">CMediaType.CMediaType::operator= method (Mtype.h) - cmtype parameter</span></span>

<span data-ttu-id="a56a3-104">Cet opérateur surcharge l’opérateur d’assignation pour copier un type de média.</span><span class="sxs-lookup"><span data-stu-id="a56a3-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a56a3-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="a56a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a56a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a56a3-107">*cmtype* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="a56a3-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="a56a3-108">Référence à un objet **CMediaType** .</span><span class="sxs-lookup"><span data-stu-id="a56a3-108">Reference to a **CMediaType** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a56a3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a56a3-109">Return value</span></span>

<span data-ttu-id="a56a3-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="a56a3-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a56a3-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a56a3-111">Requirements</span></span>

| <span data-ttu-id="a56a3-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a56a3-112">Requirement</span></span>                   | <span data-ttu-id="a56a3-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a56a3-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a56a3-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="a56a3-114">Header</span></span>  | <span data-ttu-id="a56a3-115">Mtype. h (include streams. h)</span><span class="sxs-lookup"><span data-stu-id="a56a3-115">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="a56a3-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a56a3-116">Library</span></span> | <span data-ttu-id="a56a3-117">Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug)</span><span class="sxs-lookup"><span data-stu-id="a56a3-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="a56a3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a56a3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56a3-119">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="a56a3-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




