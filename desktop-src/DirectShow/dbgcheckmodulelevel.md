---
description: La fonction DbgCheckModuleLevel vérifie si la journalisation est activée pour les types de messages et le niveau donnés. Ignoré dans les builds de vente au détail.
ms.assetid: f4b12df7-9001-4bfb-9d84-84a0e8295a8b
title: DbgCheckModuleLevel, fonction (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgCheckModuleLevel
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79df8cd06617cf9b17fa9933d4d7a87954a6e2b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537875"
---
# <a name="dbgcheckmodulelevel-function"></a><span data-ttu-id="ba966-104">DbgCheckModuleLevel fonction)</span><span class="sxs-lookup"><span data-stu-id="ba966-104">DbgCheckModuleLevel function</span></span>

<span data-ttu-id="ba966-105">La `DbgCheckModuleLevel` fonction vérifie si la journalisation est activée pour les types de messages et le niveau donnés.</span><span class="sxs-lookup"><span data-stu-id="ba966-105">The `DbgCheckModuleLevel` function checks whether logging is enabled for the given message types and level.</span></span> <span data-ttu-id="ba966-106">Ignoré dans les builds de vente au détail.</span><span class="sxs-lookup"><span data-stu-id="ba966-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba966-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba966-107">Syntax</span></span>


```C++
BOOL DbgCheckModuleLevel(
   DWORD Types,
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="ba966-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba966-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba966-109">*Types*</span><span class="sxs-lookup"><span data-stu-id="ba966-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="ba966-110">Combinaison d’opérations de bits d’un ou plusieurs types de messages.</span><span class="sxs-lookup"><span data-stu-id="ba966-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="ba966-111">*Niveau*</span><span class="sxs-lookup"><span data-stu-id="ba966-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="ba966-112">Niveau de journalisation</span><span class="sxs-lookup"><span data-stu-id="ba966-112">Logging level</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba966-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba966-113">Return value</span></span>

<span data-ttu-id="ba966-114">Retourne la **valeur true** si la journalisation de l’un des types de messages spécifiés est définie au niveau spécifié ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="ba966-114">Returns **TRUE** if logging for any of the specified message types is set to the specified level or higher.</span></span> <span data-ttu-id="ba966-115">Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="ba966-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba966-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba966-116">Requirements</span></span>



| <span data-ttu-id="ba966-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba966-117">Requirement</span></span> | <span data-ttu-id="ba966-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba966-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba966-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba966-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ba966-120"><dt>Wxdebug. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba966-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ba966-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba966-121">Library</span></span><br/> | <dl> <span data-ttu-id="ba966-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ba966-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba966-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba966-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba966-124">Fonctions de sortie de débogage</span><span class="sxs-lookup"><span data-stu-id="ba966-124">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




