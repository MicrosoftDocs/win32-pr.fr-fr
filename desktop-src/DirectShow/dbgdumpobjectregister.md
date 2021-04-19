---
description: La fonction DbgDumpObjectRegister affiche des informations sur les objets actifs. Ignoré dans les builds de vente au détail.
ms.assetid: 362d9912-662c-4a72-95b4-01f3d808e299
title: DbgDumpObjectRegister, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgDumpObjectRegister
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727d9c00ebbe3d48bb46797a1e27b9dd27c7b2c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542339"
---
# <a name="dbgdumpobjectregister-function"></a><span data-ttu-id="7428b-104">DbgDumpObjectRegister fonction)</span><span class="sxs-lookup"><span data-stu-id="7428b-104">DbgDumpObjectRegister function</span></span>

<span data-ttu-id="7428b-105">La `DbgDumpObjectRegister` fonction affiche des informations sur les objets actifs.</span><span class="sxs-lookup"><span data-stu-id="7428b-105">The `DbgDumpObjectRegister` function displays information about active objects.</span></span> <span data-ttu-id="7428b-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="7428b-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="7428b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7428b-107">Syntax</span></span>


```C++
void DbgDumpObjectRegister(void);
```



## <a name="parameters"></a><span data-ttu-id="7428b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7428b-108">Parameters</span></span>

<span data-ttu-id="7428b-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="7428b-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7428b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7428b-110">Return value</span></span>

<span data-ttu-id="7428b-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="7428b-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7428b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="7428b-112">Remarks</span></span>

<span data-ttu-id="7428b-113">Dans les versions Debug, la bibliothèque de débogage gère une liste d’objets actifs.</span><span class="sxs-lookup"><span data-stu-id="7428b-113">In debug builds, the debug library maintains a list of active objects.</span></span> <span data-ttu-id="7428b-114">La liste comprend tous les objets qui dérivent de [**CBaseObject**](cbaseobject.md), qui ont été créés par le module en cours et qui n’ont pas été détruits.</span><span class="sxs-lookup"><span data-stu-id="7428b-114">The list includes any objects that derive from [**CBaseObject**](cbaseobject.md), were created by the current module, and have not been destroyed.</span></span> <span data-ttu-id="7428b-115">Le constructeur **CBaseObject** et les méthodes de destructeur mettent à jour la liste.</span><span class="sxs-lookup"><span data-stu-id="7428b-115">The **CBaseObject** constructor and destructor methods update the list.</span></span>

<span data-ttu-id="7428b-116">Cette fonction génère plusieurs messages de mémoire de journal \_ .</span><span class="sxs-lookup"><span data-stu-id="7428b-116">This function generates several LOG\_MEMORY messages.</span></span> <span data-ttu-id="7428b-117">Au niveau de la journalisation 1, la fonction affiche uniquement le nombre total d’objets.</span><span class="sxs-lookup"><span data-stu-id="7428b-117">At logging level 1, the function displays only the total number of objects.</span></span> <span data-ttu-id="7428b-118">Au niveau de la journalisation 2 ou supérieur, elle affiche une liste des objets.</span><span class="sxs-lookup"><span data-stu-id="7428b-118">At logging level 2 or higher, it displays a list of the objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="7428b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7428b-119">Requirements</span></span>



| <span data-ttu-id="7428b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7428b-120">Requirement</span></span> | <span data-ttu-id="7428b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7428b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7428b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="7428b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7428b-123"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7428b-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7428b-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7428b-124">Library</span></span><br/> | <dl> <span data-ttu-id="7428b-125"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7428b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7428b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7428b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7428b-127">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="7428b-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




