---
description: La méthode HideCursor masque ou affiche le curseur.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Méthode CBaseControlWindow. HideCursor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536039"
---
# <a name="cbasecontrolwindowhidecursor-method"></a><span data-ttu-id="9f6bc-103">Méthode CBaseControlWindow. HideCursor</span><span class="sxs-lookup"><span data-stu-id="9f6bc-103">CBaseControlWindow.HideCursor method</span></span>

<span data-ttu-id="9f6bc-104">La `HideCursor` méthode masque ou affiche le curseur.</span><span class="sxs-lookup"><span data-stu-id="9f6bc-104">The `HideCursor` method hides or displays the cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f6bc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f6bc-105">Syntax</span></span>


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a><span data-ttu-id="9f6bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f6bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f6bc-107">*HideCursor*</span><span class="sxs-lookup"><span data-stu-id="9f6bc-107">*HideCursor*</span></span> 
</dt> <dd>

<span data-ttu-id="9f6bc-108">Valeur spécifiant s’il faut afficher le curseur.</span><span class="sxs-lookup"><span data-stu-id="9f6bc-108">Value specifying whether to show the cursor.</span></span> <span data-ttu-id="9f6bc-109">Définissez sur OATRUE pour masquer le curseur, ou OAFALSE pour afficher le curseur.</span><span class="sxs-lookup"><span data-stu-id="9f6bc-109">Set to OATRUE to hide the cursor, or OAFALSE to display the cursor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f6bc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f6bc-110">Return value</span></span>

<span data-ttu-id="9f6bc-111">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f6bc-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f6bc-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f6bc-112">Requirements</span></span>



| <span data-ttu-id="9f6bc-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f6bc-113">Requirement</span></span> | <span data-ttu-id="9f6bc-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f6bc-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f6bc-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f6bc-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9f6bc-116"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f6bc-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f6bc-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9f6bc-117">Library</span></span><br/> | <dl> <span data-ttu-id="9f6bc-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f6bc-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f6bc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f6bc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f6bc-120">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="9f6bc-120">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




