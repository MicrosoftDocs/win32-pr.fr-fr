---
description: La méthode GetSourcesCount récupère le nombre de sources dans la piste.
ms.assetid: eb7f249f-355f-454d-9fe6-c3271fd13fc7
title: 'IAMTimelineTrack :: GetSourcesCount, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSourcesCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0e143b16e5cdc1e193760c0b97846be07eb72c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528658"
---
# <a name="iamtimelinetrackgetsourcescount-method"></a><span data-ttu-id="39fd7-103">IAMTimelineTrack :: GetSourcesCount, méthode</span><span class="sxs-lookup"><span data-stu-id="39fd7-103">IAMTimelineTrack::GetSourcesCount method</span></span>

> [!Note]  
> <span data-ttu-id="39fd7-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="39fd7-104">\[Deprecated.</span></span> <span data-ttu-id="39fd7-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39fd7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="39fd7-106">La `GetSourcesCount` méthode récupère le nombre de sources dans la piste.</span><span class="sxs-lookup"><span data-stu-id="39fd7-106">The `GetSourcesCount` method retrieves the number of sources in the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="39fd7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39fd7-107">Syntax</span></span>


```C++
HRESULT GetSourcesCount(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="39fd7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39fd7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39fd7-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="39fd7-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="39fd7-110">Reçoit le nombre de sources dans la piste.</span><span class="sxs-lookup"><span data-stu-id="39fd7-110">Receives the number of sources in the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39fd7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39fd7-111">Return value</span></span>

<span data-ttu-id="39fd7-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="39fd7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="39fd7-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="39fd7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="39fd7-114">Notes</span><span class="sxs-lookup"><span data-stu-id="39fd7-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="39fd7-115">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="39fd7-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="39fd7-116">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="39fd7-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="39fd7-117">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="39fd7-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39fd7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39fd7-118">Requirements</span></span>



| <span data-ttu-id="39fd7-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39fd7-119">Requirement</span></span> | <span data-ttu-id="39fd7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="39fd7-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39fd7-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="39fd7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="39fd7-122"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="39fd7-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="39fd7-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39fd7-123">Library</span></span><br/> | <dl> <span data-ttu-id="39fd7-124"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39fd7-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39fd7-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39fd7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fd7-126">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="39fd7-126">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="39fd7-127">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="39fd7-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




