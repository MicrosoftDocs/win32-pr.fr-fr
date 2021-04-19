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
# <a name="handling-protected-content-in-the-application"></a>Gestion du contenu protégé dans l’application

\[La fonctionnalité Windows Media DRM est déconseillée et ne doit pas être utilisée. Utilisez plutôt [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Une application doit avoir un certificat de transfert pour pouvoir gérer le contenu DRM protégé. Pour savoir où obtenir ce certificat, consultez [outils de développement](tools-for-development.md). Pour gérer du contenu non protégé, vous pouvez utiliser un certificat factice comme décrit dans [authentification de l’application](authenticating-the-application.md).

Avant d’utiliser un appareil, votre application doit déterminer si l’appareil prend en charge Windows Media DRM 10 pour les appareils mobiles et, le cas échéant, que les composants DRM sont à jour. (Actuel signifie que l’horloge sécurisée est correcte et que l’appareil a été correctement individualisé.) Si l’appareil ne prend pas en charge cette version de la gestion des droits numériques, ou s’il ne peut pas être mis à jour, vous pouvez toujours envoyer des fichiers à l’appareil, mais ils peuvent ne pas être lisibles, en fonction de la version de la licence.

> [!Note]  
> L’individualisation des appareils n’est pas prise en charge actuellement.

 

Si votre application est liée aux méthodes du kit de développement logiciel (SDK) Windows Media format, elle doit être liée à la bibliothèque de format Windows Media WMStubDRM. lib. Pour plus d’informations sur l’appel des méthodes Windows Media format sur du contenu DRM protégé, consultez la rubrique « activation de la prise en charge de DRM » dans la documentation du kit de développement logiciel (SDK) Windows Media format. Notez qu’il existe un problème de liaison à Mssachlp. lib et WMStubDRM. lib. Ce sujet est traité dans [l’article 890079 de la base de connaissances sur MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

L’exemple de code C++ suivant détermine si un appareil est un appareil Windows Media DRM 10 et, le cas échéant, que son horloge est à jour.

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



Si l’appareil ne prend pas en charge Windows Media DRM 10 pour les périphériques portables et doit être mis à jour (autrement dit, si la valeur de l' *État* dans l’exemple précédent n’est pas simplement WMDM d' \_ appareil \_ ISWMDRM), l’application doit appeler [**IWMDRMDeviceApp :: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) et transmettre la valeur de *Status* pour effectuer les mises à jour requises. L’ordinateur de bureau doit être connecté à Internet.

L’exemple de fonction C++ suivant tente de mettre à jour un périphérique DRM.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’une application Windows Media Gestionnaire de périphériques**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Gestion du contenu protégé**](handling-protected-content.md)
</dt> </dl>

 

 