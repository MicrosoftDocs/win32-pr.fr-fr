---
description: Désactive l’utilisation des plug-ins de la caméra de l’après-traitement par le lecteur source.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: Attribut MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210364"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a><span data-ttu-id="0f96b-103">\_ \_ \_ Attribut plug-ins de désactivation de l' \_ appareil source \_ MF</span><span class="sxs-lookup"><span data-stu-id="0f96b-103">MF\_SOURCE\_READER\_DISABLE\_CAMERA\_PLUGINS attribute</span></span>

<span data-ttu-id="0f96b-104">Désactive l’utilisation des plug-ins de la caméra de l’après-traitement par le [lecteur source](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="0f96b-104">Disables the use of post-processing camera plug-ins by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="0f96b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0f96b-105">Data type</span></span>

<span data-ttu-id="0f96b-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0f96b-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0f96b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0f96b-107">Remarks</span></span>

<span data-ttu-id="0f96b-108">Cet attribut s’applique lorsque le lecteur source est utilisé avec une source de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="0f96b-108">This attribute applies when the Source Reader is used with a video capture source.</span></span> <span data-ttu-id="0f96b-109">Si cet attribut a la **valeur true**, il empêche le lecteur source de charger les plug-ins de publication que l’appareil photo peut fournir.</span><span class="sxs-lookup"><span data-stu-id="0f96b-109">If this attribute is **TRUE**, it prevents the Source Reader from loading any post-processing plug-ins that the camera might provide.</span></span> <span data-ttu-id="0f96b-110">Dans le cas contraire, le lecteur source les chargera par défaut.</span><span class="sxs-lookup"><span data-stu-id="0f96b-110">Otherwise, by default the Source Reader will load them.</span></span>

<span data-ttu-id="0f96b-111">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="0f96b-111">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="0f96b-112">Définissez l’attribut lorsque vous créez le lecteur source.</span><span class="sxs-lookup"><span data-stu-id="0f96b-112">Set the attribute when you create the source reader.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f96b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f96b-113">Requirements</span></span>



| <span data-ttu-id="0f96b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f96b-114">Requirement</span></span> | <span data-ttu-id="0f96b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f96b-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f96b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f96b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0f96b-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0f96b-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0f96b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f96b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0f96b-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="0f96b-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0f96b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f96b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f96b-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f96b-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f96b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f96b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f96b-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f96b-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0f96b-124">Attributs du lecteur source</span><span class="sxs-lookup"><span data-stu-id="0f96b-124">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




