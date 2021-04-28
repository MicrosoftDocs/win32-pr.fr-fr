---
description: Méthode constructeur CBaseStreamControl. CBaseStreamControl.
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
ms.openlocfilehash: 4c6521bec65e0182b8eb48eb5d3efe9ea609c6a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095847"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a><span data-ttu-id="f3a37-103">Constructeur CBaseStreamControl. CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="f3a37-103">CBaseStreamControl.CBaseStreamControl constructor</span></span>

<span data-ttu-id="f3a37-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f3a37-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a37-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3a37-105">Syntax</span></span>


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="f3a37-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3a37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3a37-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="f3a37-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f3a37-108">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f3a37-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="f3a37-109">Si le constructeur échoue, ce paramètre reçoit un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f3a37-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="f3a37-110">Si cela se produit, l’état de l’objet n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f3a37-110">If this occurs, the object is not in a valid state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3a37-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3a37-111">Requirements</span></span>



| <span data-ttu-id="f3a37-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3a37-112">Requirement</span></span> | <span data-ttu-id="f3a37-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3a37-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a37-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3a37-114">Header</span></span><br/>  | <dl> <span data-ttu-id="f3a37-115"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3a37-115"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f3a37-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f3a37-116">Library</span></span><br/> | <dl> <span data-ttu-id="f3a37-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f3a37-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a37-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3a37-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a37-119">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="f3a37-119">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




