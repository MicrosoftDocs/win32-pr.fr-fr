---
description: Temps d’envoi de base pour le récepteur de média ASF, en millisecondes.
ms.assetid: 1b99845e-751a-4ec6-bd2d-e4644cd6863e
title: MFPKEY_ASFMEDIASINK_BASE_SENDTIME, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f9bc7f9d92a598a723e3eeee733f63b59d27d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106532171"
---
# <a name="mfpkey_asfmediasink_base_sendtime-property"></a><span data-ttu-id="54484-103">MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME, propriété</span><span class="sxs-lookup"><span data-stu-id="54484-103">MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME property</span></span>

<span data-ttu-id="54484-104">Temps d’envoi de base pour le récepteur de média ASF, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="54484-104">Base send time for the ASF media sink, in milliseconds.</span></span>



<span data-ttu-id="54484-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="54484-105">Data type</span></span>

<span data-ttu-id="54484-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="54484-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="54484-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="54484-107">PROPVARIANT member</span></span>

<span data-ttu-id="54484-108">**CORRESPONDANTE**</span><span class="sxs-lookup"><span data-stu-id="54484-108">**ULONG**</span></span>

<span data-ttu-id="54484-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="54484-109">VT\_UI4</span></span>

<span data-ttu-id="54484-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="54484-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="54484-111">Notes</span><span class="sxs-lookup"><span data-stu-id="54484-111">Remarks</span></span>

<span data-ttu-id="54484-112">L’heure d’envoi est l’heure à laquelle un paquet ASF est envoyé sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="54484-112">The send time is the time at which an ASF packet is sent across the network.</span></span> <span data-ttu-id="54484-113">Il ne correspond pas directement à l’heure de présentation des données dans le paquet.</span><span class="sxs-lookup"><span data-stu-id="54484-113">It does not correspond directly to the presentation time of the data in the packet.</span></span>

<span data-ttu-id="54484-114">Vous pouvez utiliser cette propriété pour configurer le récepteur multimédia ASF.</span><span class="sxs-lookup"><span data-stu-id="54484-114">You can use this property to configure the ASF media sink.</span></span> <span data-ttu-id="54484-115">L’utilisation dépend de la fonction que vous appelez pour créer le récepteur multimédia ASF :</span><span class="sxs-lookup"><span data-stu-id="54484-115">The usage depends on which function you call to create the ASF media sink:</span></span>

-   <span data-ttu-id="54484-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): interroge le pointeur [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) récupéré pour l’interface **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="54484-116">[**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink): Query the retrieved [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) pointer for the **IPropertyStore** interface.</span></span>

-   <span data-ttu-id="54484-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sur le pointeur [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) spécifié dans le paramètre *pContentInfo* .</span><span class="sxs-lookup"><span data-stu-id="54484-117">[**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate): Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) on the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer specified in the *pContentInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="54484-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54484-118">Requirements</span></span>



| <span data-ttu-id="54484-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54484-119">Requirement</span></span> | <span data-ttu-id="54484-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="54484-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="54484-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54484-121">Minimum supported client</span></span><br/> | <span data-ttu-id="54484-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54484-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="54484-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54484-123">Minimum supported server</span></span><br/> | <span data-ttu-id="54484-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54484-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="54484-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="54484-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="54484-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54484-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54484-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54484-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54484-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="54484-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




