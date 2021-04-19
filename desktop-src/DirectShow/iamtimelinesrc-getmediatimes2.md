---
description: 'La méthode GetMediaTimes2 récupère les heures de début et de fin des médias. Cette méthode est équivalente à IAMTimelineSrc :: GetMediaTimes, mais prend des valeurs REFTIME.'
ms.assetid: c3961c2c-7198-44bd-8734-7301a7c5b21e
title: 'IAMTimelineSrc :: GetMediaTimes2, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 779876e542ab51914725b326a0e3b217b893f254
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545566"
---
# <a name="iamtimelinesrcgetmediatimes2-method"></a><span data-ttu-id="ae84d-104">IAMTimelineSrc :: GetMediaTimes2, méthode</span><span class="sxs-lookup"><span data-stu-id="ae84d-104">IAMTimelineSrc::GetMediaTimes2 method</span></span>

> [!Note]  
> <span data-ttu-id="ae84d-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ae84d-105">\[Deprecated.</span></span> <span data-ttu-id="ae84d-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ae84d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ae84d-107">La `GetMediaTimes2` méthode récupère les heures de démarrage et d’arrêt du média.</span><span class="sxs-lookup"><span data-stu-id="ae84d-107">The `GetMediaTimes2` method retrieves the media start and stop times.</span></span> <span data-ttu-id="ae84d-108">Cette méthode est équivalente à [**IAMTimelineSrc :: GetMediaTimes**](iamtimelinesrc-getmediatimes.md), mais prend des valeurs [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="ae84d-108">This method is equivalent to [**IAMTimelineSrc::GetMediaTimes**](iamtimelinesrc-getmediatimes.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae84d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae84d-109">Syntax</span></span>


```C++
HRESULT GetMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="ae84d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae84d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae84d-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="ae84d-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="ae84d-112">Reçoit l’heure de début du support, en secondes.</span><span class="sxs-lookup"><span data-stu-id="ae84d-112">Receives the media start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ae84d-113">*pStop*</span><span class="sxs-lookup"><span data-stu-id="ae84d-113">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="ae84d-114">Reçoit l’heure d’arrêt du support, en secondes.</span><span class="sxs-lookup"><span data-stu-id="ae84d-114">Receives the media stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae84d-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae84d-115">Return value</span></span>

<span data-ttu-id="ae84d-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ae84d-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae84d-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae84d-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae84d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ae84d-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ae84d-119">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="ae84d-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ae84d-120">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ae84d-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ae84d-121">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ae84d-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ae84d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae84d-122">Requirements</span></span>



| <span data-ttu-id="ae84d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae84d-123">Requirement</span></span> | <span data-ttu-id="ae84d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae84d-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae84d-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae84d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ae84d-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae84d-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ae84d-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae84d-127">Library</span></span><br/> | <dl> <span data-ttu-id="ae84d-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae84d-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae84d-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae84d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae84d-130">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="ae84d-130">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="ae84d-131">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="ae84d-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




