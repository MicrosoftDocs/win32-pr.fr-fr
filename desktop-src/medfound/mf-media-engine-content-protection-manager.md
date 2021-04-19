---
description: Permet au moteur multimédia de lire du contenu protégé.
ms.assetid: F6F17EC7-6553-4127-B691-C20C945DD4D8
title: Attribut MF_MEDIA_ENGINE_CONTENT_PROTECTION_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb99d1df36c9b9adbf1c099d619df60e1144b87
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537166"
---
# <a name="mf_media_engine_content_protection_manager-attribute"></a><span data-ttu-id="7a4c9-103">\_Attribut Media \_ Engine \_ Content \_ protection \_ Manager MF</span><span class="sxs-lookup"><span data-stu-id="7a4c9-103">MF\_MEDIA\_ENGINE\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="7a4c9-104">Permet au moteur multimédia de lire du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="7a4c9-104">Enables the Media Engine to play protected content.</span></span>

## <a name="data-type"></a><span data-ttu-id="7a4c9-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7a4c9-105">Data type</span></span>

<span data-ttu-id="7a4c9-106">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="7a4c9-106">**IUnknown\***</span></span>

## <a name="remarks"></a><span data-ttu-id="7a4c9-107">Notes</span><span class="sxs-lookup"><span data-stu-id="7a4c9-107">Remarks</span></span>

<span data-ttu-id="7a4c9-108">La valeur de cet attribut est un pointeur vers l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="7a4c9-108">The value of this attribute is a pointer to the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span> <span data-ttu-id="7a4c9-109">L’appelant doit implémenter l’interface.</span><span class="sxs-lookup"><span data-stu-id="7a4c9-109">The caller must implement the interface.</span></span>

<span data-ttu-id="7a4c9-110">Cet attribut peut être l’un des attributs passés à [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span><span class="sxs-lookup"><span data-stu-id="7a4c9-110">This attribute can be one of the attributes passed to [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance).</span></span> <span data-ttu-id="7a4c9-111">Il est obligatoire si le contenu protégé doit être lu.</span><span class="sxs-lookup"><span data-stu-id="7a4c9-111">It is required if protected content is to be played.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a4c9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a4c9-112">Requirements</span></span>



| <span data-ttu-id="7a4c9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a4c9-113">Requirement</span></span> | <span data-ttu-id="7a4c9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a4c9-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4c9-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a4c9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7a4c9-116">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="7a4c9-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="7a4c9-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a4c9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7a4c9-118">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="7a4c9-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="7a4c9-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a4c9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a4c9-120"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a4c9-120"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a4c9-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a4c9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a4c9-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7a4c9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7a4c9-123">**IMFMediaEngineClassFactory :: CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="7a4c9-123">**IMFMediaEngineClassFactory::CreateInstance**</span></span>](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




