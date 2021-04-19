---
description: Définit le pic &\# 0034 ; compartiment à fuite&\# 0034 ; paramètres (consultez la section Notes) pour l’encodage d’un fichier Windows Media. Ces paramètres sont utilisés pour le taux binaire de pointe. Définissez cet attribut à l’aide de l’interface IMFASFStreamConfig.
ms.assetid: 422d6d1b-4d29-4156-877b-8dc3bcb7580f
title: Attribut MF_ASFSTREAMCONFIG_LEAKYBUCKET2 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94c4cca3252d543d35bef37d70dcb612c24df6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544967"
---
# <a name="mf_asfstreamconfig_leakybucket2-attribute"></a><span data-ttu-id="02faf-105">\_ \_ Attribut LEAKYBUCKET2 ASFSTREAMCONFIG MF</span><span class="sxs-lookup"><span data-stu-id="02faf-105">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2 attribute</span></span>

<span data-ttu-id="02faf-106">Définit le pic des paramètres du compartiment perdu (consultez la section Notes) pour l’encodage d’un fichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="02faf-106">Sets the peak "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="02faf-107">Ces paramètres sont utilisés pour le taux binaire de pointe.</span><span class="sxs-lookup"><span data-stu-id="02faf-107">These parameters are used for the peak bit rate.</span></span> <span data-ttu-id="02faf-108">Définissez cet attribut à l’aide de l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="02faf-108">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="02faf-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="02faf-109">Data type</span></span>

<span data-ttu-id="02faf-110">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="02faf-110">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="02faf-111">Notes</span><span class="sxs-lookup"><span data-stu-id="02faf-111">Remarks</span></span>

<span data-ttu-id="02faf-112">La valeur de cet attribut est un tableau de trois **DWORD**, dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="02faf-112">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="02faf-113">Vitesse de transmission, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="02faf-113">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="02faf-114">Fenêtre de mémoire tampon, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="02faf-114">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="02faf-115">Saturation de la mémoire tampon initiale, en octets.</span><span class="sxs-lookup"><span data-stu-id="02faf-115">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="02faf-116">Pour plus d’informations sur le concept de compartiment avec fuites, consultez la rubrique [modèle de tampon de compartiment](the-leaky-bucket-buffer-model.md) perdu dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="02faf-116">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="02faf-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="02faf-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="02faf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02faf-118">Requirements</span></span>



| <span data-ttu-id="02faf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02faf-119">Requirement</span></span> | <span data-ttu-id="02faf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="02faf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="02faf-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02faf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="02faf-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02faf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="02faf-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="02faf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="02faf-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="02faf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="02faf-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="02faf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="02faf-126"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="02faf-126"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02faf-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02faf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02faf-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="02faf-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="02faf-129">Attributs ASF</span><span class="sxs-lookup"><span data-stu-id="02faf-129">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="02faf-130">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="02faf-130">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="02faf-131">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="02faf-131">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="02faf-132">**\_LEAKYBUCKET1 ASFSTREAMCONFIG \_ MF**</span><span class="sxs-lookup"><span data-stu-id="02faf-132">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**</span></span>](mf-asfstreamconfig-leakybucket1-attribute.md)
</dt> </dl>

 

 




