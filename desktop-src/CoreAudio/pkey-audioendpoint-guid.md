---
description: La propriété AudioEndpoint de la valeur de la valeur de la propriété GUID de la propriété de la \_ \_ valeur de fichier
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515578"
---
# <a name="pkey_audioendpoint_guid"></a><span data-ttu-id="7fcfe-103">GUID de AudioEndpoint de la \_ \_</span><span class="sxs-lookup"><span data-stu-id="7fcfe-103">PKEY\_AudioEndpoint\_GUID</span></span>

<span data-ttu-id="7fcfe-104">La **propriété \_ AudioEndpoint \_** de la valeur de la valeur de la propriété GUID de la propriété de la valeur de fichier</span><span class="sxs-lookup"><span data-stu-id="7fcfe-104">The **PKEY\_AudioEndpoint\_GUID** property supplies the DirectSound device identifier that corresponds to the audio endpoint device.</span></span> <span data-ttu-id="7fcfe-105">La valeur de la propriété est un GUID que le client peut fournir comme identificateur d’appareil à la fonction **DirectSoundCreate** ou **DIRECTSOUNDCAPTURECREATE** dans l’API DirectSound.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-105">The property value is a GUID that the client can supply as the device identifier to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function in the DirectSound API.</span></span> <span data-ttu-id="7fcfe-106">Cette valeur identifie de façon unique l’appareil de point de terminaison audio sur tous les périphériques de point de terminaison audio du système.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-106">This value uniquely identifies the audio endpoint device across all audio endpoint devices in the system.</span></span> <span data-ttu-id="7fcfe-107">Pour plus d’informations sur DirectSound, consultez la documentation du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-107">For more information about DirectSound, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="7fcfe-108">Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-108">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="7fcfe-109">Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID qui identifie l’appareil de point de terminaison audio dans DirectSound.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-109">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains a GUID that identifies the audio endpoint device in DirectSound.</span></span>

<span data-ttu-id="7fcfe-110">Comme expliqué précédemment, l' [API MMDevice](mmdevice-api.md) prend en charge les [rôles d’appareil](device-roles.md).</span><span class="sxs-lookup"><span data-stu-id="7fcfe-110">As explained previously, the [MMDevice API](mmdevice-api.md) supports [device roles](device-roles.md).</span></span> <span data-ttu-id="7fcfe-111">Bien que DirectSound ne prenne pas directement en charge les rôles d’appareil, un client DirectSound peut utiliser la \_ \_ propriété GUID AudioEndpoint de type de périphérique pour sélectionner un appareil de rendu ou de capture DirectSound en fonction de son rôle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-111">Although DirectSound does not directly support device roles, a DirectSound client can use the PKEY\_AudioEndpoint\_GUID property to select a DirectSound rendering or capture device based on its device role.</span></span>

<span data-ttu-id="7fcfe-112">Par exemple, une application DirectSound effectue les étapes suivantes pour créer un appareil DirectSound qui correspond à l’appareil de point de terminaison de rendu auquel l’utilisateur a affecté le rôle eMultimedia :</span><span class="sxs-lookup"><span data-stu-id="7fcfe-112">For example, a DirectSound application performs the following steps to create a DirectSound device that corresponds to the rendering endpoint device that the user has assigned the eMultimedia role to:</span></span>

1.  <span data-ttu-id="7fcfe-113">Appelez la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour accéder à l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) de l’appareil de point de terminaison de rendu qui a le rôle eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-113">Call the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to get the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the rendering endpoint device that has the eMultimedia role.</span></span>
2.  <span data-ttu-id="7fcfe-114">Appelez la méthode [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) pour obtenir l’interface **IPropertyStore** de l’appareil eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-114">Call the [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) method to obtain the **IPropertyStore** interface of the eMultimedia device.</span></span> <span data-ttu-id="7fcfe-115">Pour plus d’informations sur **IPropertyStore**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-115">For more information about **IPropertyStore**, see the Windows SDK documentation.</span></span>
3.  <span data-ttu-id="7fcfe-116">Appelez la méthode **IPropertyStore :: GetValue** pour obtenir la valeur de la \_ \_ propriété GUID AudioEndpoint GUID.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-116">Call the **IPropertyStore::GetValue** method to obtain the PKEY\_AudioEndpoint\_GUID property value.</span></span>
4.  <span data-ttu-id="7fcfe-117">Convertit la valeur de propriété d’un GUID sous forme de chaîne en une structure GUID de 16 octets.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-117">Convert the property value from a GUID in string format to a 16-byte GUID structure.</span></span>
5.  <span data-ttu-id="7fcfe-118">Appelez la fonction **DirectSoundCreate** avec le GUID pour créer l’appareil avec le rôle eMultimedia.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-118">Call the **DirectSoundCreate** function with the GUID to create the device with the eMultimedia role.</span></span>

> [!Note]  
> <span data-ttu-id="7fcfe-119">A-la **\_ AudioEndpoint \_ GUID** est une propriété en lecture seule, quel que soit le mode d’accès au stockage demandé par l’application dans [**IMMDevice :: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span><span class="sxs-lookup"><span data-stu-id="7fcfe-119">**PKEY\_AudioEndpoint\_GUID** is a read-only property regardless of the storage-access mode requested by the application in [**IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore).</span></span> <span data-ttu-id="7fcfe-120">Si une application tente de définir une valeur à l’aide de **IPropertyStore :: SetValue**, cet appel échoue avec le \_ code d’erreur E ACCESSDENIED.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-120">If an application attempts to set a value by using **IPropertyStore::SetValue**, this call fails with the E\_ACCESSDENIED error code.</span></span>

 

<span data-ttu-id="7fcfe-121">Notez que le GUID de 16 octets généré à l’étape 4 correspond au GUID de l’appareil qui identifie l’appareil lors de l’énumération de l’appareil DirectSound.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-121">Note that the 16-byte GUID generated in step 4 matches the device GUID that identifies the device during DirectSound device enumeration.</span></span> <span data-ttu-id="7fcfe-122">La fonction **DirectSoundEnumerate** énumère les appareils de point de terminaison de rendu et la fonction **DirectSoundCaptureEnumerate** énumère les appareils de point de terminaison de capture.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-122">The **DirectSoundEnumerate** function enumerates rendering endpoint devices, and the **DirectSoundCaptureEnumerate** function enumerates capture endpoint devices.</span></span> <span data-ttu-id="7fcfe-123">Dans les deux cas, le GUID du périphérique est le premier paramètre passé à la fonction de rappel d’énumération.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-123">In either case, the device GUID is the first parameter passed to the enumeration callback function.</span></span> <span data-ttu-id="7fcfe-124">Pour plus d’informations sur l’énumération DirectSound, consultez la documentation du kit de développement logiciel (SDK) DirectX.</span><span class="sxs-lookup"><span data-stu-id="7fcfe-124">For more information about DirectSound enumeration, see the DirectX SDK documentation.</span></span>

<span data-ttu-id="7fcfe-125">Pour obtenir un exemple de code qui utilise \_ la \_ propriété GUID AudioEndpoint de la page de codes, consultez [rôles d’appareil pour les applications DirectSound](device-roles-for-directsound-applications.md).</span><span class="sxs-lookup"><span data-stu-id="7fcfe-125">For a code example that uses the PKEY\_AudioEndpoint\_GUID property, see [Device Roles for DirectSound Applications](device-roles-for-directsound-applications.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcfe-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fcfe-126">Requirements</span></span>



| <span data-ttu-id="7fcfe-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fcfe-127">Requirement</span></span> | <span data-ttu-id="7fcfe-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fcfe-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcfe-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fcfe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcfe-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fcfe-130">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7fcfe-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fcfe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcfe-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7fcfe-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7fcfe-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fcfe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcfe-134"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcfe-134"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcfe-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fcfe-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcfe-136">**Propriétés du point de terminaison audio**</span><span class="sxs-lookup"><span data-stu-id="7fcfe-136">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="7fcfe-137">Propriétés audio principales</span><span class="sxs-lookup"><span data-stu-id="7fcfe-137">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




