---
title: Interface IMsRdpClientAdvancedSettings5
description: Gère les paramètres client avancés. Dérive de l’interface IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512574"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a><span data-ttu-id="1395c-106">Interface IMsRdpClientAdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="1395c-106">IMsRdpClientAdvancedSettings5 interface</span></span>

<span data-ttu-id="1395c-107">Gère les paramètres client avancés.</span><span class="sxs-lookup"><span data-stu-id="1395c-107">Manages advanced client settings.</span></span> <span data-ttu-id="1395c-108">Dérive de l’interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="1395c-108">Derives from the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="1395c-109">Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="1395c-109">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="1395c-110">Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings5** à **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="1395c-110">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings5** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="1395c-111">Membres</span><span class="sxs-lookup"><span data-stu-id="1395c-111">Members</span></span>

<span data-ttu-id="1395c-112">L’interface **IMsRdpClientAdvancedSettings5** hérite de [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span><span class="sxs-lookup"><span data-stu-id="1395c-112">The **IMsRdpClientAdvancedSettings5** interface inherits from [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span></span> <span data-ttu-id="1395c-113">**IMsRdpClientAdvancedSettings5** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="1395c-113">**IMsRdpClientAdvancedSettings5** also has these types of members:</span></span>

-   [<span data-ttu-id="1395c-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1395c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1395c-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1395c-115">Properties</span></span>

<span data-ttu-id="1395c-116">L’interface **IMsRdpClientAdvancedSettings5** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1395c-116">The **IMsRdpClientAdvancedSettings5** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1395c-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="1395c-117">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1395c-118">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="1395c-118">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1395c-119">Description</span><span class="sxs-lookup"><span data-stu-id="1395c-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1395c-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="1395c-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1395c-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-122">Mode de redirection audio.</span><span class="sxs-lookup"><span data-stu-id="1395c-122">The audio redirection mode.</span></span> <span data-ttu-id="1395c-123">La propriété <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> a les valeurs possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="1395c-123">The <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> property has the following possible values.</span></span><br/><span data-ttu-id="1395c-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (la redirection audio est activée et l’option de redirection est &quot; Envoyer à cet ordinateur &quot; .</span><span class="sxs-lookup"><span data-stu-id="1395c-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (Audio redirection is enabled and the option for redirection is &quot;Bring to this computer&quot;.</span></span> <span data-ttu-id="1395c-125">Il s’agit du mode par défaut.)</span><span class="sxs-lookup"><span data-stu-id="1395c-125">This is the default mode.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="1395c-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (la redirection audio est activée et l’option &quot; laisse sur l’ordinateur distant &quot; .</span><span class="sxs-lookup"><span data-stu-id="1395c-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (Audio redirection is enabled and the option is &quot;Leave at remote computer&quot;.</span></span> <span data-ttu-id="1395c-127">L' &quot; option de départ sur l’ordinateur distant &quot; est prise en charge uniquement lors de la connexion à distance à un ordinateur hôte qui exécute Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1395c-127">The &quot;Leave at remote computer&quot; option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="1395c-128">Si la connexion est vers un ordinateur hôte qui exécute Windows Server 2008, l’option &quot; conserver sur l’ordinateur distant &quot; est remplacée par &quot; ne pas lire &quot; .)</span><span class="sxs-lookup"><span data-stu-id="1395c-128">If the connection is to a host computer that is running Windows Server 2008, the option &quot;Leave at remote computer&quot; is changed to &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="1395c-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (la redirection audio est activée et le mode n’est &quot; pas lu &quot; .)</span><span class="sxs-lookup"><span data-stu-id="1395c-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Audio redirection is enabled and the mode is &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1395c-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="1395c-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1395c-131">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-132">Spécifie la taille du fichier de cache virtuel pour les bitmaps de 32 bits par pixel (BPP).</span><span class="sxs-lookup"><span data-stu-id="1395c-132">Specifies the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span> <span data-ttu-id="1395c-133">La valeur maximale est de 48 mégaoctets (Mo).</span><span class="sxs-lookup"><span data-stu-id="1395c-133">The maximum value is 48 megabytes (MB).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1395c-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="1395c-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1395c-135">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-136">Spécifie si le bouton épingler doit être affiché dans la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="1395c-136">Specifies whether the pin button should be shown on the connection bar.</span></span> <span data-ttu-id="1395c-137">Par défaut, la valeur est <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="1395c-137">By default, the value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1395c-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="1395c-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-139">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1395c-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-140">Spécifie si le mode public doit être activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="1395c-140">Specifies whether public mode should be enabled or disabled.</span></span> <span data-ttu-id="1395c-141">Par défaut, le mode public a la valeur <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="1395c-141">By default, public mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1395c-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span><span class="sxs-lookup"><span data-stu-id="1395c-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-143">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1395c-143">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-144">Spécifie si la redirection du presse-papiers doit être activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="1395c-144">Specifies whether clipboard redirection should be enabled or disabled.</span></span> <span data-ttu-id="1395c-145">Par défaut, le mode de redirection du presse-papiers a la valeur <strong>true</strong> (activé).</span><span class="sxs-lookup"><span data-stu-id="1395c-145">By default, clipboard redirection mode is set to <strong>TRUE</strong> (enabled).</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="1395c-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="1395c-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-147">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1395c-147">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-148">Spécifie si les appareils redirigés doivent être activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="1395c-148">Specifies whether redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="1395c-149">Par défaut, le mode appareils Redirigé est défini sur <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="1395c-149">By default, redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1395c-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="1395c-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-151">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="1395c-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1395c-152">Spécifie si les appareils redirigés de point de service doivent être activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="1395c-152">Specifies whether Point of Service redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="1395c-153">Par défaut, le mode appareils redirigés point de service est défini sur <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="1395c-153">By default, Point of Service redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="1395c-154">Notes</span><span class="sxs-lookup"><span data-stu-id="1395c-154">Remarks</span></span>

<span data-ttu-id="1395c-155">Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :</span><span class="sxs-lookup"><span data-stu-id="1395c-155">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="1395c-156">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1395c-156">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="1395c-157">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1395c-157">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="1395c-158">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1395c-158">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a><span data-ttu-id="1395c-159">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1395c-159">Requirements</span></span>



| <span data-ttu-id="1395c-160">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1395c-160">Requirement</span></span> | <span data-ttu-id="1395c-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="1395c-161">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1395c-162">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1395c-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1395c-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1395c-163">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="1395c-164">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1395c-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1395c-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1395c-165">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="1395c-166">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1395c-166">Type library</span></span><br/>             | <dl> <span data-ttu-id="1395c-167"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1395c-167"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1395c-168">DLL</span><span class="sxs-lookup"><span data-stu-id="1395c-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1395c-169"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1395c-169"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="1395c-170">IID</span><span class="sxs-lookup"><span data-stu-id="1395c-170">IID</span></span><br/>                      | <span data-ttu-id="1395c-171">IID \_ IMsRdpClientAdvancedSettings5 est défini en tant que FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="1395c-171">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1395c-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1395c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1395c-173">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1395c-173">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1395c-174">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1395c-174">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="1395c-175">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1395c-175">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="1395c-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="1395c-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1395c-177">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="1395c-177">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1395c-178">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="1395c-178">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

