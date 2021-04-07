---
description: La \_ \_ propriété DeviceFormat AudioEngine spécifie le format de l’appareil, qui est le format que l’utilisateur a sélectionné pour le flux de données qui circule entre le moteur audio et l’appareil de point de terminaison audio lorsque l’appareil fonctionne en mode partagé.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748901"
---
# <a name="pkey_audioengine_deviceformat"></a><span data-ttu-id="bd69c-103">\_AudioEngine \_ DeviceFormat</span><span class="sxs-lookup"><span data-stu-id="bd69c-103">PKEY\_AudioEngine\_DeviceFormat</span></span>

<span data-ttu-id="bd69c-104">La **propriété \_ \_ DeviceFormat AudioEngine** spécifie le format de l’appareil, qui est le format que l’utilisateur a sélectionné pour le flux de données qui circule entre le moteur audio et l’appareil de point de terminaison audio lorsque l’appareil fonctionne en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="bd69c-104">The **PKEY\_AudioEngine\_DeviceFormat** property specifies the device format, which is the format that the user has selected for the stream that flows between the audio engine and the audio endpoint device when the device operates in shared mode.</span></span> <span data-ttu-id="bd69c-105">Ce format peut ne pas être le meilleur format par défaut qu’une application en mode exclusif utilise.</span><span class="sxs-lookup"><span data-stu-id="bd69c-105">This format might not be the best default format for an exclusive-mode application to use.</span></span> <span data-ttu-id="bd69c-106">En règle générale, une application en mode exclusif détecte un format d’appareil approprié en effectuant un certain nombre d’appels à la méthode [**IAudioClient :: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="bd69c-106">Typically, an exclusive-mode application finds a suitable device format by making some number of calls to the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method.</span></span> <span data-ttu-id="bd69c-107">Pour plus d’informations, consultez [formats de périphérique](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="bd69c-107">For more information, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="bd69c-108">Le membre **VT** de la structure **PROPVARIANT** est défini sur l' \_ objet BLOB VT.</span><span class="sxs-lookup"><span data-stu-id="bd69c-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="bd69c-109">Le membre **BLOB** de la structure **PROPVARIANT** est une structure de type **BLOB** qui contient deux membres.</span><span class="sxs-lookup"><span data-stu-id="bd69c-109">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="bd69c-110">BLOB de membre **. cbSize** est une **valeur DWORD** qui spécifie le nombre d’octets dans la description de format.</span><span class="sxs-lookup"><span data-stu-id="bd69c-110">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="bd69c-111">BLOB de membre **. pBlobData** pointe vers une structure **WAVEFORMATEX** qui contient la description de format.</span><span class="sxs-lookup"><span data-stu-id="bd69c-111">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="bd69c-112">Pour plus d’informations sur les **objets BLOB**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="bd69c-112">For more information about **BLOB**, see the Windows SDK documentation.</span></span> <span data-ttu-id="bd69c-113">Pour plus d’informations sur **WAVEFORMATEX**, consultez la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="bd69c-113">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd69c-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd69c-114">Requirements</span></span>



| <span data-ttu-id="bd69c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd69c-115">Requirement</span></span> | <span data-ttu-id="bd69c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd69c-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd69c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd69c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bd69c-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd69c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bd69c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd69c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bd69c-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd69c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bd69c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd69c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd69c-122"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd69c-122"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd69c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd69c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd69c-124">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="bd69c-124">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="bd69c-125">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="bd69c-125">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




