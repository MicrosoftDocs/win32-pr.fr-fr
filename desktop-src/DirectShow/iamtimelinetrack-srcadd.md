---
description: La méthode SrcAdd ajoute une source à la piste.
ms.assetid: 71c62e92-02d6-4c6f-8121-2052d6cc832c
title: 'IAMTimelineTrack :: SrcAdd, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.SrcAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e3d1d727fb6a99e3dea9ec2659838df1bfcd392b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535889"
---
# <a name="iamtimelinetracksrcadd-method"></a><span data-ttu-id="0a7bc-103">IAMTimelineTrack :: SrcAdd, méthode</span><span class="sxs-lookup"><span data-stu-id="0a7bc-103">IAMTimelineTrack::SrcAdd method</span></span>

> [!Note]  
> <span data-ttu-id="0a7bc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-104">\[Deprecated.</span></span> <span data-ttu-id="0a7bc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a7bc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a7bc-106">La `SrcAdd` méthode ajoute une source à la piste.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-106">The `SrcAdd` method adds a source to the track.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a7bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a7bc-107">Syntax</span></span>


```C++
HRESULT SrcAdd(
   IAMTimelineObj *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="0a7bc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a7bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a7bc-109">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="0a7bc-109">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="0a7bc-110">Pointeur vers l’interface [**IAMTimelineObj**](iamtimelineobj.md) de l’objet source.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-110">Pointer to the source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a7bc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a7bc-111">Return value</span></span>

<span data-ttu-id="0a7bc-112">Retourne S \_ OK en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-112">Returns S\_OK if successful.</span></span> <span data-ttu-id="0a7bc-113">Retourne E \_ nointerface si l’objet n’est pas un objet source.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-113">Returns E\_NOINTERFACE if the object is not a source object.</span></span> <span data-ttu-id="0a7bc-114">Sinon, retourne une valeur **HRESULT** indiquant la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-114">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a7bc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0a7bc-115">Remarks</span></span>

<span data-ttu-id="0a7bc-116">Définissez les heures de début et de fin de la source avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-116">Set the source's start and stop times before calling this method.</span></span> <span data-ttu-id="0a7bc-117">(Appelez [**IAMTimelineObj :: SetStartStop**](iamtimelineobj-setstartstop.md).)</span><span class="sxs-lookup"><span data-stu-id="0a7bc-117">(Call [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md).)</span></span>

<span data-ttu-id="0a7bc-118">Actuellement, les ne peuvent pas afficher simultanément plus de 75 sources compressées avec des codecs VCM (Video Compression Manager).</span><span class="sxs-lookup"><span data-stu-id="0a7bc-118">Currently, DES cannot simultaneously render more than 75 sources that were compressed with Video Compression Manager (VCM) codecs.</span></span> <span data-ttu-id="0a7bc-119">En outre, si le projet dans son ensemble contient plus de 75 de telles sources, vous devez utiliser la reconnexion dynamique ou DES ne peuvent pas afficher un aperçu du projet.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-119">Also, if the project as a whole contains more than 75 such sources, you must use dynamic reconnection or DES cannot preview the project.</span></span> <span data-ttu-id="0a7bc-120">Pour plus d’informations, consultez [**IRenderEngine :: SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span><span class="sxs-lookup"><span data-stu-id="0a7bc-120">For more information, see [**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md).</span></span>

> [!Note]  
> <span data-ttu-id="0a7bc-121">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a7bc-122">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0a7bc-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a7bc-123">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="0a7bc-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a7bc-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a7bc-124">Requirements</span></span>



| <span data-ttu-id="0a7bc-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a7bc-125">Requirement</span></span> | <span data-ttu-id="0a7bc-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a7bc-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7bc-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a7bc-127">Header</span></span><br/>  | <dl> <span data-ttu-id="0a7bc-128"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a7bc-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a7bc-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0a7bc-129">Library</span></span><br/> | <dl> <span data-ttu-id="0a7bc-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a7bc-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a7bc-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a7bc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a7bc-132">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="0a7bc-132">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="0a7bc-133">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="0a7bc-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




