---
description: La méthode SetSmartRecompressFormat spécifie un format de compression vidéo à utiliser pour la recompression intelligente.
ms.assetid: 80c02215-6da2-4b3e-ab0d-004e49480fb9
title: 'IAMTimelineGroup :: SetSmartRecompressFormat, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetSmartRecompressFormat
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9c8505f54d6ee9f6b2ec02216fd875fddbc619de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543295"
---
# <a name="iamtimelinegroupsetsmartrecompressformat-method"></a><span data-ttu-id="65d45-103">IAMTimelineGroup :: SetSmartRecompressFormat, méthode</span><span class="sxs-lookup"><span data-stu-id="65d45-103">IAMTimelineGroup::SetSmartRecompressFormat method</span></span>

> [!Note]  
> <span data-ttu-id="65d45-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="65d45-104">\[Deprecated.</span></span> <span data-ttu-id="65d45-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="65d45-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="65d45-106">La `SetSmartRecompressFormat` méthode spécifie un format de compression vidéo à utiliser pour la recompression intelligente.</span><span class="sxs-lookup"><span data-stu-id="65d45-106">The `SetSmartRecompressFormat` method specifies a video compression format to use for smart recompression.</span></span>

<span data-ttu-id="65d45-107">La recompression intelligente n’est pas prise en charge pour les groupes audio.</span><span class="sxs-lookup"><span data-stu-id="65d45-107">Smart recompression is not supported for audio groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d45-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65d45-108">Syntax</span></span>


```C++
HRESULT SetSmartRecompressFormat(
   long *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="65d45-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65d45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65d45-110">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="65d45-110">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="65d45-111">Pointeur vers une structure décrivant le format de compression.</span><span class="sxs-lookup"><span data-stu-id="65d45-111">Pointer to a structure describing the compression format.</span></span> <span data-ttu-id="65d45-112">Actuellement, seule la structure [**SCompFmt0**](scompfmt0.md) est valide.</span><span class="sxs-lookup"><span data-stu-id="65d45-112">Currently, only the [**SCompFmt0**](scompfmt0.md) structure is valid.</span></span> <span data-ttu-id="65d45-113">Vous devez effectuer un cast de ce paramètre en un pointeur de type **long**.</span><span class="sxs-lookup"><span data-stu-id="65d45-113">You must cast this parameter to a pointer of type **long**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65d45-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65d45-114">Return value</span></span>

<span data-ttu-id="65d45-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65d45-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65d45-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65d45-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65d45-117">Notes</span><span class="sxs-lookup"><span data-stu-id="65d45-117">Remarks</span></span>

<span data-ttu-id="65d45-118">Avant d’appeler cette méthode, appelez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) sur le même groupe pour spécifier un format non compressé.</span><span class="sxs-lookup"><span data-stu-id="65d45-118">Before calling this method, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method on the same group, to specify an uncompressed format.</span></span>

<span data-ttu-id="65d45-119">Si la `SetSmartRecompressFormat` méthode est réussie, vous pouvez utiliser le moteur de rendu intelligent pour générer un flux vidéo compressé.</span><span class="sxs-lookup"><span data-stu-id="65d45-119">If the `SetSmartRecompressFormat` method succeeds, you can use the Smart Render Engine to output a compressed video stream.</span></span> <span data-ttu-id="65d45-120">La vidéo compressée aura la largeur, la hauteur et la fréquence d’images spécifiées dans le paramètre *pFormat* .</span><span class="sxs-lookup"><span data-stu-id="65d45-120">The compressed video will have the width, height, and frame rate that was specified in the *pFormat* parameter.</span></span> <span data-ttu-id="65d45-121">Ces valeurs remplaceront celles données pour le format non compressé dans la méthode **SetMediaType** .</span><span class="sxs-lookup"><span data-stu-id="65d45-121">These values will override those given for the uncompressed format in the **SetMediaType** method.</span></span> <span data-ttu-id="65d45-122">Toutefois, pour bénéficier des avantages de la recompression intelligente, les deux formats doivent correspondre.</span><span class="sxs-lookup"><span data-stu-id="65d45-122">However, to get the benefits of smart recompression, the two formats should match.</span></span> <span data-ttu-id="65d45-123">En d’autres termes, les formats compressés et non compressés doivent avoir la même hauteur, largeur et fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="65d45-123">In other words, the compressed and uncompressed formats should have the same height, width, and frame rate.</span></span>

<span data-ttu-id="65d45-124">Si le moteur de rendu intelligent ne peut pas produire le format compressé, il génère un flux vidéo non compressé à la place.</span><span class="sxs-lookup"><span data-stu-id="65d45-124">If the Smart Render Engine is unable to produce the compressed format, it will produce an uncompressed video stream instead.</span></span> <span data-ttu-id="65d45-125">Si cela se produit, le moteur de rendu intelligent signale une \_ erreur de rendu de compresseur de l’ID DEX \_ \_ introuvable \_ pendant la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="65d45-125">If that occurs, the Smart Render Engine reports a DEX\_IDS\_CANT\_FIND\_COMPRESSOR rendering error during the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="65d45-126">L’application peut intercepter cette erreur par le biais de la méthode [**IAMErrorLog :: LogError**](iamerrorlog-logerror.md) .</span><span class="sxs-lookup"><span data-stu-id="65d45-126">The application can catch this error through the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="65d45-127">(Pour plus d’informations, consultez [journalisation des erreurs](logging-errors.md) et des [Erreurs de rendu](rendering-errors.md).)</span><span class="sxs-lookup"><span data-stu-id="65d45-127">(For more information, see [Logging Errors](logging-errors.md) and [Rendering Errors](rendering-errors.md).)</span></span>

<span data-ttu-id="65d45-128">Le format de recompression intelligente n’est pas persistant.</span><span class="sxs-lookup"><span data-stu-id="65d45-128">The smart recompression format is not persistent.</span></span> <span data-ttu-id="65d45-129">Si une application utilise la recompression intelligente, elle doit définir le format de recompression chaque fois qu’elle charge un fichier projet.</span><span class="sxs-lookup"><span data-stu-id="65d45-129">If an application uses smart recompression, it must set the recompression format whenever it loads a project file.</span></span>

> [!Note]  
> <span data-ttu-id="65d45-130">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="65d45-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="65d45-131">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="65d45-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="65d45-132">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="65d45-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65d45-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65d45-133">Requirements</span></span>



| <span data-ttu-id="65d45-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65d45-134">Requirement</span></span> | <span data-ttu-id="65d45-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="65d45-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65d45-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="65d45-136">Header</span></span><br/>  | <dl> <span data-ttu-id="65d45-137"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="65d45-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="65d45-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="65d45-138">Library</span></span><br/> | <dl> <span data-ttu-id="65d45-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65d45-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65d45-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65d45-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d45-141">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="65d45-141">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="65d45-142">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="65d45-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="65d45-143">Moteur de rendu intelligent</span><span class="sxs-lookup"><span data-stu-id="65d45-143">Smart Render Engine</span></span>](smart-render-engine.md)
</dt> <dt>

[<span data-ttu-id="65d45-144">Écriture d’un projet dans un fichier</span><span class="sxs-lookup"><span data-stu-id="65d45-144">Writing a Project to a File</span></span>](writing-a-project-to-a-file.md)
</dt> </dl>

 

 




