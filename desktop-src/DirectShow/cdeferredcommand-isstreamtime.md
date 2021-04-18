---
description: La méthode IsStreamTime spécifie si la commande doit être exécutée au moment du flux ou de la présentation.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Méthode CDeferredCommand. IsStreamTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e15b579f911f6461df30c6b5ae9d3fc29f6fa1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533264"
---
# <a name="cdeferredcommandisstreamtime-method"></a><span data-ttu-id="84fa6-103">Méthode CDeferredCommand. IsStreamTime</span><span class="sxs-lookup"><span data-stu-id="84fa6-103">CDeferredCommand.IsStreamTime method</span></span>

<span data-ttu-id="84fa6-104">La `IsStreamTime` méthode spécifie si la commande doit être exécutée au moment du flux ou de la présentation.</span><span class="sxs-lookup"><span data-stu-id="84fa6-104">The `IsStreamTime` method specifies whether the command is to be run at stream time or presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="84fa6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84fa6-105">Syntax</span></span>


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a><span data-ttu-id="84fa6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84fa6-106">Parameters</span></span>

<span data-ttu-id="84fa6-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="84fa6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84fa6-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84fa6-108">Return value</span></span>

<span data-ttu-id="84fa6-109">Retourne la **valeur true** s’il est défini sur Time Stream. Sinon, retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="84fa6-109">Returns **TRUE** if set to stream time; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="84fa6-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84fa6-110">Requirements</span></span>



| <span data-ttu-id="84fa6-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84fa6-111">Requirement</span></span> | <span data-ttu-id="84fa6-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="84fa6-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84fa6-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="84fa6-113">Header</span></span><br/>  | <dl> <span data-ttu-id="84fa6-114"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84fa6-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="84fa6-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84fa6-115">Library</span></span><br/> | <dl> <span data-ttu-id="84fa6-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="84fa6-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84fa6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84fa6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84fa6-118">**CDeferredCommand, classe**</span><span class="sxs-lookup"><span data-stu-id="84fa6-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




