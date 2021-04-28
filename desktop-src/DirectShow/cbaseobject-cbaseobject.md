---
description: Méthode constructeur CBaseObject. CBaseObject.
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
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099617"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="bfda3-103">Constructeur CBaseObject. CBaseObject</span><span class="sxs-lookup"><span data-stu-id="bfda3-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="bfda3-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="bfda3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfda3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfda3-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="bfda3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfda3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfda3-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="bfda3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="bfda3-108">Chaîne qui contient le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="bfda3-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfda3-109">Notes </span><span class="sxs-lookup"><span data-stu-id="bfda3-109">Remarks</span></span>

<span data-ttu-id="bfda3-110">Cette méthode incrémente le nombre d’objets actifs.</span><span class="sxs-lookup"><span data-stu-id="bfda3-110">This method increments the active-object count.</span></span> <span data-ttu-id="bfda3-111">(Voir [**CBaseObject :: ObjectsActive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="bfda3-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="bfda3-112">Allouez le paramètre *pname* dans la mémoire statique :</span><span class="sxs-lookup"><span data-stu-id="bfda3-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="bfda3-113">La macro de [**nom**](name.md) compile en **valeur null** dans les versions commerciales, afin que les chaînes statiques apparaissent uniquement dans les versions Debug.</span><span class="sxs-lookup"><span data-stu-id="bfda3-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="bfda3-114">Pour plus d’informations, consultez [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="bfda3-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfda3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfda3-115">Requirements</span></span>



| <span data-ttu-id="bfda3-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfda3-116">Requirement</span></span> | <span data-ttu-id="bfda3-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfda3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfda3-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfda3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bfda3-119"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bfda3-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bfda3-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bfda3-120">Library</span></span><br/> | <dl> <span data-ttu-id="bfda3-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="bfda3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfda3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfda3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfda3-123">**CBaseObject, classe**</span><span class="sxs-lookup"><span data-stu-id="bfda3-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




