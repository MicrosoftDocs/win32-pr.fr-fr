---
description: Méthode de constructeur.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Constructeur CBaseObject. CBaseObject (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545348"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="be00d-103">Constructeur CBaseObject. CBaseObject</span><span class="sxs-lookup"><span data-stu-id="be00d-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="be00d-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="be00d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="be00d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be00d-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="be00d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be00d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be00d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="be00d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="be00d-108">Chaîne qui contient le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="be00d-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be00d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="be00d-109">Remarks</span></span>

<span data-ttu-id="be00d-110">Cette méthode incrémente le nombre d’objets actifs.</span><span class="sxs-lookup"><span data-stu-id="be00d-110">This method increments the active-object count.</span></span> <span data-ttu-id="be00d-111">(Voir [**CBaseObject :: ObjectsActive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="be00d-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="be00d-112">Allouez le paramètre *pname* dans la mémoire statique :</span><span class="sxs-lookup"><span data-stu-id="be00d-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="be00d-113">La macro de [**nom**](name.md) compile en **valeur null** dans les versions commerciales, afin que les chaînes statiques apparaissent uniquement dans les versions Debug.</span><span class="sxs-lookup"><span data-stu-id="be00d-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="be00d-114">Pour plus d’informations, consultez [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="be00d-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be00d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be00d-115">Requirements</span></span>



| <span data-ttu-id="be00d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be00d-116">Requirement</span></span> | <span data-ttu-id="be00d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="be00d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be00d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="be00d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="be00d-119"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be00d-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be00d-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="be00d-120">Library</span></span><br/> | <dl> <span data-ttu-id="be00d-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="be00d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be00d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be00d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be00d-123">**CBaseObject, classe**</span><span class="sxs-lookup"><span data-stu-id="be00d-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




