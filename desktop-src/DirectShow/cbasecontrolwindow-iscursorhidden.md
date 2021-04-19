---
description: La méthode IsCursorHidden récupère l’état actuel du \_ membre de données m bCursorHidden.
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: Méthode CBaseControlWindow. IsCursorHidden (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537705"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a><span data-ttu-id="d4680-103">Méthode CBaseControlWindow. IsCursorHidden</span><span class="sxs-lookup"><span data-stu-id="d4680-103">CBaseControlWindow.IsCursorHidden method</span></span>

<span data-ttu-id="d4680-104">La `IsCursorHidden` méthode récupère l’état actuel du membre de données **m \_ bCursorHidden** .</span><span class="sxs-lookup"><span data-stu-id="d4680-104">The `IsCursorHidden` method retrieves the current state of the **m\_bCursorHidden** data member.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4680-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4680-105">Syntax</span></span>


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a><span data-ttu-id="d4680-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4680-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4680-107">*CursorHidden*</span><span class="sxs-lookup"><span data-stu-id="d4680-107">*CursorHidden*</span></span> 
</dt> <dd>

<span data-ttu-id="d4680-108">Pointeur vers la valeur de **m \_ bCursorHidden**.</span><span class="sxs-lookup"><span data-stu-id="d4680-108">Pointer to the value of **m\_bCursorHidden**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4680-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d4680-109">Return value</span></span>

<span data-ttu-id="d4680-110">En cas d’appel sans paramètre, retourne OATRUE si le curseur est masqué ou OAFALSE si le curseur est visible.</span><span class="sxs-lookup"><span data-stu-id="d4680-110">When called without a parameter, returns OATRUE if the cursor is hidden, or OAFALSE if the cursor is visible.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4680-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d4680-111">Remarks</span></span>

<span data-ttu-id="d4680-112">Les objets internes doivent appeler cette fonction membre sans le paramètre *CursorHidden* pour éviter de verrouiller la section critique.</span><span class="sxs-lookup"><span data-stu-id="d4680-112">Internal objects should call this member function without the *CursorHidden* parameter to avoid locking the critical section.</span></span> <span data-ttu-id="d4680-113">Les objets externes accèdent à cette fonction membre avec le paramètre *CursorHidden* via la méthode [**IVideoWindow :: IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) .</span><span class="sxs-lookup"><span data-stu-id="d4680-113">External objects access this member function with the *CursorHidden* parameter through the [**IVideoWindow::IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4680-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4680-114">Requirements</span></span>



| <span data-ttu-id="d4680-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4680-115">Requirement</span></span> | <span data-ttu-id="d4680-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4680-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4680-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4680-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d4680-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4680-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d4680-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4680-119">Library</span></span><br/> | <dl> <span data-ttu-id="d4680-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4680-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4680-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4680-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4680-122">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="d4680-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




