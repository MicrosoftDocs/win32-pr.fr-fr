---
description: La méthode WriteBitmapBits récupère une image vidéo à l’heure du média spécifiée et l’écrit dans un fichier. La trame vidéo est toujours au format RGB 24 bits.
ms.assetid: 8b21f37b-553d-4de2-8725-c94c29fa3a1a
title: 'IMediaDet :: WriteBitmapBits, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.WriteBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 79bf54f136cc2ab9db1208ad6c2b4e5cb12bd950
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542570"
---
# <a name="imediadetwritebitmapbits-method"></a><span data-ttu-id="757a0-104">IMediaDet :: WriteBitmapBits, méthode</span><span class="sxs-lookup"><span data-stu-id="757a0-104">IMediaDet::WriteBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="757a0-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="757a0-105">\[Deprecated.</span></span> <span data-ttu-id="757a0-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="757a0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="757a0-107">La `WriteBitmapBits` méthode récupère une image vidéo à l’heure du média spécifiée et l’écrit dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="757a0-107">The `WriteBitmapBits` method retrieves a video frame at the specified media time and writes it to a file.</span></span> <span data-ttu-id="757a0-108">La trame vidéo est toujours au format RGB 24 bits.</span><span class="sxs-lookup"><span data-stu-id="757a0-108">The video frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="757a0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="757a0-109">Syntax</span></span>


```C++
HRESULT WriteBitmapBits(
   double StreamTime,
   long   Width,
   long   Height,
   BSTR   Filename
);
```



## <a name="parameters"></a><span data-ttu-id="757a0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="757a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757a0-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="757a0-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="757a0-112">Heure à laquelle récupérer l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="757a0-112">Time at which to retrieve the video frame.</span></span>

</dd> <dt>

<span data-ttu-id="757a0-113">*Width*</span><span class="sxs-lookup"><span data-stu-id="757a0-113">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="757a0-114">Largeur de l’image, en pixels.</span><span class="sxs-lookup"><span data-stu-id="757a0-114">Width of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="757a0-115">*Height*</span><span class="sxs-lookup"><span data-stu-id="757a0-115">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="757a0-116">Hauteur de l’image, en pixels.</span><span class="sxs-lookup"><span data-stu-id="757a0-116">Height of the image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="757a0-117">*Nom du fichier*</span><span class="sxs-lookup"><span data-stu-id="757a0-117">*Filename*</span></span> 
</dt> <dd>

<span data-ttu-id="757a0-118">Chemin d’accès du fichier dans lequel enregistrer l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="757a0-118">Path of the file in which to save the bitmap.</span></span> <span data-ttu-id="757a0-119">Si le fichier existe déjà, cette méthode le remplace.</span><span class="sxs-lookup"><span data-stu-id="757a0-119">If the file already exists, this method overwrites it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="757a0-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="757a0-120">Return value</span></span>

<span data-ttu-id="757a0-121">Retourne S \_ OK correctement.</span><span class="sxs-lookup"><span data-stu-id="757a0-121">Returns S\_OK it successful.</span></span> <span data-ttu-id="757a0-122">Sinon, retourne une valeur **HRESULT** qui indique la cause de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="757a0-122">Otherwise, returns an **HRESULT** value that indicates the cause of the error.</span></span> <span data-ttu-id="757a0-123">Les codes d’erreur possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="757a0-123">Possible error codes include the following:</span></span>



| <span data-ttu-id="757a0-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="757a0-124">Return code</span></span>                                                                                             | <span data-ttu-id="757a0-125">Description</span><span class="sxs-lookup"><span data-stu-id="757a0-125">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="757a0-126"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-126"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="757a0-127">Impossible d’ajouter l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) au graphique.</span><span class="sxs-lookup"><span data-stu-id="757a0-127">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="757a0-128"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-128"><dt>**E\_FAIL**</dt></span></span> </dl>                  | <span data-ttu-id="757a0-129">Échec.</span><span class="sxs-lookup"><span data-stu-id="757a0-129">Failure.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="757a0-130"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="757a0-131">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="757a0-131">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="757a0-132"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="757a0-133">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="757a0-133">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="757a0-134"><dt>**STG \_ E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-134"><dt>**STG\_E\_ACCESSDENIED**</dt></span></span> </dl>     | <span data-ttu-id="757a0-135">Impossible de remplacer le fichier.</span><span class="sxs-lookup"><span data-stu-id="757a0-135">Cannot overwrite file.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="757a0-136"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-136"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="757a0-137">Type de média non valide.</span><span class="sxs-lookup"><span data-stu-id="757a0-137">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="757a0-138">Notes</span><span class="sxs-lookup"><span data-stu-id="757a0-138">Remarks</span></span>

<span data-ttu-id="757a0-139">Avant d’appeler cette méthode, définissez le nom de fichier et le flux en appelant [**IMediaDet ::p ut \_ filename**](imediadet-put-filename.md) et [**IMediaDet ::p ut \_ CurrentStream**](imediadet-put-currentstream.md).</span><span class="sxs-lookup"><span data-stu-id="757a0-139">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="757a0-140">Cette méthode met le détecteur de média en mode de manipulation bitmap.</span><span class="sxs-lookup"><span data-stu-id="757a0-140">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="757a0-141">Une fois cette méthode appelée, les différentes méthodes d’informations de flux de **IMediaDet** ne fonctionnent pas, sauf si vous créez une nouvelle instance du détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="757a0-141">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="757a0-142">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="757a0-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="757a0-143">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="757a0-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="757a0-144">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="757a0-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="757a0-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="757a0-145">Requirements</span></span>



| <span data-ttu-id="757a0-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="757a0-146">Requirement</span></span> | <span data-ttu-id="757a0-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="757a0-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="757a0-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="757a0-148">Header</span></span><br/>  | <dl> <span data-ttu-id="757a0-149"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="757a0-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="757a0-150">Library</span></span><br/> | <dl> <span data-ttu-id="757a0-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="757a0-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757a0-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="757a0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757a0-153">**Interface IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="757a0-153">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="757a0-154">Codes d’erreur et de réussite</span><span class="sxs-lookup"><span data-stu-id="757a0-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




