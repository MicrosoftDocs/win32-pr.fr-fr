---
description: La méthode Invoke fournit l’accès aux méthodes et aux propriétés exposées par un objet.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: CDeferredCommand. Invoke, méthode (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545545"
---
# <a name="cdeferredcommandinvoke-method"></a><span data-ttu-id="78777-103">CDeferredCommand. Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="78777-103">CDeferredCommand.Invoke method</span></span>

<span data-ttu-id="78777-104">La `Invoke` méthode fournit l’accès aux méthodes et aux propriétés exposées par un objet.</span><span class="sxs-lookup"><span data-stu-id="78777-104">The `Invoke` method provides access to methods and properties exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="78777-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78777-105">Syntax</span></span>


```C++
HRESULT Invoke();
```



## <a name="parameters"></a><span data-ttu-id="78777-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78777-106">Parameters</span></span>

<span data-ttu-id="78777-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="78777-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="78777-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78777-108">Return value</span></span>

<span data-ttu-id="78777-109">Retourne VFW \_ E \_ déjà \_ annulé si **m \_ pQueue** a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="78777-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="78777-110">Sinon, retourne le **HRESULT** résultant d’un appel à **IDispatch :: GetTypeInfo** ou **IUnknown :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="78777-110">Otherwise, returns the **HRESULT** resulting from a call to **IDispatch::GetTypeInfo** or **IUnknown::QueryInterface**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78777-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78777-111">Requirements</span></span>



| <span data-ttu-id="78777-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78777-112">Requirement</span></span> | <span data-ttu-id="78777-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="78777-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78777-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="78777-114">Header</span></span><br/>  | <dl> <span data-ttu-id="78777-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78777-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78777-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78777-116">Library</span></span><br/> | <dl> <span data-ttu-id="78777-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="78777-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78777-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78777-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78777-119">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="78777-119">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




