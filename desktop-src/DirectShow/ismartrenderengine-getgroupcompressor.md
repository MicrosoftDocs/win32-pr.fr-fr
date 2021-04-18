---
description: La méthode GetGroupCompressor récupère le filtre de compression pour le groupe spécifié.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'ISmartRenderEngine :: GetGroupCompressor, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540489"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a><span data-ttu-id="f5de0-103">ISmartRenderEngine :: GetGroupCompressor, méthode</span><span class="sxs-lookup"><span data-stu-id="f5de0-103">ISmartRenderEngine::GetGroupCompressor method</span></span>

> [!Note]  
> <span data-ttu-id="f5de0-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="f5de0-104">\[Deprecated.</span></span> <span data-ttu-id="f5de0-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5de0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f5de0-106">La `GetGroupCompressor` méthode récupère le filtre de compression pour le groupe spécifié.</span><span class="sxs-lookup"><span data-stu-id="f5de0-106">The `GetGroupCompressor` method retrieves the compression filter for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5de0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5de0-107">Syntax</span></span>


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a><span data-ttu-id="f5de0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5de0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5de0-109">*Groupe*</span><span class="sxs-lookup"><span data-stu-id="f5de0-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="f5de0-110">Index de base zéro du groupe.</span><span class="sxs-lookup"><span data-stu-id="f5de0-110">Zero-based index of the group.</span></span>

</dd> <dt>

<span data-ttu-id="f5de0-111">*pCompressor*</span><span class="sxs-lookup"><span data-stu-id="f5de0-111">*pCompressor*</span></span> 
</dt> <dd>

<span data-ttu-id="f5de0-112">Reçoit un pointeur vers l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) du filtre de compression.</span><span class="sxs-lookup"><span data-stu-id="f5de0-112">Receives a pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the compression filter.</span></span> <span data-ttu-id="f5de0-113">Elle reçoit la valeur **null** s’il n’existe aucun filtre de compression.</span><span class="sxs-lookup"><span data-stu-id="f5de0-113">It receives the value **NULL** if there is no compression filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5de0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f5de0-114">Return value</span></span>

<span data-ttu-id="f5de0-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5de0-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f5de0-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f5de0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5de0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f5de0-117">Remarks</span></span>

<span data-ttu-id="f5de0-118">Utilisez cette méthode pour définir les propriétés du filtre de compression, telles que la fréquence d’images clés.</span><span class="sxs-lookup"><span data-stu-id="f5de0-118">Use this method to set properties on the compression filter, such as the key-frame rate.</span></span> <span data-ttu-id="f5de0-119">Appelez cette méthode après avoir appelé [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md), mais avant de restituer le projet.</span><span class="sxs-lookup"><span data-stu-id="f5de0-119">Call this method after calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), but before rendering the project.</span></span> <span data-ttu-id="f5de0-120">Interrogez ensuite la broche de sortie du filtre de compression pour l’interface [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , qui contient des méthodes pour définir des paramètres de compression.</span><span class="sxs-lookup"><span data-stu-id="f5de0-120">Then query the compression filter's output pin for the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface, which contains methods for setting compression parameters.</span></span> <span data-ttu-id="f5de0-121">Relâchez l’interface lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="f5de0-121">Release the interface when you are done.</span></span> <span data-ttu-id="f5de0-122">Si vous apportez des modifications ultérieures à la chronologie, appelez **ConnectFrontEnd**, puis appelez à nouveau **GetGroupCompressor** pour réinitialiser les paramètres de compression.</span><span class="sxs-lookup"><span data-stu-id="f5de0-122">If you make any subsequent changes to the timeline, call **ConnectFrontEnd**, and then call **GetGroupCompressor** again to reset the compression parameters.</span></span>

<span data-ttu-id="f5de0-123">En cas de retour, si la valeur de \* *pCompressor* est non **null**, l’interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) a un nombre de références en suspens.</span><span class="sxs-lookup"><span data-stu-id="f5de0-123">On return, if the value of \**pCompressor* is non-**NULL**, the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface has an outstanding reference count.</span></span> <span data-ttu-id="f5de0-124">Veillez à libérer l’interface lorsque vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="f5de0-124">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="f5de0-125">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="f5de0-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f5de0-126">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f5de0-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f5de0-127">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f5de0-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5de0-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5de0-128">Requirements</span></span>



| <span data-ttu-id="f5de0-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5de0-129">Requirement</span></span> | <span data-ttu-id="f5de0-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5de0-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5de0-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5de0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="f5de0-132"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5de0-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f5de0-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5de0-133">Library</span></span><br/> | <dl> <span data-ttu-id="f5de0-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5de0-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5de0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5de0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5de0-136">**Interface ISmartRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="f5de0-136">**ISmartRenderEngine Interface**</span></span>](ismartrenderengine.md)
</dt> <dt>

[<span data-ttu-id="f5de0-137">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="f5de0-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




