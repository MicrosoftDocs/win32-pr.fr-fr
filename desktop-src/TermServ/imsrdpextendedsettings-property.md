---
title: IMsRdpExtendedSettings Property, propriété
description: Contient une propriété nommée.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Propriété Property Services Bureau à distance
- Propriété Property Services Bureau à distance, IMsRdpExtendedSettings, interface
- Services Bureau à distance de l’interface IMsRdpExtendedSettings, propriété Property
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745349"
---
# <a name="imsrdpextendedsettingsproperty-property"></a><span data-ttu-id="6a5ea-106">IMsRdpExtendedSettings ::P propriété opriétés</span><span class="sxs-lookup"><span data-stu-id="6a5ea-106">IMsRdpExtendedSettings::Property property</span></span>

<span data-ttu-id="6a5ea-107">Contient une propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-107">Contains a named property.</span></span>

<span data-ttu-id="6a5ea-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5ea-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a5ea-109">Syntax</span></span>


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a><span data-ttu-id="6a5ea-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="6a5ea-110">Property value</span></span>

<span data-ttu-id="6a5ea-111">Valeur de la propriété nommée.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-111">The named property value.</span></span>

| <span data-ttu-id="6a5ea-112">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="6a5ea-112">Property name</span></span> | <span data-ttu-id="6a5ea-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="6a5ea-113">Data type</span></span> | <span data-ttu-id="6a5ea-114">Accès</span><span class="sxs-lookup"><span data-stu-id="6a5ea-114">Access</span></span> | <span data-ttu-id="6a5ea-115">Peut être modifié après le démarrage de la connexion</span><span class="sxs-lookup"><span data-stu-id="6a5ea-115">Can be changed after connection started</span></span> | <span data-ttu-id="6a5ea-116">Description</span><span class="sxs-lookup"><span data-stu-id="6a5ea-116">Description</span></span> |
|----------|-----------|--------|-----------------------------------------|-------------|
| <span data-ttu-id="6a5ea-117">ConnectToChildSession</span><span class="sxs-lookup"><span data-stu-id="6a5ea-117">ConnectToChildSession</span></span> | <span data-ttu-id="6a5ea-118">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6a5ea-118">**VT\_BOOL**</span></span> | <span data-ttu-id="6a5ea-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a5ea-119">Read/Write</span></span> | <span data-ttu-id="6a5ea-120">Oui</span><span class="sxs-lookup"><span data-stu-id="6a5ea-120">Yes</span></span> | <span data-ttu-id="6a5ea-121">Si vous affectez la **valeur true** à cette propriété, le contrôle client se connecte à la session enfant sur l’ordinateur local au lieu d’un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-121">Setting this property to **True** causes the client control to connect to the child session on the local machine instead of a remote server.</span></span> <span data-ttu-id="6a5ea-122">Si cette propriété est définie sur **true**, vous ne pouvez pas vous connecter à un serveur distant, car toutes les connexions sont redirigées vers localhost.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-122">If this property is set to **true**, you cannot connect to a remote server because all connections are redirected to localhost.</span></span> <span data-ttu-id="6a5ea-123">Pour plus d’informations sur les sessions enfants, consultez [sessions enfants](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="6a5ea-123">For more information about child sessions, see [Child Sessions](child-sessions.md).</span></span> |
| <span data-ttu-id="6a5ea-124">DisableCredentialsDelegation</span><span class="sxs-lookup"><span data-stu-id="6a5ea-124">DisableCredentialsDelegation</span></span> | <span data-ttu-id="6a5ea-125">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6a5ea-125">**VT\_BOOL**</span></span> | <span data-ttu-id="6a5ea-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a5ea-126">Read/Write</span></span> | <span data-ttu-id="6a5ea-127">Non</span><span class="sxs-lookup"><span data-stu-id="6a5ea-127">No</span></span> | <span data-ttu-id="6a5ea-128">Si la **valeur est true**, les informations d’identification ne sont pas envoyées au serveur distant.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-128">If **True**, credentials are not sent to the remote server.</span></span> |
| <span data-ttu-id="6a5ea-129">EnableFrameBufferRedirection</span><span class="sxs-lookup"><span data-stu-id="6a5ea-129">EnableFrameBufferRedirection</span></span> | <span data-ttu-id="6a5ea-130">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6a5ea-130">**VT\_BOOL**</span></span> | <span data-ttu-id="6a5ea-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a5ea-131">Read/Write</span></span> | <span data-ttu-id="6a5ea-132">Non</span><span class="sxs-lookup"><span data-stu-id="6a5ea-132">No</span></span> | <span data-ttu-id="6a5ea-133">Si la **valeur est true**, la redirection de la mémoire tampon de frame est tentée.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-133">If **True**, frame buffer redirection is attempted.</span></span> <span data-ttu-id="6a5ea-134">Pour une connexion de bouclage (le même ordinateur étant à la fois client et serveur), la redirection de la mémoire tampon de trame permet de partager la mémoire de la mémoire tampon de trame entre les sessions.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-134">For a loopback connection (the same computer is both client and server) frame buffer redirection allows the memory for the frame buffer to be shared between the sessions.</span></span> |
| <span data-ttu-id="6a5ea-135">EnableHardwareMode</span><span class="sxs-lookup"><span data-stu-id="6a5ea-135">EnableHardwareMode</span></span> | <span data-ttu-id="6a5ea-136">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6a5ea-136">**VT\_BOOL**</span></span>  | <span data-ttu-id="6a5ea-137">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="6a5ea-137">Write Only</span></span> | <span data-ttu-id="6a5ea-138">Non</span><span class="sxs-lookup"><span data-stu-id="6a5ea-138">No</span></span> | <span data-ttu-id="6a5ea-139">Si la **valeur est true**, l’assistance matérielle au décodage graphique est tentée.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-139">If **True**, hardware assist with graphics decoding is attempted.</span></span> |
| <span data-ttu-id="6a5ea-140">IgnoreCursors</span><span class="sxs-lookup"><span data-stu-id="6a5ea-140">IgnoreCursors</span></span> | <span data-ttu-id="6a5ea-141">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6a5ea-141">**VT\_BOOL**</span></span> | <span data-ttu-id="6a5ea-142">Écriture seule</span><span class="sxs-lookup"><span data-stu-id="6a5ea-142">Write Only</span></span> | <span data-ttu-id="6a5ea-143">Non</span><span class="sxs-lookup"><span data-stu-id="6a5ea-143">No</span></span> | <span data-ttu-id="6a5ea-144">Si la **valeur est true**, les curseurs envoyés par le serveur distant sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-144">If **True**, cursors sent by the remote server are ignored.</span></span> |
| <span data-ttu-id="6a5ea-145">ManualClipboardSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="6a5ea-145">ManualClipboardSyncEnabled</span></span> | <span data-ttu-id="6a5ea-146">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="6a5ea-146">**VT\_BOOL**</span></span> | <span data-ttu-id="6a5ea-147">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a5ea-147">Read/Write</span></span> | <span data-ttu-id="6a5ea-148">Oui</span><span class="sxs-lookup"><span data-stu-id="6a5ea-148">Yes</span></span> | <span data-ttu-id="6a5ea-149">Si cette propriété a la **valeur true** , cela signifie que les presse-papiers locaux et distants ne seront pas synchronisés automatiquement. Au lieu de cela, l’interface [**IMsRdpClipboard**](imsrdpclipboard.md) doit être utilisée pour synchroniser les formats du presse-papiers du presse-papiers local vers le presse-papiers distant et le presse-papiers distant vers le presse-papiers local.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-149">Setting this property to **True** means that the local and remote clipboards will not be automatically kept in sync. Instead the [**IMsRdpClipboard**](imsrdpclipboard.md) interface must be used to sync clipboard formats from the local clipboard to the remote clipboard and the remote clipboard to the local clipboard.</span></span> |
| <span data-ttu-id="6a5ea-150">ZoomLevel</span><span class="sxs-lookup"><span data-stu-id="6a5ea-150">ZoomLevel</span></span> | <span data-ttu-id="6a5ea-151">\**_VT \_ UI4_*</span><span class="sxs-lookup"><span data-stu-id="6a5ea-151">\**_VT\_UI4_*</span></span> | <span data-ttu-id="6a5ea-152">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="6a5ea-152">Read/Write</span></span> | <span data-ttu-id="6a5ea-153">Oui</span><span class="sxs-lookup"><span data-stu-id="6a5ea-153">Yes</span></span> | <span data-ttu-id="6a5ea-154">Implémente la fonctionnalité de zoom à l’aide du contrôle ActiveX RDP.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-154">Implements the Zoom feature by using the RDP ActiveX control.</span></span> <span data-ttu-id="6a5ea-155">La fonctionnalité de zoom est disponible dans le menu **système** de RDP.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-155">The Zoom feature is available from the **System** menu of RDP.</span></span> <span data-ttu-id="6a5ea-156">La propriété **zoomLevel** n’a aucun effet en mode RemoteApp et en mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-156">The **ZoomLevel** property has no effect in RemoteApp mode and full-screen mode.</span></span> <span data-ttu-id="6a5ea-157">[**IMsRdpClientAdvancedSettings :: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) et **zoomLevel** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="6a5ea-157">[**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) and **ZoomLevel** are mutually exclusive.</span></span> |

## <a name="requirements"></a><span data-ttu-id="6a5ea-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a5ea-158">Requirements</span></span>



| <span data-ttu-id="6a5ea-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a5ea-159">Requirement</span></span> | <span data-ttu-id="6a5ea-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a5ea-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5ea-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a5ea-161">Minimum supported client</span></span><br/> | <span data-ttu-id="6a5ea-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a5ea-162">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="6a5ea-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a5ea-163">Minimum supported server</span></span><br/> | <span data-ttu-id="6a5ea-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a5ea-164">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="6a5ea-165">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6a5ea-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a5ea-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a5ea-166"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="6a5ea-167">DLL</span><span class="sxs-lookup"><span data-stu-id="6a5ea-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a5ea-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a5ea-168"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="6a5ea-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="6a5ea-169">CLSID</span></span><br/>                    | <span data-ttu-id="6a5ea-170">Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54d38bf7-b1ef-4479-9674-1bd6ea465258</span><span class="sxs-lookup"><span data-stu-id="6a5ea-170">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54d38bf7-b1ef-4479-9674-1bd6ea465258</span></span><br/> <span data-ttu-id="6a5ea-171">Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="6a5ea-171">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="6a5ea-172">Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="6a5ea-172">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="6a5ea-173">IID</span><span class="sxs-lookup"><span data-stu-id="6a5ea-173">IID</span></span><br/>                      | <span data-ttu-id="6a5ea-174">IID \_ IMsRdpExtendedSettings est défini en tant que 302D8188-0052-4807-806A-362B628F9AC5</span><span class="sxs-lookup"><span data-stu-id="6a5ea-174">IID\_IMsRdpExtendedSettings is defined as 302D8188-0052-4807-806A-362B628F9AC5</span></span><br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="6a5ea-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a5ea-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5ea-176">**IMsRdpExtendedSettings**</span><span class="sxs-lookup"><span data-stu-id="6a5ea-176">**IMsRdpExtendedSettings**</span></span>](imsrdpextendedsettings.md)
</dt> </dl>

 

 





