---
description: Spécifie le &\# 0034 ; compartiment avec fuite&\# 0034 ; paramètres pour un flux sur un récepteur multimédia ASF.
ms.assetid: b01e59b6-0a7f-4125-867c-532385a27c15
title: MFPKEY_ASFSTREAMSINK_CORRECTED_LEAKYBUCKET, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a4ebc2dc41a1f43906aff5d2fe8caea8d53057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862954"
---
# <a name="mfpkey_asfstreamsink_corrected_leakybucket-property"></a><span data-ttu-id="68b2a-103">MFPKEY \_ ASFSTREAMSINK \_ corrigé \_ LEAKYBUCKET, propriété</span><span class="sxs-lookup"><span data-stu-id="68b2a-103">MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET property</span></span>

<span data-ttu-id="68b2a-104">Spécifie les paramètres de « compartiment perdu » (consultez la section Notes) pour un flux sur un récepteur multimédia ASF.</span><span class="sxs-lookup"><span data-stu-id="68b2a-104">Specifies the "leaky bucket" parameters (see Remarks) for a stream on an ASF media sink.</span></span>



<span data-ttu-id="68b2a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="68b2a-105">Data type</span></span>

<span data-ttu-id="68b2a-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="68b2a-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="68b2a-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="68b2a-107">PROPVARIANT member</span></span>

<span data-ttu-id="68b2a-108">Tableau de valeurs **DWORD** (**CAUL**)</span><span class="sxs-lookup"><span data-stu-id="68b2a-108">Array of **DWORD** values (**CAUL**)</span></span>

<span data-ttu-id="68b2a-109">VT \_ Vector \| VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="68b2a-109">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="68b2a-110">**caul**</span><span class="sxs-lookup"><span data-stu-id="68b2a-110">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="68b2a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="68b2a-111">Remarks</span></span>

<span data-ttu-id="68b2a-112">Une application peut définir cette propriété sur un flux du récepteur de média ASF une fois que le type de média du flux est négocié.</span><span class="sxs-lookup"><span data-stu-id="68b2a-112">An application can set this property on a stream of the ASF media sink after the media type for the stream is negotiated.</span></span> <span data-ttu-id="68b2a-113">Utilisez cette propriété pour spécifier la fenêtre de mémoire tampon réelle que le codec Windows Media utilisera.</span><span class="sxs-lookup"><span data-stu-id="68b2a-113">Use this property to specify the actual buffer window that the Windows Media codec will use.</span></span> <span data-ttu-id="68b2a-114">Vous pouvez obtenir ces informations à partir du codec à l’aide de l’interface **IWMCodecLeakyBucket** , qui est documentée dans le kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="68b2a-114">You can obtain this information from the codec by using the **IWMCodecLeakyBucket** interface, which is documented in the Windows Media Format SDK.</span></span>

<span data-ttu-id="68b2a-115">La valeur de cette propriété est un tableau de trois valeurs **DWORD** dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="68b2a-115">The value of this property is an array of three **DWORD** values in the following order:</span></span>

-   <span data-ttu-id="68b2a-116">Vitesse de transmission, en bits par seconde.</span><span class="sxs-lookup"><span data-stu-id="68b2a-116">Bit rate, in bits per second.</span></span>
-   <span data-ttu-id="68b2a-117">Taille de la mémoire tampon, en octets.</span><span class="sxs-lookup"><span data-stu-id="68b2a-117">Buffer size, in bytes.</span></span>
-   <span data-ttu-id="68b2a-118">Saturation de la mémoire tampon initiale, en octets.</span><span class="sxs-lookup"><span data-stu-id="68b2a-118">Initial buffer fullness, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b2a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="68b2a-119">Requirements</span></span>



| <span data-ttu-id="68b2a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="68b2a-120">Requirement</span></span> | <span data-ttu-id="68b2a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="68b2a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68b2a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68b2a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68b2a-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68b2a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68b2a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="68b2a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68b2a-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="68b2a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="68b2a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="68b2a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68b2a-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68b2a-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b2a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="68b2a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b2a-129">**IMFStreamSink**</span><span class="sxs-lookup"><span data-stu-id="68b2a-129">**IMFStreamSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)
</dt> <dt>

[<span data-ttu-id="68b2a-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="68b2a-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




