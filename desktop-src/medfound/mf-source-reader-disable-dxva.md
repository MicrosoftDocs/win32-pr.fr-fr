---
description: Spécifie si le lecteur source active DirectX Video Acceleration (DXVA) sur le décodeur vidéo.
ms.assetid: ec539038-3fd3-41b7-a0e6-e75e3f2828a7
title: Attribut MF_SOURCE_READER_DISABLE_DXVA (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9362f067d1d6ceae426e9ee6530e08b95837595f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320470"
---
# <a name="mf_source_reader_disable_dxva-attribute"></a><span data-ttu-id="f7cc7-103">\_ \_ \_ Attribut DXVA de désactivation de lecteur source \_ MF</span><span class="sxs-lookup"><span data-stu-id="f7cc7-103">MF\_SOURCE\_READER\_DISABLE\_DXVA attribute</span></span>

<span data-ttu-id="f7cc7-104">Spécifie si le [lecteur source](source-reader.md) active DirectX Video Acceleration (DXVA) sur le décodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-104">Specifies whether the [Source Reader](source-reader.md) enables DirectX Video Acceleration (DXVA) on the video decoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="f7cc7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f7cc7-105">Data type</span></span>

<span data-ttu-id="f7cc7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f7cc7-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="f7cc7-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f7cc7-107">Get/set</span></span>

<span data-ttu-id="f7cc7-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f7cc7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f7cc7-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f7cc7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7cc7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="f7cc7-110">Remarks</span></span>

<span data-ttu-id="f7cc7-111">Cet attribut s’applique si les conditions suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="f7cc7-111">This attribute applies if the following conditions are true:</span></span>

-   <span data-ttu-id="f7cc7-112">Le lecteur source décode un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-112">The source reader decodes a video stream.</span></span>
-   <span data-ttu-id="f7cc7-113">Le décodeur vidéo prend en charge le décodage DXVA.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-113">The video decoder supports DXVA decoding.</span></span>
-   <span data-ttu-id="f7cc7-114">L’application utilise l’attribut du [ \_ \_ \_ \_ Gestionnaire D3D du lecteur source MF](mf-source-reader-d3d-manager.md) pour définir le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) sur le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-114">The application uses the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute to set the [Direct3D Device Manager](direct3d-device-manager.md) on the source reader.</span></span>

<span data-ttu-id="f7cc7-115">Cet attribut permet à l’application de désactiver DXVA tout en décodant toujours les surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-115">This attribute enables the application to disable DXVA while still decoding to Direct3D surfaces.</span></span>

<span data-ttu-id="f7cc7-116">Par défaut, le lecteur source utilise le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) pour deux raisons :</span><span class="sxs-lookup"><span data-stu-id="f7cc7-116">By default, the source reader uses the [Direct3D Device Manager](direct3d-device-manager.md) for two purposes:</span></span>

-   <span data-ttu-id="f7cc7-117">Pour activer le décodage DXVA dans le décodeur vidéo.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-117">To enable DXVA decoding in the video decoder.</span></span>
-   <span data-ttu-id="f7cc7-118">Pour allouer des surfaces Direct3D pour les exemples vidéo.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-118">To allocate Direct3D surfaces for the video samples.</span></span>

<span data-ttu-id="f7cc7-119">Si la valeur de l' \_ \_ \_ attribut DXVA de désactivation de l' \_ attribut DXVA est **true**, le lecteur source désactive le décodage DXVA, bien qu’il utilise toujours le [Gestionnaire de périphériques Direct3D](direct3d-device-manager.md) pour allouer des surfaces Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-119">If the value of the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is **TRUE**, the source reader does disables DXVA decoding, although it still uses the [Direct3D Device Manager](direct3d-device-manager.md) to allocate Direct3D surfaces.</span></span>

<span data-ttu-id="f7cc7-120">Si l’attribut du [ \_ \_ \_ \_ Gestionnaire D3D du lecteur source MF](mf-source-reader-d3d-manager.md) n’est pas défini, l' \_ attribut DXVA du lecteur source MF de \_ \_ désactivation \_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-120">If the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute is not set, the MF\_SOURCE\_READER\_DISABLE\_DXVA attribute is ignored.</span></span>

<span data-ttu-id="f7cc7-121">La valeur par défaut de cet attribut est **false**, ce qui signifie que le décodage DXVA est activé lorsqu’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="f7cc7-121">The default value of this attribute is **FALSE**, meaning that DXVA decoding is enabled when available.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7cc7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7cc7-122">Requirements</span></span>



| <span data-ttu-id="f7cc7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7cc7-123">Requirement</span></span> | <span data-ttu-id="f7cc7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7cc7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7cc7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7cc7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f7cc7-126">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f7cc7-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f7cc7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7cc7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f7cc7-128">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f7cc7-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f7cc7-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7cc7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7cc7-130"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7cc7-130"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7cc7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7cc7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7cc7-132">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f7cc7-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f7cc7-133">Lecteur source</span><span class="sxs-lookup"><span data-stu-id="f7cc7-133">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="f7cc7-134">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="f7cc7-134">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




