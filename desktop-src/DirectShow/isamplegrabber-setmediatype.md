---
description: La méthode SetMediaType spécifie le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.
ms.assetid: 9568832f-6666-45c9-9421-485c877affb3
title: 'ISampleGrabber :: SetMediaType, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a39aa79e9311fe3491d0925fdc1b2dd3b1cc65c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541603"
---
# <a name="isamplegrabbersetmediatype-method"></a><span data-ttu-id="5235d-103">ISampleGrabber :: SetMediaType, méthode</span><span class="sxs-lookup"><span data-stu-id="5235d-103">ISampleGrabber::SetMediaType method</span></span>

> [!Note]  
> <span data-ttu-id="5235d-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5235d-104">\[Deprecated.</span></span> <span data-ttu-id="5235d-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5235d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5235d-106">La `SetMediaType` méthode spécifie le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="5235d-106">The `SetMediaType` method specifies the media type for the connection on the input pin of the Sample Grabber.</span></span>

## <a name="syntax"></a><span data-ttu-id="5235d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5235d-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a><span data-ttu-id="5235d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5235d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5235d-109">*pType*</span><span class="sxs-lookup"><span data-stu-id="5235d-109">*pType*</span></span> 
</dt> <dd>

<span data-ttu-id="5235d-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) spécifie le type de média requis.</span><span class="sxs-lookup"><span data-stu-id="5235d-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specifies the required media type.</span></span> <span data-ttu-id="5235d-111">Il n’est pas nécessaire de définir tous les membres de structure ; Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="5235d-111">It is not necessary to set all the structure members; see Remarks for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5235d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5235d-112">Return value</span></span>

<span data-ttu-id="5235d-113">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5235d-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5235d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5235d-114">Remarks</span></span>

<span data-ttu-id="5235d-115">Par défaut, l’exemple de la accroche n’a pas de type de média préféré.</span><span class="sxs-lookup"><span data-stu-id="5235d-115">By default, the Sample Grabber has no preferred media type.</span></span> <span data-ttu-id="5235d-116">Pour vous assurer que l’exemple d’accroche se connecte au filtre correct, appelez cette méthode avant de générer le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="5235d-116">To ensure that the Sample Grabber connects to the correct filter, call this method before building the filter graph.</span></span>

<span data-ttu-id="5235d-117">Cette méthode restreint la plage de types de médias que le filtre acceptera.</span><span class="sxs-lookup"><span data-stu-id="5235d-117">This method restricts the range of media types that the filter will accept.</span></span> <span data-ttu-id="5235d-118">Quand le filtre se connecte, il tente de faire correspondre le type de média donné dans *PTYPE*.</span><span class="sxs-lookup"><span data-stu-id="5235d-118">When the filter connects, it tries to match the media type given in *pType*.</span></span> <span data-ttu-id="5235d-119">Pour ce faire, il compare le type, le sous-type et les GUID de type de format principaux, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="5235d-119">To do so, it compares the major type, subtype, and format type GUIDs, in that order.</span></span> <span data-ttu-id="5235d-120">Pour chacun de ces GUID, si *PTYPE* a la valeur Guid \_ null, l’exemple de la accroche accepte le type de média sans aucune autre vérification.</span><span class="sxs-lookup"><span data-stu-id="5235d-120">For each of these GUIDs, if *pType* has the value GUID\_NULL, the Sample Grabber accepts the media type without any further checks.</span></span> <span data-ttu-id="5235d-121">Si *PTYPE* a une autre valeur, l’exemple d’accroche le compare au GUID dans le type de connexion.</span><span class="sxs-lookup"><span data-stu-id="5235d-121">If *pType* has any other value, the Sample Grabber compares it to the GUID in the connection type.</span></span> <span data-ttu-id="5235d-122">À moins que les deux GUID correspondent exactement, l’accroche d’échantillon rejette la connexion.</span><span class="sxs-lookup"><span data-stu-id="5235d-122">Unless the two GUIDs match exactly, the Sample Grabber rejects the connection.</span></span>

<span data-ttu-id="5235d-123">Pour les types de média vidéo, la accroche d’échantillon ignore le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="5235d-123">For video media types, the Sample Grabber ignores the format block.</span></span> <span data-ttu-id="5235d-124">Par conséquent, elle accepte toute taille vidéo et fréquence d’images.</span><span class="sxs-lookup"><span data-stu-id="5235d-124">Therefore, it will accept any video size and frame rate.</span></span> <span data-ttu-id="5235d-125">Quand vous appelez `SetMediaType` , affectez la valeur **null** au bloc de format (**pbFormat**) et la taille (**cbFormat**) à zéro.</span><span class="sxs-lookup"><span data-stu-id="5235d-125">When you call `SetMediaType`, set the format block (**pbFormat**) to **NULL** and the size (**cbFormat**) to zero.</span></span> <span data-ttu-id="5235d-126">Pour les types de média audio, l’exemple de accroche examine la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) et nécessite que l’autre filtre se connecte avec ce format, à moins que le bloc de format de *PTYPE* soit null ou que la balise format soit de **type** Wave \_ \_ PCM et que les autres membres de la structure soient nuls.</span><span class="sxs-lookup"><span data-stu-id="5235d-126">For audio media types, the Sample Grabber will examine the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure and will require the other filter to connect with that format — unless the format block in *pType* is **NULL**, or the format tag is WAVE\_FORMAT\_PCM and the other structure members are zero.</span></span>

<span data-ttu-id="5235d-127">Exemple 1 :</span><span class="sxs-lookup"><span data-stu-id="5235d-127">Example 1:</span></span>

-   <span data-ttu-id="5235d-128">Type majeur : \_ vidéo MediaType</span><span class="sxs-lookup"><span data-stu-id="5235d-128">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="5235d-129">Sous-type : GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="5235d-129">Subtype: GUID\_NULL</span></span>
-   <span data-ttu-id="5235d-130">Type de format : GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="5235d-130">Format type: GUID\_NULL</span></span>

<span data-ttu-id="5235d-131">L’exemple de la accroche accepte tout type de vidéo dans lequel le type de principal est égal à la vidéo de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="5235d-131">The Sample Grabber will accept any video type where the major type equals MEDIATYPE\_Video.</span></span> <span data-ttu-id="5235d-132">Il ne vérifie pas le sous-type.</span><span class="sxs-lookup"><span data-stu-id="5235d-132">It will not check the subtype.</span></span>

<span data-ttu-id="5235d-133">Exemple 2 :</span><span class="sxs-lookup"><span data-stu-id="5235d-133">Example 2:</span></span>

-   <span data-ttu-id="5235d-134">Type majeur : \_ vidéo MediaType</span><span class="sxs-lookup"><span data-stu-id="5235d-134">Major type: MEDIATYPE\_Video</span></span>
-   <span data-ttu-id="5235d-135">Sous-type : MEDIASUBTYPE \_ Rgb24</span><span class="sxs-lookup"><span data-stu-id="5235d-135">Subtype: MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="5235d-136">Type de format : GUID \_ null</span><span class="sxs-lookup"><span data-stu-id="5235d-136">Format type: GUID\_NULL</span></span>

<span data-ttu-id="5235d-137">À présent, l’exemple de la accroche vérifie le sous-type et n’accepte que les vidéos RVB 24.</span><span class="sxs-lookup"><span data-stu-id="5235d-137">Now the Sample Grabber will check the subtype, and accept only RGB 24 video.</span></span>

<span data-ttu-id="5235d-138">**Limitations :** Quel que soit le type que vous avez défini, le filtre d’accroche d’échantillon rejette tous les types vidéo avec une orientation verticale ( *bihauteur* négative) ou un type de format \_ VideoInfo2.</span><span class="sxs-lookup"><span data-stu-id="5235d-138">**Limitations:** Regardless of what type you set, the Sample Grabber Filter rejects any video types with top-down orientation (negative *biHeight*), or with a format type of FORMAT\_VideoInfo2.</span></span> <span data-ttu-id="5235d-139">Dans ce cas, bien que la `SetMediaType` méthode aboutisse, le filtre ne se connecte pas.</span><span class="sxs-lookup"><span data-stu-id="5235d-139">In this case, although the `SetMediaType` method succeeds, the filter will not connect.</span></span>

> [!Note]  
> <span data-ttu-id="5235d-140">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="5235d-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5235d-141">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5235d-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5235d-142">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5235d-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5235d-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5235d-143">Requirements</span></span>



| <span data-ttu-id="5235d-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5235d-144">Requirement</span></span> | <span data-ttu-id="5235d-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="5235d-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5235d-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="5235d-146">Header</span></span><br/>  | <dl> <span data-ttu-id="5235d-147"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5235d-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5235d-148">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5235d-148">Library</span></span><br/> | <dl> <span data-ttu-id="5235d-149"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5235d-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5235d-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5235d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5235d-151">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="5235d-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="5235d-152">**Interface ISampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="5235d-152">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 
