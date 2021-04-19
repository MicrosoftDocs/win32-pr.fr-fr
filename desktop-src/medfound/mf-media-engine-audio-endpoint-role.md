---
description: Spécifie le rôle d’appareil pour le flux audio.
ms.assetid: E4B7660D-5F41-495A-B77D-94B7981F4C2C
title: Attribut MF_MEDIA_ENGINE_AUDIO_ENDPOINT_ROLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b1b00115a28592140e41463cf296acf54ad7cde
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535737"
---
# <a name="mf_media_engine_audio_endpoint_role-attribute"></a><span data-ttu-id="6250b-103">\_Attribut de \_ rôle de \_ point de terminaison audio du moteur multimédia \_ MF \_</span><span class="sxs-lookup"><span data-stu-id="6250b-103">MF\_MEDIA\_ENGINE\_AUDIO\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="6250b-104">Spécifie le rôle d’appareil pour le flux audio.</span><span class="sxs-lookup"><span data-stu-id="6250b-104">Specifies the device role for the audio stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="6250b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="6250b-105">Data type</span></span>

<span data-ttu-id="6250b-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stocké en tant que **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6250b-106">**[**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6250b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6250b-107">Remarks</span></span>

<span data-ttu-id="6250b-108">La valeur de cet attribut est un membre de l’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="6250b-108">The value of this attribute is a member of the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>

<span data-ttu-id="6250b-109">Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="6250b-109">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span> <span data-ttu-id="6250b-110">L’attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6250b-110">The attribute is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6250b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6250b-111">Requirements</span></span>



| <span data-ttu-id="6250b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6250b-112">Requirement</span></span> | <span data-ttu-id="6250b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6250b-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6250b-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6250b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6250b-115">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="6250b-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                            |
| <span data-ttu-id="6250b-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6250b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6250b-117">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="6250b-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6250b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="6250b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6250b-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6250b-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6250b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6250b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6250b-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6250b-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
