---
description: La méthode GetDefaultRect récupère la taille par défaut de la zone cliente.
ms.assetid: 9eb9e3a4-0d45-4aa3-a496-1b0bd92d4989
title: Méthode CBaseWindow. GetDefaultRect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetDefaultRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d7ec9612eab45e21262f8344daf7a52a6a888b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537497"
---
# <a name="cbasewindowgetdefaultrect-method"></a><span data-ttu-id="f459a-103">Méthode CBaseWindow. GetDefaultRect</span><span class="sxs-lookup"><span data-stu-id="f459a-103">CBaseWindow.GetDefaultRect method</span></span>

<span data-ttu-id="f459a-104">La `GetDefaultRect` méthode récupère la taille par défaut de la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="f459a-104">The `GetDefaultRect` method retrieves the default size of the client area.</span></span>

## <a name="syntax"></a><span data-ttu-id="f459a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f459a-105">Syntax</span></span>


```C++
virtual RECT GetDefaultRect();
```



## <a name="parameters"></a><span data-ttu-id="f459a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f459a-106">Parameters</span></span>

<span data-ttu-id="f459a-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f459a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f459a-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f459a-108">Return value</span></span>

<span data-ttu-id="f459a-109">Retourne le rectangle par défaut.</span><span class="sxs-lookup"><span data-stu-id="f459a-109">Returns the default rectangle.</span></span>

## <a name="remarks"></a><span data-ttu-id="f459a-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f459a-110">Remarks</span></span>

<span data-ttu-id="f459a-111">Lorsque la fenêtre est activée, l’objet appelle cette méthode pour déterminer la taille de la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f459a-111">When the window is activated, the object calls this method to determine how large it should make the window's client area.</span></span> <span data-ttu-id="f459a-112">Dans la classe de base, cette méthode retourne un rectangle dont la hauteur et la largeur sont les constantes définies DEFHEIGHT et DEFWIDTH.</span><span class="sxs-lookup"><span data-stu-id="f459a-112">In the base class, this method returns a rectangle whose height and width are the defined constants DEFHEIGHT and DEFWIDTH.</span></span> <span data-ttu-id="f459a-113">Une classe dérivée doit substituer cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f459a-113">A derived class should override this method.</span></span> <span data-ttu-id="f459a-114">Pour un convertisseur vidéo, la classe dérivée retourne généralement la taille de l’image vidéo native.</span><span class="sxs-lookup"><span data-stu-id="f459a-114">For a video renderer, the derived class will typically return the size of the native video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="f459a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f459a-115">Requirements</span></span>



| <span data-ttu-id="f459a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f459a-116">Requirement</span></span> | <span data-ttu-id="f459a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f459a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f459a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f459a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f459a-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f459a-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f459a-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f459a-120">Library</span></span><br/> | <dl> <span data-ttu-id="f459a-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f459a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f459a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f459a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f459a-123">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="f459a-123">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




