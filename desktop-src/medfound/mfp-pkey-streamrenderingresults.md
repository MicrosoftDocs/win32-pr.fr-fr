---
description: Spécifie les flux qui ont été connectés correctement à un récepteur multimédia.
ms.assetid: b5e45bfc-d91d-41b8-aaa4-72b3a23d869e
title: MFP_PKEY_StreamRenderingResults, propriété (mfplay. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6acf04f751e8611f3add3a62fc7b4406d757999e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318546"
---
# <a name="mfp_pkey_streamrenderingresults-property"></a><span data-ttu-id="d573a-103">\_Propriété StreamRenderingResults de la propriété HYPERmfp \_</span><span class="sxs-lookup"><span data-stu-id="d573a-103">MFP\_PKEY\_StreamRenderingResults property</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d573a-104">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d573a-104">Deprecated.</span></span> <span data-ttu-id="d573a-105">Cette API peut être supprimée dans les versions futures de Windows.</span><span class="sxs-lookup"><span data-stu-id="d573a-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="d573a-106">Les applications doivent utiliser la [session multimédia](media-session.md) pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="d573a-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="d573a-107">Spécifie les flux qui ont été connectés correctement à un récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="d573a-107">Specifies which streams were connected successfully to a media sink.</span></span>



<span data-ttu-id="d573a-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="d573a-108">Data type</span></span>

<span data-ttu-id="d573a-109">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="d573a-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="d573a-110">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="d573a-110">PROPVARIANT member</span></span>

<span data-ttu-id="d573a-111">Tableau de valeurs **DWORD** (**CAUL**)</span><span class="sxs-lookup"><span data-stu-id="d573a-111">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="d573a-112">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="d573a-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="d573a-113">**caul**</span><span class="sxs-lookup"><span data-stu-id="d573a-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="d573a-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d573a-114">Remarks</span></span>

<span data-ttu-id="d573a-115">Cette propriété peut être envoyée avec le **\_ type d’événement MFP \_ \_ MEDIAITEM \_ Set** Event.</span><span class="sxs-lookup"><span data-stu-id="d573a-115">This property can be sent with the **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event.</span></span>

<span data-ttu-id="d573a-116">La valeur de la propriété est un tableau de **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="d573a-116">The value of the property is an array of **HRESULT** s.</span></span> <span data-ttu-id="d573a-117">Les entrées de tableau correspondent aux flux sur l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="d573a-117">The array entries correspond to streams on the current media item.</span></span> <span data-ttu-id="d573a-118">Chaque entrée du tableau indique si le flux correspondant a été connecté à un récepteur multimédia, comme suit :</span><span class="sxs-lookup"><span data-stu-id="d573a-118">Each entry in the array indicates whether the corresponding stream was connected to a media sink, as follows:</span></span>

-   <span data-ttu-id="d573a-119">Si le flux est connecté à un récepteur multimédia, la valeur est **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d573a-119">If the stream is connected to a media sink, the value is **S\_OK**.</span></span>
-   <span data-ttu-id="d573a-120">Si le flux n’est pas sélectionné, la valeur est **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d573a-120">If the stream is not selected, the value is **S\_FALSE**.</span></span>
-   <span data-ttu-id="d573a-121">Si une erreur s’est produite lors de la tentative de connexion du flux, la valeur est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d573a-121">If an error occurred while attempting to connect the stream, the value is an error code.</span></span>

<span data-ttu-id="d573a-122">Si au moins un flux a été correctement connecté, la lecture est possible.</span><span class="sxs-lookup"><span data-stu-id="d573a-122">If at least one stream was connected successfully, playback is possible.</span></span> <span data-ttu-id="d573a-123">Par exemple, l’utilisateur peut avoir le codec nécessaire pour lire le flux audio, mais pas pour lire le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="d573a-123">For example, the user might have the codec needed to play the audio stream but not to play the video stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d573a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d573a-124">Requirements</span></span>



| <span data-ttu-id="d573a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d573a-125">Requirement</span></span> | <span data-ttu-id="d573a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d573a-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d573a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d573a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d573a-128">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d573a-128">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d573a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d573a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d573a-130">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d573a-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d573a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="d573a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d573a-132"><dt>Mfplay. h</dt></span><span class="sxs-lookup"><span data-stu-id="d573a-132"><dt>Mfplay.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d573a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d573a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d573a-134">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d573a-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="d573a-135">**\_événement de \_ jeu de MEDIAITEM MFP \_**</span><span class="sxs-lookup"><span data-stu-id="d573a-135">**MFP\_MEDIAITEM\_SET\_EVENT**</span></span>](/windows/desktop/api/mfplay/ns-mfplay-mfp_mediaitem_set_event)
</dt> </dl>

 

 




