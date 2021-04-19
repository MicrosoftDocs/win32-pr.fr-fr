---
description: La méthode Insert ajoute un objet CDeferredCommand à la file d’attente.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: CCmdQueue. Insert, méthode (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532909"
---
# <a name="ccmdqueueinsert-method"></a><span data-ttu-id="a2f7e-103">CCmdQueue. Insert, méthode</span><span class="sxs-lookup"><span data-stu-id="a2f7e-103">CCmdQueue.Insert method</span></span>

<span data-ttu-id="a2f7e-104">La `Insert` méthode ajoute un objet [**CDeferredCommand**](cdeferredcommand.md) à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="a2f7e-104">The `Insert` method adds a [**CDeferredCommand**](cdeferredcommand.md) object to the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2f7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2f7e-105">Syntax</span></span>


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="a2f7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2f7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2f7e-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="a2f7e-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="a2f7e-108">Pointeur vers l’objet **CDeferredCommand** à ajouter à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="a2f7e-108">Pointer to the **CDeferredCommand** object to add to the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2f7e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2f7e-109">Return value</span></span>

<span data-ttu-id="a2f7e-110">Retourne S \_ OK dans l’implémentation par défaut.</span><span class="sxs-lookup"><span data-stu-id="a2f7e-110">Returns S\_OK in the default implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2f7e-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2f7e-111">Requirements</span></span>



| <span data-ttu-id="a2f7e-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2f7e-112">Requirement</span></span> | <span data-ttu-id="a2f7e-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2f7e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2f7e-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2f7e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a2f7e-115"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2f7e-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2f7e-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2f7e-116">Library</span></span><br/> | <dl> <span data-ttu-id="a2f7e-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a2f7e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2f7e-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2f7e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2f7e-119">**CCmdQueue, classe**</span><span class="sxs-lookup"><span data-stu-id="a2f7e-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




