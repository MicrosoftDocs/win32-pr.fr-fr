---
description: La fonction LoadOLEAut32 charge la bibliothèque de liens dynamiques (OleAut32.dll) Automation.
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: LoadOLEAut32 fonction) (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532519"
---
# <a name="loadoleaut32-function"></a><span data-ttu-id="1fc5b-103">LoadOLEAut32 fonction)</span><span class="sxs-lookup"><span data-stu-id="1fc5b-103">LoadOLEAut32 function</span></span>

<span data-ttu-id="1fc5b-104">La fonction **LoadOLEAut32** charge la bibliothèque de liens dynamiques (OleAut32.dll) Automation.</span><span class="sxs-lookup"><span data-stu-id="1fc5b-104">The **LoadOLEAut32** function loads the Automation dynamic-link library (OleAut32.dll).</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1fc5b-105">Syntax</span></span>


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a><span data-ttu-id="1fc5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1fc5b-106">Parameters</span></span>

<span data-ttu-id="1fc5b-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="1fc5b-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1fc5b-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1fc5b-108">Return value</span></span>

<span data-ttu-id="1fc5b-109">Retourne un handle vers une instance de DLL Automation.</span><span class="sxs-lookup"><span data-stu-id="1fc5b-109">Returns a handle to an Automation DLL instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc5b-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1fc5b-110">Remarks</span></span>

<span data-ttu-id="1fc5b-111">Lorsque le destructeur [**CBaseObject**](cbaseobject.md) détruit l’objet qui a chargé OleAut32.dll, il décharge la bibliothèque si elle est toujours chargée.</span><span class="sxs-lookup"><span data-stu-id="1fc5b-111">When the [**CBaseObject**](cbaseobject.md) destructor destroys the object that loaded OleAut32.dll, it will unload the library if it is still loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc5b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1fc5b-112">Requirements</span></span>



| <span data-ttu-id="1fc5b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1fc5b-113">Requirement</span></span> | <span data-ttu-id="1fc5b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1fc5b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc5b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="1fc5b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1fc5b-116"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc5b-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1fc5b-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1fc5b-117">Library</span></span><br/> | <dl> <span data-ttu-id="1fc5b-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1fc5b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fc5b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1fc5b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc5b-120">**Fonctions d’assistance COM**</span><span class="sxs-lookup"><span data-stu-id="1fc5b-120">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




