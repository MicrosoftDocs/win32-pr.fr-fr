---
description: Récupère la taille maximale en octets nécessaire pour le flux actuel, à l’exclusion du numéro de version.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Méthode CPersistStream. SizeMax (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539700"
---
# <a name="cpersiststreamsizemax-method"></a><span data-ttu-id="9827f-103">Méthode CPersistStream. SizeMax</span><span class="sxs-lookup"><span data-stu-id="9827f-103">CPersistStream.SizeMax method</span></span>

<span data-ttu-id="9827f-104">Récupère la taille maximale en octets nécessaire pour le flux actuel, à l’exclusion du numéro de version.</span><span class="sxs-lookup"><span data-stu-id="9827f-104">Retrieves the maximum byte size needed for the current stream, not including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="9827f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9827f-105">Syntax</span></span>


```C++
virtual int SizeMax();
```



## <a name="parameters"></a><span data-ttu-id="9827f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9827f-106">Parameters</span></span>

<span data-ttu-id="9827f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="9827f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9827f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9827f-108">Return value</span></span>

<span data-ttu-id="9827f-109">Retourne le nombre d’octets nécessaires pour les données, à l’exclusion du numéro de version.</span><span class="sxs-lookup"><span data-stu-id="9827f-109">Returns the number of bytes needed for data, not including the version number.</span></span>

## <a name="remarks"></a><span data-ttu-id="9827f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9827f-110">Remarks</span></span>

<span data-ttu-id="9827f-111">La version par défaut retourne zéro ; elle doit être substituée pour fournir une autre valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="9827f-111">The default version returns zero; it should be overridden to provide some other appropriate value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9827f-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9827f-112">Requirements</span></span>



| <span data-ttu-id="9827f-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9827f-113">Requirement</span></span> | <span data-ttu-id="9827f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9827f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9827f-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="9827f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9827f-116"><dt>PStream. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9827f-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9827f-117">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9827f-117">Library</span></span><br/> | <dl> <span data-ttu-id="9827f-118"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9827f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9827f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9827f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9827f-120">**CPersistStream, classe**</span><span class="sxs-lookup"><span data-stu-id="9827f-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




