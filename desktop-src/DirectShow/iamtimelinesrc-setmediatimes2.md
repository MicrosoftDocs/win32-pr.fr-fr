---
description: 'La méthode SetMediaTimes2 définit les heures de démarrage et d’arrêt du support. Cette méthode est équivalente à IAMTimelineSrc :: SetMediaTimes, mais prend des valeurs REFTIME.'
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: 'IAMTimelineSrc :: SetMediaTimes2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4aa4f68a6fb93c329507edceea4e9665bfecd5f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543331"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a><span data-ttu-id="70db8-104">IAMTimelineSrc :: SetMediaTimes2, méthode</span><span class="sxs-lookup"><span data-stu-id="70db8-104">IAMTimelineSrc::SetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="70db8-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="70db8-105">\[Deprecated.</span></span> <span data-ttu-id="70db8-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70db8-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="70db8-107">La `SetMediaTimes2` méthode définit les heures de démarrage et d’arrêt du support.</span><span class="sxs-lookup"><span data-stu-id="70db8-107">The `SetMediaTimes2` method sets the media stop and start times.</span></span> <span data-ttu-id="70db8-108">Cette méthode est équivalente à [**IAMTimelineSrc :: SetMediaTimes**](iamtimelinesrc-setmediatimes.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="70db8-108">This method is equivalent to [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="70db8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70db8-109">Syntax</span></span>


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="70db8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70db8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70db8-111">*Start*</span><span class="sxs-lookup"><span data-stu-id="70db8-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="70db8-112">Heure de début du média, en secondes.</span><span class="sxs-lookup"><span data-stu-id="70db8-112">Media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="70db8-113">*Stop*</span><span class="sxs-lookup"><span data-stu-id="70db8-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="70db8-114">Temps d’arrêt du support, en secondes.</span><span class="sxs-lookup"><span data-stu-id="70db8-114">Media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70db8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70db8-115">Return value</span></span>

<span data-ttu-id="70db8-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="70db8-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="70db8-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70db8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="70db8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="70db8-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="70db8-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="70db8-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="70db8-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="70db8-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="70db8-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="70db8-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="70db8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70db8-122">Requirements</span></span>



| <span data-ttu-id="70db8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70db8-123">Requirement</span></span> | <span data-ttu-id="70db8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="70db8-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70db8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="70db8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="70db8-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="70db8-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="70db8-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="70db8-127">Library</span></span><br/> | <dl> <span data-ttu-id="70db8-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70db8-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70db8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70db8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70db8-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="70db8-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="70db8-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="70db8-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




