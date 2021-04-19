---
description: 'La méthode GetClassID récupère l’identificateur de classe (CLSID) de l’objet. Cette méthode implémente la méthode IPersist :: GetClassID.'
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: Méthode CSystemClock. GetClassID (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532018"
---
# <a name="csystemclockgetclassid-method"></a><span data-ttu-id="06161-104">Méthode CSystemClock. GetClassID</span><span class="sxs-lookup"><span data-stu-id="06161-104">CSystemClock.GetClassID method</span></span>

<span data-ttu-id="06161-105">La `GetClassID` méthode récupère l’identificateur de classe (CLSID) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="06161-105">The `GetClassID` method retrieves the class identifier (CLSID) of the object.</span></span> <span data-ttu-id="06161-106">Cette méthode implémente la méthode **IPersist :: GetClassID** .</span><span class="sxs-lookup"><span data-stu-id="06161-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06161-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06161-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="06161-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06161-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06161-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="06161-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="06161-110">Pointeur vers une variable qui reçoit la valeur CLSID \_ SystemClock.</span><span class="sxs-lookup"><span data-stu-id="06161-110">Pointer to a variable that receives the value CLSID\_SystemClock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06161-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06161-111">Return value</span></span>

<span data-ttu-id="06161-112">Retourne le \_ pointeur S ou OK \_ .</span><span class="sxs-lookup"><span data-stu-id="06161-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="06161-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06161-113">Requirements</span></span>



| <span data-ttu-id="06161-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06161-114">Requirement</span></span> | <span data-ttu-id="06161-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="06161-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06161-116">Version</span><span class="sxs-lookup"><span data-stu-id="06161-116">Version</span></span><br/> | <span data-ttu-id="06161-117">CSystemClock, classe</span><span class="sxs-lookup"><span data-stu-id="06161-117">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="06161-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="06161-118">Header</span></span><br/>  | <dl> <span data-ttu-id="06161-119"><dt>Sysclock. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06161-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="06161-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="06161-120">Library</span></span><br/> | <dl> <span data-ttu-id="06161-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="06161-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




