---
title: Gestion du contenu protégé dans l’application
description: Gestion du contenu protégé dans l’application
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Gestionnaire de périphériques Windows Media, certificats
- Gestionnaire de périphériques, certificats
- Guide de programmation, certificats
- applications de bureau, certificats
- création d’applications Windows Media Gestionnaire de périphériques, de certificats
- certificates
- Gestionnaire de périphériques Windows Media, contenu protégé par DRM
- Gestionnaire de périphériques, contenu protégé par DRM
- Guide de programmation, contenu protégé par DRM
- applications de bureau, contenu protégé par DRM
- création d’applications Windows Media Gestionnaire de périphériques, contenu protégé par DRM
- Contenu protégé par DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106518024"
---
# <a name="handling-protected-content-in-the-application"></a><span data-ttu-id="564b3-115">Gestion du contenu protégé dans l’application</span><span class="sxs-lookup"><span data-stu-id="564b3-115">Handling Protected Content in the Application</span></span>

<span data-ttu-id="564b3-116">\[La fonctionnalité Windows Media DRM est déconseillée et ne doit pas être utilisée.</span><span class="sxs-lookup"><span data-stu-id="564b3-116">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="564b3-117">Utilisez plutôt [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="564b3-117">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="564b3-118">Une application doit avoir un certificat de transfert pour pouvoir gérer le contenu DRM protégé.</span><span class="sxs-lookup"><span data-stu-id="564b3-118">An application must have a transfer certificate to be able to handle DRM-protected content.</span></span> <span data-ttu-id="564b3-119">Pour savoir où obtenir ce certificat, consultez [outils de développement](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="564b3-119">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="564b3-120">Pour gérer du contenu non protégé, vous pouvez utiliser un certificat factice comme décrit dans [authentification de l’application](authenticating-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="564b3-120">For handling unprotected content, you can use a dummy certificate as described in [Authenticating the Application](authenticating-the-application.md).</span></span>

<span data-ttu-id="564b3-121">Avant d’utiliser un appareil, votre application doit déterminer si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles et, le cas échéant, que les composants DRM sont à jour.</span><span class="sxs-lookup"><span data-stu-id="564b3-121">Before using a device, your application should determine whether the device supports Windows Media DRM 10 for Portable Devices, and if so, that the DRM components are current.</span></span> <span data-ttu-id="564b3-122">(Actuel signifie que l’horloge sécurisée est correcte et que l’appareil a été correctement individualisé.) Si l’appareil ne prend pas en charge cette version de la gestion des droits numériques, ou s’il ne peut pas être mis à jour, vous pouvez toujours envoyer des fichiers à l’appareil, mais ils peuvent ne pas être lisibles, en fonction de la version de la licence.</span><span class="sxs-lookup"><span data-stu-id="564b3-122">(Current means that the secure clock is correct and that the device has been properly individualized.) If the device does not support this version of DRM, or if it cannot be updated, you can still send files to the device, but they might not be playable, depending on the license version.</span></span>

> [!Note]  
> <span data-ttu-id="564b3-123">L’individualisation des appareils n’est pas prise en charge actuellement.</span><span class="sxs-lookup"><span data-stu-id="564b3-123">Individualization of devices is not currently supported.</span></span>

 

<span data-ttu-id="564b3-124">Si votre application est liée aux méthodes du kit de développement logiciel (SDK) Windows Media format, elle doit être liée à la bibliothèque de format Windows Media WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="564b3-124">If your application will link to Windows Media Format SDK methods, it will need to link to the Windows Media Format library WMStubDRM.lib.</span></span> <span data-ttu-id="564b3-125">Pour plus d’informations sur l’appel des méthodes Windows Media format sur du contenu DRM protégé, consultez la rubrique « activation de la prise en charge de DRM » dans la documentation du kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="564b3-125">For more information on calling Windows Media Format methods on DRM-protected content, see "Enabling DRM Support" in the Windows Media Format SDK documentation.</span></span> <span data-ttu-id="564b3-126">Notez qu’il existe un problème de liaison à Mssachlp. lib et WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="564b3-126">Note that there is a problem with linking to both Mssachlp.lib and WMStubDRM.lib.</span></span> <span data-ttu-id="564b3-127">Ce sujet est traité dans [l’article 890079 de la base de connaissances sur MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span><span class="sxs-lookup"><span data-stu-id="564b3-127">This is covered in [KB article 890079 on MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span></span>

<span data-ttu-id="564b3-128">L’exemple de code C++ suivant détermine si un appareil est un appareil Windows Media DRM 10 et, le cas échéant, que son horloge est à jour.</span><span class="sxs-lookup"><span data-stu-id="564b3-128">The following C++ code example determines whether a device is a Windows Media DRM 10 device and, if so, that its clock is up to date.</span></span>

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



<span data-ttu-id="564b3-129">Si l’appareil ne prend pas en charge Windows Media DRM 10 pour les périphériques portables et doit être mis à jour (autrement dit, si la valeur de l' *État* dans l’exemple précédent n’est pas simplement WMDM d' \_ appareil \_ ISWMDRM), l’application doit appeler [**IWMDRMDeviceApp :: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) et transmettre la valeur de *Status* pour effectuer les mises à jour requises.</span><span class="sxs-lookup"><span data-stu-id="564b3-129">If the device does support Windows Media DRM 10 for Portable Devices, and needs to be updated (that is, if the value of *status* in the previous example is not simply WMDM\_DEVICE\_ISWMDRM), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the value of *status* to perform the required updates.</span></span> <span data-ttu-id="564b3-130">L’ordinateur de bureau doit être connecté à Internet.</span><span class="sxs-lookup"><span data-stu-id="564b3-130">The desktop computer must be connected to the Internet.</span></span>

<span data-ttu-id="564b3-131">L’exemple de fonction C++ suivant tente de mettre à jour un périphérique DRM.</span><span class="sxs-lookup"><span data-stu-id="564b3-131">The following C++ example function attempts to update a DRM device.</span></span>


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="564b3-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="564b3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="564b3-133">**Création d’une application Windows Media Gestionnaire de périphériques**</span><span class="sxs-lookup"><span data-stu-id="564b3-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="564b3-134">**Gestion du contenu protégé**</span><span class="sxs-lookup"><span data-stu-id="564b3-134">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 