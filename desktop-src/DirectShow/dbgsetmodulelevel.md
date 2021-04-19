---
description: La fonction DbgSetModuleLevel définit le niveau de journalisation pour un ou plusieurs types de messages. Ignoré dans les builds de vente au détail.
ms.assetid: 89d25106-8018-4089-8b77-d3c87529e984
title: DbgSetModuleLevel, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgSetModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d6623793b150c600eb00f0c0843dd72c68deb4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528108"
---
# <a name="dbgsetmodulelevel-function"></a><span data-ttu-id="3d5db-104">DbgSetModuleLevel fonction)</span><span class="sxs-lookup"><span data-stu-id="3d5db-104">DbgSetModuleLevel function</span></span>

<span data-ttu-id="3d5db-105">La fonction **DbgSetModuleLevel** définit le niveau de journalisation pour un ou plusieurs types de messages.</span><span class="sxs-lookup"><span data-stu-id="3d5db-105">The **DbgSetModuleLevel** function sets the logging level for one or more message types.</span></span> <span data-ttu-id="3d5db-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="3d5db-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d5db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d5db-107">Syntax</span></span>


```C++
void DbgSetModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="3d5db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d5db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d5db-109">*Types*</span><span class="sxs-lookup"><span data-stu-id="3d5db-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5db-110">Combinaison d’opérations de bits d’un ou plusieurs types de messages.</span><span class="sxs-lookup"><span data-stu-id="3d5db-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="3d5db-111">*Niveau*</span><span class="sxs-lookup"><span data-stu-id="3d5db-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="3d5db-112">Niveau de journalisation pour les types de messages spécifiés.</span><span class="sxs-lookup"><span data-stu-id="3d5db-112">Logging level for the specified message types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d5db-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3d5db-113">Return value</span></span>

<span data-ttu-id="3d5db-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3d5db-114">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d5db-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d5db-115">Requirements</span></span>



| <span data-ttu-id="3d5db-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d5db-116">Requirement</span></span> | <span data-ttu-id="3d5db-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d5db-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d5db-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d5db-118">Header</span></span><br/>  | <dl> <span data-ttu-id="3d5db-119"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3d5db-119"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3d5db-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3d5db-120">Library</span></span><br/> | <dl> <span data-ttu-id="3d5db-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3d5db-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d5db-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d5db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d5db-123">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="3d5db-123">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




