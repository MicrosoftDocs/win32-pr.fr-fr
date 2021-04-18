---
description: La méthode UnblockOutputPin débloque le code confidentiel. Lorsque le code confidentiel est débloqué, il peut fournir des échantillons, modifier son format de sortie et se reconnecter.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Méthode CDynamicOutputPin. UnblockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526613"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a><span data-ttu-id="ef336-104">Méthode CDynamicOutputPin. UnblockOutputPin</span><span class="sxs-lookup"><span data-stu-id="ef336-104">CDynamicOutputPin.UnblockOutputPin method</span></span>

<span data-ttu-id="ef336-105">La `UnblockOutputPin` méthode débloque le code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="ef336-105">The `UnblockOutputPin` method unblocks the pin.</span></span> <span data-ttu-id="ef336-106">Lorsque le code confidentiel est débloqué, il peut fournir des échantillons, modifier son format de sortie et se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="ef336-106">When the pin is unblocked, it can deliver samples, change its output format, and reconnect itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef336-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef336-107">Syntax</span></span>


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="ef336-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef336-108">Parameters</span></span>

<span data-ttu-id="ef336-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ef336-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ef336-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef336-110">Return value</span></span>

<span data-ttu-id="ef336-111">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ef336-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ef336-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ef336-112">Return code</span></span>                                                                             | <span data-ttu-id="ef336-113">Description</span><span class="sxs-lookup"><span data-stu-id="ef336-113">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ef336-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ef336-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ef336-115">Le code pin a déjà été débloqué.</span><span class="sxs-lookup"><span data-stu-id="ef336-115">Pin was already unblocked.</span></span><br/> |
| <dl> <span data-ttu-id="ef336-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef336-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ef336-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="ef336-117">Success.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="ef336-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef336-118">Requirements</span></span>



| <span data-ttu-id="ef336-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef336-119">Requirement</span></span> | <span data-ttu-id="ef336-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef336-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef336-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef336-121">Header</span></span><br/>  | <dl> <span data-ttu-id="ef336-122"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef336-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ef336-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ef336-123">Library</span></span><br/> | <dl> <span data-ttu-id="ef336-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ef336-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef336-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef336-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef336-126">**CDynamicOutputPin, classe**</span><span class="sxs-lookup"><span data-stu-id="ef336-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




