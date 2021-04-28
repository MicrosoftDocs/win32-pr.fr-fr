---
description: Méthode constructeur CBaseControlWindow. CBaseControlWindow.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Constructeur CBaseControlWindow. CBaseControlWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 47c8277a76dbf0fbb9e05262eea5b419466044cc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096337"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="b897f-103">Constructeur CBaseControlWindow. CBaseControlWindow</span><span class="sxs-lookup"><span data-stu-id="b897f-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="b897f-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="b897f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b897f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b897f-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="b897f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b897f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b897f-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="b897f-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="b897f-108">Pointeur vers l’objet de filtre de média propriétaire.</span><span class="sxs-lookup"><span data-stu-id="b897f-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="b897f-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="b897f-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="b897f-110">Pointeur vers la section critique à utiliser pour le verrouillage.</span><span class="sxs-lookup"><span data-stu-id="b897f-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="b897f-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="b897f-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b897f-112">Pointeur vers la description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b897f-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="b897f-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="b897f-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b897f-114">Pointeur vers l’interface de contrôle **IUnknown** , si l’objet fait partie d’un agrégat ; dans le cas contraire, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b897f-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b897f-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="b897f-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b897f-116">Pointeur vers une variable qui reçoit une valeur HRESULT indiquant la réussite ou l’échec de la méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="b897f-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b897f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b897f-117">Requirements</span></span>



| <span data-ttu-id="b897f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b897f-118">Requirement</span></span> | <span data-ttu-id="b897f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b897f-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b897f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b897f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b897f-121"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b897f-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b897f-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b897f-122">Library</span></span><br/> | <dl> <span data-ttu-id="b897f-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b897f-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b897f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b897f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b897f-125">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="b897f-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




