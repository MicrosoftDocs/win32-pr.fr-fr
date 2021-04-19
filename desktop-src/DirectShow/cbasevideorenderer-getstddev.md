---
description: La méthode GetStdDev évalue l’écart type en millisecondes entre le moment où chaque image est due et le moment où elle est réellement rendue, pour les statistiques par image.
ms.assetid: 1a4d5c8d-38de-434f-b218-412d45976b8c
title: Méthode CBaseVideoRenderer. GetStdDev (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.GetStdDev
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85b40bda4715a8201cd05109b59746630c54654c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523541"
---
# <a name="cbasevideorenderergetstddev-method"></a><span data-ttu-id="643cf-103">Méthode CBaseVideoRenderer. GetStdDev</span><span class="sxs-lookup"><span data-stu-id="643cf-103">CBaseVideoRenderer.GetStdDev method</span></span>

<span data-ttu-id="643cf-104">La `GetStdDev` méthode évalue l’écart type en millisecondes entre le moment où chaque image est due et le moment où elle est réellement rendue, pour les statistiques par image.</span><span class="sxs-lookup"><span data-stu-id="643cf-104">The `GetStdDev` method estimates the standard deviation in milliseconds between when each frame is due and when it is actually rendered, for per-frame statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="643cf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="643cf-105">Syntax</span></span>


```C++
HRESULT GetStdDev(
   int      nSamples,
   int      *piResult,
   LONGLONG llSumSq,
   LONGLONG iTot
);
```



## <a name="parameters"></a><span data-ttu-id="643cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="643cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="643cf-107">*nSamples*</span><span class="sxs-lookup"><span data-stu-id="643cf-107">*nSamples*</span></span> 
</dt> <dd>

<span data-ttu-id="643cf-108">Valeur entière qui contient le nombre d’échantillons vidéo reçus par le convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="643cf-108">Integer value that contains the number of video samples received by the video renderer.</span></span>

</dd> <dt>

<span data-ttu-id="643cf-109">*piResult*</span><span class="sxs-lookup"><span data-stu-id="643cf-109">*piResult*</span></span> 
</dt> <dd>

<span data-ttu-id="643cf-110">Pointeur vers une valeur entière qui contiendra l’écart type.</span><span class="sxs-lookup"><span data-stu-id="643cf-110">Pointer to an integer value that will contain the standard deviation.</span></span>

</dd> <dt>

<span data-ttu-id="643cf-111">*llSumSq*</span><span class="sxs-lookup"><span data-stu-id="643cf-111">*llSumSq*</span></span> 
</dt> <dd>

<span data-ttu-id="643cf-112">Valeur qui représente l’écart type, en millisecondes, de tous les échantillons vidéo rendus.</span><span class="sxs-lookup"><span data-stu-id="643cf-112">Value that represents the standard deviation, in milliseconds, of all rendered video samples.</span></span> <span data-ttu-id="643cf-113">Plus la valeur est faible, plus le rendu est cohérent.</span><span class="sxs-lookup"><span data-stu-id="643cf-113">The lower the value, the more consistent the rendering.</span></span>

</dd> <dt>

<span data-ttu-id="643cf-114">*iTot*</span><span class="sxs-lookup"><span data-stu-id="643cf-114">*iTot*</span></span> 
</dt> <dd>

<span data-ttu-id="643cf-115">Valeur qui représente la valeur moyenne, en millisecondes, entre le temps horodaté et l’heure affichée pour tous les échantillons vidéo rendus.</span><span class="sxs-lookup"><span data-stu-id="643cf-115">Value that represents the mean value, in milliseconds, between the stamped time and rendered time for all rendered video samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="643cf-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="643cf-116">Return value</span></span>

<span data-ttu-id="643cf-117">Retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="643cf-117">Returns NOERROR.</span></span>

## <a name="requirements"></a><span data-ttu-id="643cf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="643cf-118">Requirements</span></span>



| <span data-ttu-id="643cf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="643cf-119">Requirement</span></span> | <span data-ttu-id="643cf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="643cf-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="643cf-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="643cf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="643cf-122"><dt>Renbase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="643cf-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="643cf-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="643cf-123">Library</span></span><br/> | <dl> <span data-ttu-id="643cf-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="643cf-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="643cf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="643cf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="643cf-126">**CBaseVideoRenderer, classe**</span><span class="sxs-lookup"><span data-stu-id="643cf-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




