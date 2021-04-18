---
title: Authentification de l’application
description: Authentification de l’application
ms.assetid: 011815fa-d55c-4abc-9ec8-55d754827342
keywords:
- Gestionnaire de périphériques Windows Media, authentification
- Gestionnaire de périphériques, authentification
- Guide de programmation, authentification
- applications de bureau, authentification
- création d’applications Windows Media Gestionnaire de périphériques, authentification
- Authentification
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7779cdbb874278e6b62517cc2c1983dd2ce8fa1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106536274"
---
# <a name="authenticating-the-application"></a>Authentification de l’application

La première étape que votre application doit effectuer est l’authentification. L’authentification vérifie l’identité de l’application auprès de Windows Media Gestionnaire de périphériques. Une fois que vous avez authentifié votre application, vous pouvez appeler **QueryInterface** pour obtenir l’interface [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) racine, qui peut être interrogée pour d’autres interfaces requises, qui peuvent eux-mêmes être interrogées pour toutes les autres interfaces. L’authentification n’a besoin d’être effectuée qu’une seule fois, au démarrage.

Pour authentifier votre application, procédez comme suit :

1.  Cocréez l’objet **MediaDevMgr** (ID de classe MediaDevMgr) et demandez une interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .
2.  Créez un objet [CSecureChannelClient](csecurechannelclient-class.md) pour gérer l’authentification.
3.  Transmettez votre clé d’application et transférez le certificat à l’objet de canal sécurisé. Vous pouvez utiliser la clé factice/certificat indiquée dans l’exemple de code suivant pour bénéficier des fonctionnalités de base des fonctions du kit de développement logiciel (SDK). Toutefois, pour obtenir toutes les fonctionnalités (importantes pour le transfert de fichiers vers et depuis l’appareil), vous devez demander une clé et un certificat auprès de Microsoft, comme décrit dans [outils pour le développement](tools-for-development.md).
4.  Transmettez l’interface **IComponentAuthenticate** que vous avez créée à l’étape 1 à l’objet de canal sécurisé.
5.  Appelez [**CSecureChannelClient :: Authenticate**](/previous-versions/ms983906(v=msdn.10)) pour authentifier votre application.
6.  Interrogez **IComponentAuthenticate** pour l’interface **IWMDeviceManager** .

Ces étapes sont présentées dans le code C++ suivant.


```C++
HRESULT CWMDMController::Authenticate()
{
    // Use a dummy key/certificate pair to allow basic functionality.
    // An authentic keypair is required for full SDK functionality.
    BYTE abPVK[] = {0x00};
    BYTE abCert[] = {0x00};
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

    if (FAILED(hr)) return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL) return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (FAILED(hr)) return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and authenticate the application with the V1 protocol.
    // (This is the only protocol currently supported.)
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (FAILED(hr)) return hr;

    // Authentication succeeded, so we can use WMDM.
    // Query for the root WMDM interface.
    hr = pAuth->QueryInterface( __uuidof(IWMDeviceManager), (void**)&m_IWMDMDeviceMgr);

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création d’une application Windows Media Gestionnaire de périphériques**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 