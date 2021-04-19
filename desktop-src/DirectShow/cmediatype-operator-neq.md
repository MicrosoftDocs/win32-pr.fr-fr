---
description: Cet opérateur vérifie l’inégalité entre les objets CMediaType.
ms.assetid: 9caf4cb9-f049-42e7-abe4-79f8bf0ea542
title: 'CMediaType. CMediaType :: Operator ! =, méthode (mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator!=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe3d5b60ed1990423d5ad9375ffdf192da313b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532997"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="e80c9-103">CMediaType. CMediaType :: Operator ! =, méthode</span><span class="sxs-lookup"><span data-stu-id="e80c9-103">CMediaType.CMediaType::operator!= method</span></span>

<span data-ttu-id="e80c9-104">Cet opérateur vérifie l’inégalité entre les objets [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="e80c9-104">This operator tests for inequality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="e80c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e80c9-105">Syntax</span></span>


```C++
BOOL CMediaType::operator!=(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="e80c9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e80c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e80c9-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="e80c9-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e80c9-108">Référence à l’objet **CMediaType** à comparer.</span><span class="sxs-lookup"><span data-stu-id="e80c9-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e80c9-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e80c9-109">Return value</span></span>

<span data-ttu-id="e80c9-110">Retourne la **valeur true** si *RT* n’est pas égal à cet objet.</span><span class="sxs-lookup"><span data-stu-id="e80c9-110">Returns **TRUE** if *rt* is not equal to this object.</span></span> <span data-ttu-id="e80c9-111">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="e80c9-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e80c9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e80c9-112">Requirements</span></span>



| <span data-ttu-id="e80c9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e80c9-113">Requirement</span></span> | <span data-ttu-id="e80c9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e80c9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e80c9-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="e80c9-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e80c9-116"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e80c9-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="e80c9-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e80c9-117">Library</span></span><br/> | <dl> <span data-ttu-id="e80c9-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e80c9-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e80c9-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e80c9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e80c9-120">**CMediaType, classe**</span><span class="sxs-lookup"><span data-stu-id="e80c9-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




