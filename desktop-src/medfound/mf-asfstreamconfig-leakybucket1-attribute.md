---
description: Définit la moyenne &\# 0034 ; compartiment à fuite&\# 0034 ; paramètres (consultez la section Notes) pour l’encodage d’un fichier Windows Media. Définissez cet attribut à l’aide de l’interface IMFASFStreamConfig.
ms.assetid: 5aa570eb-1004-4942-9a63-b8f6373d4e53
title: Attribut MF_ASFSTREAMCONFIG_LEAKYBUCKET1 (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4db383d19ff5009ccc9fc3203281e04000870474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529744"
---
# <a name="mf_asfstreamconfig_leakybucket1-attribute"></a><span data-ttu-id="29b6c-104">\_ \_ Attribut LEAKYBUCKET1 ASFSTREAMCONFIG MF</span><span class="sxs-lookup"><span data-stu-id="29b6c-104">MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1 attribute</span></span>

<span data-ttu-id="29b6c-105">Définit les paramètres de la « plage perdue » moyenne (consultez la section Notes) pour l’encodage d’un fichier Windows Media.</span><span class="sxs-lookup"><span data-stu-id="29b6c-105">Sets the average "leaky bucket" parameters (see Remarks) for encoding a Windows Media file.</span></span> <span data-ttu-id="29b6c-106">Définissez cet attribut à l’aide de l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="29b6c-106">Set this attribute by using the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

## <a name="data-type"></a><span data-ttu-id="29b6c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="29b6c-107">Data type</span></span>

<span data-ttu-id="29b6c-108">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="29b6c-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="29b6c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="29b6c-109">Remarks</span></span>

<span data-ttu-id="29b6c-110">La valeur de cet attribut est un tableau de trois **DWORD**, dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="29b6c-110">The value of this attribute is an array of three **DWORD** s, in the following order:</span></span>

-   <span data-ttu-id="29b6c-111">Vitesse de transmission, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="29b6c-111">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="29b6c-112">Fenêtre de mémoire tampon, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="29b6c-112">Buffer window, in milliseconds.</span></span>
-   <span data-ttu-id="29b6c-113">Saturation de la mémoire tampon initiale, en octets.</span><span class="sxs-lookup"><span data-stu-id="29b6c-113">Initial buffer fullness, in bytes.</span></span>

<span data-ttu-id="29b6c-114">Pour plus d’informations sur le concept de compartiment avec fuites, consultez la rubrique [modèle de tampon de compartiment](the-leaky-bucket-buffer-model.md) perdu dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="29b6c-114">For more information about the leaky bucket concept, see the topic [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md) in the Windows Media Format SDK documentation.</span></span>

<span data-ttu-id="29b6c-115">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="29b6c-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="29b6c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29b6c-116">Requirements</span></span>



| <span data-ttu-id="29b6c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29b6c-117">Requirement</span></span> | <span data-ttu-id="29b6c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="29b6c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="29b6c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29b6c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29b6c-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29b6c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="29b6c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29b6c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29b6c-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29b6c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="29b6c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="29b6c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="29b6c-124"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="29b6c-124"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29b6c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29b6c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29b6c-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29b6c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="29b6c-127">Attributs ASF</span><span class="sxs-lookup"><span data-stu-id="29b6c-127">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="29b6c-128">**IMFAttributes :: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="29b6c-128">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="29b6c-129">**IMFAttributes :: SetBlob**</span><span class="sxs-lookup"><span data-stu-id="29b6c-129">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="29b6c-130">**\_LEAKYBUCKET2 ASFSTREAMCONFIG \_ MF**</span><span class="sxs-lookup"><span data-stu-id="29b6c-130">**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**</span></span>](mf-asfstreamconfig-leakybucket2-attribute.md)
</dt> </dl>

 

 




