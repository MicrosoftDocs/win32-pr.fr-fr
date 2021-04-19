---
description: Cet opérateur vérifie l’égalité entre les objets CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'CMediaType. CMediaType :: Operator = =, méthode (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535006"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="882bf-103">CMediaType. CMediaType :: Operator = =, méthode</span><span class="sxs-lookup"><span data-stu-id="882bf-103">CMediaType.CMediaType::operator== method</span></span>

<span data-ttu-id="882bf-104">Cet opérateur vérifie l’égalité entre les objets [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="882bf-104">This operator tests for equality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="882bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="882bf-105">Syntax</span></span>


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="882bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="882bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882bf-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="882bf-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="882bf-108">Référence à l’objet **CMediaType** à comparer.</span><span class="sxs-lookup"><span data-stu-id="882bf-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882bf-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="882bf-109">Return value</span></span>

<span data-ttu-id="882bf-110">Retourne la **valeur true** si *RT* est égal à cet objet.</span><span class="sxs-lookup"><span data-stu-id="882bf-110">Returns **TRUE** if *rt* is equal to this object.</span></span> <span data-ttu-id="882bf-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="882bf-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="882bf-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="882bf-112">Requirements</span></span>



| <span data-ttu-id="882bf-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="882bf-113">Requirement</span></span> | <span data-ttu-id="882bf-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="882bf-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="882bf-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="882bf-115">Header</span></span><br/>  | <dl> <span data-ttu-id="882bf-116"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="882bf-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="882bf-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="882bf-117">Library</span></span><br/> | <dl> <span data-ttu-id="882bf-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="882bf-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="882bf-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="882bf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882bf-120">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="882bf-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




