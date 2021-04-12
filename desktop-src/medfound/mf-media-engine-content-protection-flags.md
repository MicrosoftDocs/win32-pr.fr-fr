---
description: Spécifie si le moteur multimédia doit lire du contenu protégé.
ms.assetid: 2A593499-BF40-440E-AF1D-3B0E7732489A
title: Attribut MF_MEDIA_ENGINE_CONTENT_PROTECTION_FLAGS (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e33feb8d3e1d7c216cfd0392a1fcf9df0100f924
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321517"
---
# <a name="mf_media_engine_content_protection_flags-attribute"></a><span data-ttu-id="b806b-103">\_ \_ \_ \_ Attribut indicateurs de protection du contenu Media Engine MF \_</span><span class="sxs-lookup"><span data-stu-id="b806b-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_FLAGS attribute</span></span>

<span data-ttu-id="b806b-104">Spécifie si le moteur multimédia doit lire du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="b806b-104">Specifies whether the Media Engine will play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="b806b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="b806b-105">Data type</span></span>

<span data-ttu-id="b806b-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b806b-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b806b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b806b-107">Remarks</span></span>

<span data-ttu-id="b806b-108">La valeur de cet attribut est **une opération or au niveau du bit** des indicateurs de l’énumération des [**indicateurs de protection du \_ moteur de Media \_ \_ \_ MF**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) .</span><span class="sxs-lookup"><span data-stu-id="b806b-108">The value of this attribute is a bitwise **OR** of flags from the [**MF\_MEDIA\_ENGINE\_PROTECTION\_FLAGS**](/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_protection_flags) enumeration.</span></span> <span data-ttu-id="b806b-109">Pour activer la lecture de contenu protégé, définissez l’indicateur **\_ Media \_ Engine \_ Enable \_ protected \_ content** .</span><span class="sxs-lookup"><span data-stu-id="b806b-109">To enable playback of protected content, set the **MF\_MEDIA\_ENGINE\_ENABLE\_PROTECTED\_CONTENT** flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="b806b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b806b-110">Requirements</span></span>



| <span data-ttu-id="b806b-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b806b-111">Requirement</span></span> | <span data-ttu-id="b806b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="b806b-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b806b-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b806b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b806b-114">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b806b-114">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="b806b-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b806b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b806b-116">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="b806b-116">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="b806b-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b806b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b806b-118"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="b806b-118"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b806b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b806b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b806b-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b806b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b806b-121">Attributs du moteur multimédia</span><span class="sxs-lookup"><span data-stu-id="b806b-121">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="b806b-122">**IMFMediaEngineClassFactory :: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="b806b-122">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




