---
description: 'La méthode FixMediaTimes2 arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche, comme défini par la fréquence d’images de sortie. Cette méthode est équivalente à IAMTimelineSrc :: FixMediaTimes, mais prend des valeurs REFTIME.'
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'IAMTimelineSrc :: FixMediaTimes2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537353"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a><span data-ttu-id="3eb7e-104">IAMTimelineSrc :: FixMediaTimes2, méthode</span><span class="sxs-lookup"><span data-stu-id="3eb7e-104">IAMTimelineSrc::FixMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="3eb7e-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-105">\[Deprecated.</span></span> <span data-ttu-id="3eb7e-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3eb7e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3eb7e-107">La `FixMediaTimes2` méthode arrondit les valeurs d’heure spécifiées à la limite d’image la plus proche, comme défini par la fréquence d’images de sortie.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-107">The `FixMediaTimes2` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="3eb7e-108">Cette méthode est équivalente à [**IAMTimelineSrc :: FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="3eb7e-108">This method is equivalent to [**IAMTimelineSrc::FixMediaTimes**](iamtimelinesrc-fixmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3eb7e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3eb7e-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="3eb7e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3eb7e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3eb7e-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="3eb7e-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb7e-112">Pointeur vers une variable qui contient l’heure de début, en secondes.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-112">Pointer to a variable that contains the start time, in seconds.</span></span> <span data-ttu-id="3eb7e-113">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="3eb7e-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="3eb7e-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="3eb7e-115">Pointeur vers une variable qui contient l’heure d’arrêt, en secondes.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-115">Pointer to a variable that contains the stop time, in seconds.</span></span> <span data-ttu-id="3eb7e-116">Si l’appel a échoué, cette variable est définie sur le temps arrondi.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3eb7e-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3eb7e-117">Return value</span></span>

<span data-ttu-id="3eb7e-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3eb7e-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3eb7e-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3eb7e-120">Notes</span><span class="sxs-lookup"><span data-stu-id="3eb7e-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3eb7e-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3eb7e-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="3eb7e-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3eb7e-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="3eb7e-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3eb7e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3eb7e-124">Requirements</span></span>



| <span data-ttu-id="3eb7e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3eb7e-125">Requirement</span></span> | <span data-ttu-id="3eb7e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eb7e-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3eb7e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3eb7e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3eb7e-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3eb7e-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3eb7e-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3eb7e-129">Library</span></span><br/> | <dl> <span data-ttu-id="3eb7e-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3eb7e-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3eb7e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3eb7e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3eb7e-132">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="3eb7e-132">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="3eb7e-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="3eb7e-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




