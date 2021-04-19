---
description: La méthode SetControlWindowPin définit le code confidentiel avec lequel effectuer la synchronisation.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Méthode CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533248"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a><span data-ttu-id="daf07-103">Méthode CBaseControlWindow. SetControlWindowPin</span><span class="sxs-lookup"><span data-stu-id="daf07-103">CBaseControlWindow.SetControlWindowPin method</span></span>

<span data-ttu-id="daf07-104">La `SetControlWindowPin` méthode définit le code confidentiel avec lequel effectuer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="daf07-104">The `SetControlWindowPin` method sets the pin with which to synchronize.</span></span>

## <a name="syntax"></a><span data-ttu-id="daf07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daf07-105">Syntax</span></span>


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="daf07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daf07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daf07-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="daf07-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="daf07-108">Pointeur vers le code confidentiel avec lequel l’interface est synchronisée.</span><span class="sxs-lookup"><span data-stu-id="daf07-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daf07-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="daf07-109">Return value</span></span>

<span data-ttu-id="daf07-110">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="daf07-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="daf07-111">Notes</span><span class="sxs-lookup"><span data-stu-id="daf07-111">Remarks</span></span>

<span data-ttu-id="daf07-112">Cette fonction membre définit la \_ variable de membre m pPin comme étant égale au paramètre pPin.</span><span class="sxs-lookup"><span data-stu-id="daf07-112">This member function sets the m\_pPin member variable equal to the pPin parameter.</span></span> <span data-ttu-id="daf07-113">Comme décrit dans le constructeur, l’interface peut être appelée uniquement lorsque le filtre a été connecté avec succès.</span><span class="sxs-lookup"><span data-stu-id="daf07-113">As described in the constructor, the interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="daf07-114">L’objet est passé par le biais de cette fonction membre au code confidentiel avec lequel il doit se synchroniser. dans la plupart des cas, il détermine si le code confidentiel est connecté chaque fois qu’il a une méthode d’interface appelée et retourne VFW \_ E \_ non \_ connecté en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="daf07-114">The object is passed in through this member function to the pin with which it should synchronize; in most cases, it will determine if the pin is connected whenever it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="daf07-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daf07-115">Requirements</span></span>



| <span data-ttu-id="daf07-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daf07-116">Requirement</span></span> | <span data-ttu-id="daf07-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="daf07-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="daf07-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="daf07-118">Header</span></span><br/>  | <dl> <span data-ttu-id="daf07-119"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="daf07-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="daf07-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="daf07-120">Library</span></span><br/> | <dl> <span data-ttu-id="daf07-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="daf07-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="daf07-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="daf07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="daf07-123">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="daf07-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




