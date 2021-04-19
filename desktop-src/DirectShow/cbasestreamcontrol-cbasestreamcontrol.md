---
description: Méthode de constructeur.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Constructeur CBaseStreamControl. CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d325a48476fe2a80b7424850eb71a9d667cb60e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523550"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a><span data-ttu-id="d11d2-103">Constructeur CBaseStreamControl. CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="d11d2-103">CBaseStreamControl.CBaseStreamControl constructor</span></span>

<span data-ttu-id="d11d2-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="d11d2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d11d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d11d2-105">Syntax</span></span>


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d11d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d11d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d11d2-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="d11d2-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d11d2-108">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d11d2-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="d11d2-109">Si le constructeur échoue, ce paramètre reçoit un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d11d2-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="d11d2-110">Si cela se produit, l’état de l’objet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d11d2-110">If this occurs, the object is not in a valid state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d11d2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d11d2-111">Requirements</span></span>



| <span data-ttu-id="d11d2-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d11d2-112">Requirement</span></span> | <span data-ttu-id="d11d2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d11d2-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d11d2-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="d11d2-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d11d2-115"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d11d2-115"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d11d2-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d11d2-116">Library</span></span><br/> | <dl> <span data-ttu-id="d11d2-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d11d2-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d11d2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d11d2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d11d2-119">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="d11d2-119">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




