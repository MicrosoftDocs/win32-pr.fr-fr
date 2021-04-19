---
description: Spécifie si le récepteur d’accrochage utilise l’horloge de présentation pour planifier des exemples.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Attribut MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531719"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a><span data-ttu-id="f5c82-103">SAMPLEGRABBERSINK MF- \_ \_ attribut ignorer l' \_ horloge</span><span class="sxs-lookup"><span data-stu-id="f5c82-103">MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute</span></span>

<span data-ttu-id="f5c82-104">Spécifie si le récepteur d’accrochage utilise l’horloge de présentation pour planifier des exemples.</span><span class="sxs-lookup"><span data-stu-id="f5c82-104">Specifies whether the sample-grabber sink uses the presentation clock to schedule samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5c82-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f5c82-105">Data type</span></span>

<span data-ttu-id="f5c82-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f5c82-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f5c82-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f5c82-107">Get/set</span></span>

<span data-ttu-id="f5c82-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f5c82-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f5c82-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f5c82-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5c82-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f5c82-110">Remarks</span></span>

<span data-ttu-id="f5c82-111">Vous pouvez définir cet attribut sur l’objet d’activation créé par la fonction [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="f5c82-111">You can set this attribute on the activation object created by the [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) function.</span></span> <span data-ttu-id="f5c82-112">Définissez l’attribut avant d’appeler la méthode [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sur l’objet d’activation.</span><span class="sxs-lookup"><span data-stu-id="f5c82-112">Set the attribute before calling the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method on the activation object.</span></span>

<span data-ttu-id="f5c82-113">Par défaut, lorsque le récepteur d’accrochage d’échantillon reçoit un exemple, il attend l’heure de présentation de l’exemple pour appeler le rappel de l’application.</span><span class="sxs-lookup"><span data-stu-id="f5c82-113">By default, when the sample-grabber sink receives a sample, it waits until the presentation time of the sample to invoke the application's callback.</span></span> <span data-ttu-id="f5c82-114">Si l’attribut de l' \_ horloge SAMPLEGRABBERSINK MF \_ \_ est différent de zéro, le récepteur d’accroche d’échantillon ignore l’horloge de présentation et appelle le rappel dès qu’il reçoit chaque échantillon.</span><span class="sxs-lookup"><span data-stu-id="f5c82-114">If the MF\_SAMPLEGRABBERSINK\_IGNORE\_CLOCK attribute is nonzero, the sample-grabber sink ignores the presentation clock and invokes the callback as soon as it receives each sample.</span></span>

<span data-ttu-id="f5c82-115">Utilisation recommandée :</span><span class="sxs-lookup"><span data-stu-id="f5c82-115">Recommended usage:</span></span>

-   <span data-ttu-id="f5c82-116">Si vous souhaitez traiter les exemples aussi rapidement que possible, affectez la **valeur true** à cet attribut.</span><span class="sxs-lookup"><span data-stu-id="f5c82-116">If you want to process samples as quickly as possible, set this attribute to **TRUE**.</span></span>
-   <span data-ttu-id="f5c82-117">Si vous souhaitez que les appels à la méthode de rappel soient synchronisés avec l’horloge, ne définissez pas cet attribut ou affectez-lui la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="f5c82-117">If you want the calls to the callback method to be synchronized with the clock, either do not set this attribute or set it to **FALSE**.</span></span> <span data-ttu-id="f5c82-118">Vous pouvez récupérer des échantillons légèrement avant l’horloge, tout en restant synchronisés, en définissant l’attribut de décalage de l' [**\_ heure d' \_ exemple \_ \_ MF SAMPLEGRABBERSINK**](mf-samplegrabbersink-sample-time-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="f5c82-118">You can get samples slightly ahead of the clock, while still remaining synchronized, by setting the [**MF\_SAMPLEGRABBERSINK\_SAMPLE\_TIME\_OFFSET**](mf-samplegrabbersink-sample-time-offset-attribute.md) attribute.</span></span>

<span data-ttu-id="f5c82-119">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f5c82-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c82-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5c82-120">Requirements</span></span>



| <span data-ttu-id="f5c82-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5c82-121">Requirement</span></span> | <span data-ttu-id="f5c82-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5c82-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c82-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5c82-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c82-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5c82-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f5c82-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f5c82-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c82-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f5c82-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f5c82-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5c82-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5c82-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5c82-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5c82-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5c82-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c82-130">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5c82-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5c82-131">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5c82-131">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




