---
description: Récupère le nombre d’interfaces d’informations de type fournies par un objet.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Méthode CMediaControl. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537643"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="dc0ea-103">Méthode CMediaControl. GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="dc0ea-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="dc0ea-104">Récupère le nombre d’interfaces d’informations de type fournies par un objet.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0ea-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc0ea-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="dc0ea-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc0ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc0ea-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="dc0ea-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="dc0ea-108">Pointeur vers le nombre d’interfaces d’informations de type fourni par l’objet.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="dc0ea-109">Si l’objet fournit des informations de type, ce nombre est 1 ; dans le cas contraire, le nombre est 0.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc0ea-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc0ea-110">Return value</span></span>

<span data-ttu-id="dc0ea-111">Retourne le \_ pointeur E si *pcTInfo* n’est pas valide ; sinon, retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dc0ea-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0ea-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc0ea-112">Requirements</span></span>



| <span data-ttu-id="dc0ea-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc0ea-113">Requirement</span></span> | <span data-ttu-id="dc0ea-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc0ea-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc0ea-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc0ea-115">Header</span></span><br/>  | <dl> <span data-ttu-id="dc0ea-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc0ea-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc0ea-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dc0ea-117">Library</span></span><br/> | <dl> <span data-ttu-id="dc0ea-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dc0ea-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc0ea-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc0ea-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0ea-120">**CMediaControl, classe**</span><span class="sxs-lookup"><span data-stu-id="dc0ea-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




