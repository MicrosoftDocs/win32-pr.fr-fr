---
title: Interface IMsRdpClientAdvancedSettings7
description: Expose des méthodes et des propriétés qui gèrent les paramètres avancés du contrôle ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512373"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a><span data-ttu-id="80bbb-105">Interface IMsRdpClientAdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="80bbb-105">IMsRdpClientAdvancedSettings7 interface</span></span>

<span data-ttu-id="80bbb-106">Expose des méthodes et des propriétés qui gèrent les paramètres avancés du contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="80bbb-106">Exposes methods and properties that manage advanced settings of the ActiveX control.</span></span>

<span data-ttu-id="80bbb-107">Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="80bbb-107">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="80bbb-108">Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings7** à **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="80bbb-108">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings7** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="80bbb-109">Membres</span><span class="sxs-lookup"><span data-stu-id="80bbb-109">Members</span></span>

<span data-ttu-id="80bbb-110">L’interface **IMsRdpClientAdvancedSettings7** hérite de **IMsRdpClientAdvancedSettings6**.</span><span class="sxs-lookup"><span data-stu-id="80bbb-110">The **IMsRdpClientAdvancedSettings7** interface inherits from **IMsRdpClientAdvancedSettings6**.</span></span> <span data-ttu-id="80bbb-111">**IMsRdpClientAdvancedSettings7** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80bbb-111">**IMsRdpClientAdvancedSettings7** also has these types of members:</span></span>

-   [<span data-ttu-id="80bbb-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80bbb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80bbb-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80bbb-113">Properties</span></span>

<span data-ttu-id="80bbb-114">L’interface **IMsRdpClientAdvancedSettings7** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="80bbb-114">The **IMsRdpClientAdvancedSettings7** interface has these properties.</span></span>



| <span data-ttu-id="80bbb-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="80bbb-115">Property</span></span>                                                                                                    | <span data-ttu-id="80bbb-116">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="80bbb-116">Access type</span></span>           | <span data-ttu-id="80bbb-117">Description</span><span class="sxs-lookup"><span data-stu-id="80bbb-117">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="80bbb-118">**AudioCaptureRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="80bbb-118">**AudioCaptureRedirectionMode**</span></span>](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | <span data-ttu-id="80bbb-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80bbb-119">Read/write</span></span><br/> | <span data-ttu-id="80bbb-120">Spécifie ou récupère une valeur qui indique si le périphérique d’entrée audio par défaut est redirigé du client vers la session à distance.</span><span class="sxs-lookup"><span data-stu-id="80bbb-120">Specifies or retrieves a value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span><br/> |
| [<span data-ttu-id="80bbb-121">**AudioQualityMode**</span><span class="sxs-lookup"><span data-stu-id="80bbb-121">**AudioQualityMode**</span></span>](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | <span data-ttu-id="80bbb-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80bbb-122">Read/write</span></span><br/> | <span data-ttu-id="80bbb-123">Spécifie ou récupère une valeur qui indique le paramètre de mode de qualité audio pour le son Redirigé.</span><span class="sxs-lookup"><span data-stu-id="80bbb-123">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span><br/>                                        |
| [<span data-ttu-id="80bbb-124">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="80bbb-124">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | <span data-ttu-id="80bbb-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80bbb-125">Read/write</span></span><br/> | <span data-ttu-id="80bbb-126">Spécifie ou récupère une valeur qui indique si SuperPan est activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="80bbb-126">Specifies or retrieves a value that indicates whether SuperPan is enabled or disabled.</span></span><br/>                                                    |
| [<span data-ttu-id="80bbb-127">**NetworkConnectionType**</span><span class="sxs-lookup"><span data-stu-id="80bbb-127">**NetworkConnectionType**</span></span>](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | <span data-ttu-id="80bbb-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80bbb-128">Read/write</span></span><br/> | <span data-ttu-id="80bbb-129">Spécifie ou récupère une valeur qui indique le type de connexion réseau.</span><span class="sxs-lookup"><span data-stu-id="80bbb-129">Specifies or retrieves a value that indicates the network connection type.</span></span><br/>                                                                |
| [<span data-ttu-id="80bbb-130">**RedirectDirectX**</span><span class="sxs-lookup"><span data-stu-id="80bbb-130">**RedirectDirectX**</span></span>](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | <span data-ttu-id="80bbb-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80bbb-131">Read/write</span></span><br/> | <span data-ttu-id="80bbb-132">Cette propriété n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="80bbb-132">This property is not used.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="80bbb-133">**SuperPanAccelerationFactor**</span><span class="sxs-lookup"><span data-stu-id="80bbb-133">**SuperPanAccelerationFactor**</span></span>](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | <span data-ttu-id="80bbb-134">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80bbb-134">Read/write</span></span><br/> | <span data-ttu-id="80bbb-135">Spécifie ou récupère une valeur qui indique le facteur d’accélération SuperPan.</span><span class="sxs-lookup"><span data-stu-id="80bbb-135">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span><br/>                                                           |
| [<span data-ttu-id="80bbb-136">**VideoPlaybackMode**</span><span class="sxs-lookup"><span data-stu-id="80bbb-136">**VideoPlaybackMode**</span></span>](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | <span data-ttu-id="80bbb-137">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="80bbb-137">Read/write</span></span><br/> | <span data-ttu-id="80bbb-138">Spécifie ou récupère une valeur qui indique le mode de lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="80bbb-138">Specifies or retrieves a value that indicates the video playback mode.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="80bbb-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80bbb-139">Requirements</span></span>



| <span data-ttu-id="80bbb-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80bbb-140">Requirement</span></span> | <span data-ttu-id="80bbb-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="80bbb-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80bbb-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80bbb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="80bbb-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="80bbb-143">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="80bbb-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80bbb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="80bbb-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="80bbb-145">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="80bbb-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="80bbb-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="80bbb-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80bbb-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="80bbb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="80bbb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80bbb-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80bbb-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="80bbb-150">IID</span><span class="sxs-lookup"><span data-stu-id="80bbb-150">IID</span></span><br/>                      | <span data-ttu-id="80bbb-151">IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="80bbb-151">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="80bbb-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80bbb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80bbb-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="80bbb-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="80bbb-154">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="80bbb-154">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="80bbb-155">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="80bbb-155">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="80bbb-156">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="80bbb-156">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="80bbb-157">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="80bbb-157">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="80bbb-158">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="80bbb-158">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="80bbb-159">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="80bbb-159">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

