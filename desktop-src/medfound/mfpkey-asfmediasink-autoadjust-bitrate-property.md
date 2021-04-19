---
description: Spécifie si le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission.
ms.assetid: 0a6f4dd4-4ad7-4aab-a33d-14b4716f9902
title: MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d22463f477eb5abc1bb84254ad312427ecef52
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535746"
---
# <a name="mfpkey_asfmediasink_autoadjust_bitrate-property"></a><span data-ttu-id="b659f-103">\_Propriété MFPKEY ASFMEDIASINK de vitesse de \_ \_ transmission</span><span class="sxs-lookup"><span data-stu-id="b659f-103">MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE property</span></span>

<span data-ttu-id="b659f-104">Spécifie si le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="b659f-104">Specifies whether the ASF media sink automatically adjusts the bit rate.</span></span>



<span data-ttu-id="b659f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b659f-105">Data type</span></span>

<span data-ttu-id="b659f-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="b659f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="b659f-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="b659f-107">PROPVARIANT member</span></span>

<span data-ttu-id="b659f-108">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="b659f-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="b659f-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="b659f-109">VT\_BOOL</span></span>

<span data-ttu-id="b659f-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="b659f-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="b659f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b659f-111">Remarks</span></span>

<span data-ttu-id="b659f-112">Si la valeur de cette propriété est \_ true, le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission du contenu ASF en réponse aux caractéristiques des flux multiplexés.</span><span class="sxs-lookup"><span data-stu-id="b659f-112">If the value of this property is VARIANT\_TRUE, the ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span>

<span data-ttu-id="b659f-113">Cette propriété affecte la façon dont le récepteur multimédia ASF se comporte lorsqu’un flux dépasse les paramètres « compartiment perdu » du récepteur :</span><span class="sxs-lookup"><span data-stu-id="b659f-113">This property affects how the ASF media sink behaves when a stream overflows the sink's "leaky bucket" parameters:</span></span>



| <span data-ttu-id="b659f-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b659f-114">Value</span></span>              | <span data-ttu-id="b659f-115">Comportement</span><span class="sxs-lookup"><span data-stu-id="b659f-115">Behavior</span></span>                                                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b659f-116">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="b659f-116">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="b659f-117">Le récepteur multimédia ASF ajuste automatiquement la vitesse de transmission du contenu ASF en réponse aux caractéristiques des flux en cours de multiplexage.</span><span class="sxs-lookup"><span data-stu-id="b659f-117">The ASF media sink automatically adjusts the bit rate of the ASF content in response to the characteristics of the streams being multiplexed.</span></span> |
| <span data-ttu-id="b659f-118">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="b659f-118">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="b659f-119">Le récepteur multimédia ASF utilise la valeur de vitesse de transmission de flux fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="b659f-119">The ASF media sink uses the stream bit rate value provided by the application.</span></span>                                                                |



 

<span data-ttu-id="b659f-120">La valeur par défaut **est \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b659f-120">The default value is **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="b659f-121">Définissez cette propriété lorsque vous configurez le récepteur multimédia ASF.</span><span class="sxs-lookup"><span data-stu-id="b659f-121">Set this property when you configure the ASF media sink.</span></span> <span data-ttu-id="b659f-122">L’utilisation dépend de la fonction que vous appelez pour créer le récepteur multimédia ASF :</span><span class="sxs-lookup"><span data-stu-id="b659f-122">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="b659f-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): interroge le pointeur [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) récupéré pour l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="b659f-123">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="b659f-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sur le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) spécifié dans le paramètre *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="b659f-124">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

<span data-ttu-id="b659f-125">Si vous affectez à cette propriété la \_ valeur variant true, le récepteur multimédia ASF définit l’indicateur de **\_ \_ \_ débit binaire MFASF multiplexer** sur le multiplexeur ASF.</span><span class="sxs-lookup"><span data-stu-id="b659f-125">Setting this property to VARIANT\_TRUE causes the ASF media sink to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag on the ASF multiplexer.</span></span> <span data-ttu-id="b659f-126">Consultez [**IMFASFMultiplexer :: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span><span class="sxs-lookup"><span data-stu-id="b659f-126">See [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags).</span></span>

<span data-ttu-id="b659f-127">Pour plus d’informations sur le concept de compartiment avec fuites, consultez la rubrique « modèle de tampon de compartiment perdu » dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="b659f-127">For more information about the leaky bucket concept, see the topic "The Leaky Bucket Buffer Model" in the Windows Media Format SDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b659f-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b659f-128">Requirements</span></span>



| <span data-ttu-id="b659f-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b659f-129">Requirement</span></span> | <span data-ttu-id="b659f-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b659f-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b659f-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b659f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b659f-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b659f-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b659f-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b659f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b659f-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b659f-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b659f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="b659f-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b659f-136"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b659f-136"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b659f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b659f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b659f-138">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b659f-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="b659f-139">**\_LEAKYBUCKET1 ASFSTREAMCONFIG \_ MF**</span><span class="sxs-lookup"><span data-stu-id="b659f-139">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> <dt>

[<span data-ttu-id="b659f-140">**\_LEAKYBUCKET2 ASFSTREAMCONFIG \_ MF**</span><span class="sxs-lookup"><span data-stu-id="b659f-140">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




