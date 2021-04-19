---
description: La méthode OnDeactivate est appelée lors de la destruction de la fenêtre de la boîte de dialogue.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: CBasePropertyPage. OnDeactivate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530019"
---
# <a name="cbasepropertypageondeactivate-method"></a><span data-ttu-id="7f8e0-103">CBasePropertyPage. OnDeactivate, méthode</span><span class="sxs-lookup"><span data-stu-id="7f8e0-103">CBasePropertyPage.OnDeactivate method</span></span>

<span data-ttu-id="7f8e0-104">La `OnDeactivate` méthode est appelée lorsque la fenêtre de boîte de dialogue est détruite.</span><span class="sxs-lookup"><span data-stu-id="7f8e0-104">The `OnDeactivate` method is called when the dialog box window is destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8e0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7f8e0-105">Syntax</span></span>


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a><span data-ttu-id="7f8e0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7f8e0-106">Parameters</span></span>

<span data-ttu-id="7f8e0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7f8e0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f8e0-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7f8e0-108">Return value</span></span>

<span data-ttu-id="7f8e0-109">L’implémentation de la classe de base retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7f8e0-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f8e0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7f8e0-110">Remarks</span></span>

<span data-ttu-id="7f8e0-111">La méthode [**CBasePropertyPage ::D eactivate**](cbasepropertypage-deactivate.md) appelle la `OnDeactivate` méthode.</span><span class="sxs-lookup"><span data-stu-id="7f8e0-111">The [**CBasePropertyPage::Deactivate**](cbasepropertypage-deactivate.md) method calls the `OnDeactivate` method.</span></span> <span data-ttu-id="7f8e0-112">Substituez `OnDeactivate` pour libérer toutes les ressources obtenues par la classe dérivée dans la méthode [**CBasePropertyPage :: OnActivate**](cbasepropertypage-onactivate.md) , ou pour effectuer d’autres tâches si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7f8e0-112">Override `OnDeactivate` to release any resources that the derived class obtained in the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, or to perform other tasks as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8e0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f8e0-113">Requirements</span></span>



| <span data-ttu-id="7f8e0-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f8e0-114">Requirement</span></span> | <span data-ttu-id="7f8e0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f8e0-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8e0-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f8e0-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7f8e0-117"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f8e0-117"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="7f8e0-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7f8e0-118">Library</span></span><br/> | <dl> <span data-ttu-id="7f8e0-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f8e0-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f8e0-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f8e0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8e0-121">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="7f8e0-121">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




