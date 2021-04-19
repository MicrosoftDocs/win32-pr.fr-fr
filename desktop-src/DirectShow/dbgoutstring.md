---
description: La fonction DbgOutString envoie une chaîne à l’emplacement de sortie de débogage. Ignoré dans les builds de vente au détail.
ms.assetid: 644bf4f7-ec2d-466e-85c6-690dd44da702
title: DbgOutString, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgOutString
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc12d4b73080f00a3d32c80074a801146ea4a74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542550"
---
# <a name="dbgoutstring-function"></a><span data-ttu-id="4b513-104">DbgOutString fonction)</span><span class="sxs-lookup"><span data-stu-id="4b513-104">DbgOutString function</span></span>

<span data-ttu-id="4b513-105">La fonction **DbgOutString** envoie une chaîne à l’emplacement de sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="4b513-105">The **DbgOutString** function sends a string to the debug output location.</span></span> <span data-ttu-id="4b513-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="4b513-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b513-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4b513-107">Syntax</span></span>


```C++
void DbgOutString(
   LPCTSTR psz
);
```



## <a name="parameters"></a><span data-ttu-id="4b513-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4b513-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b513-109">*psz*</span><span class="sxs-lookup"><span data-stu-id="4b513-109">*psz*</span></span> 
</dt> <dd>

<span data-ttu-id="4b513-110">Chaîne à sortir.</span><span class="sxs-lookup"><span data-stu-id="4b513-110">String to output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b513-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4b513-111">Return value</span></span>

<span data-ttu-id="4b513-112">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4b513-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b513-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4b513-113">Remarks</span></span>

<span data-ttu-id="4b513-114">Dans les versions Debug, cette fonction génère toujours la chaîne, indépendamment des niveaux de sortie de débogage actuels.</span><span class="sxs-lookup"><span data-stu-id="4b513-114">In debug builds, this function always outputs the string, regardless of the current debug output levels.</span></span> <span data-ttu-id="4b513-115">Pour un contrôle plus fin de la sortie, utilisez la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="4b513-115">For finer control over the output, use the [**DbgLog**](dbglog.md) macro.</span></span>

## <a name="examples"></a><span data-ttu-id="4b513-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="4b513-116">Examples</span></span>


```C++
DbgOutString("Creating the filter graph...\n"); 
```



## <a name="requirements"></a><span data-ttu-id="4b513-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4b513-117">Requirements</span></span>



| <span data-ttu-id="4b513-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4b513-118">Requirement</span></span> | <span data-ttu-id="4b513-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4b513-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b513-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4b513-120">Header</span></span><br/>  | <dl> <span data-ttu-id="4b513-121"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b513-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4b513-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4b513-122">Library</span></span><br/> | <dl> <span data-ttu-id="4b513-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4b513-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b513-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4b513-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b513-125">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="4b513-125">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




