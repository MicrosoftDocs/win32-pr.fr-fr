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
# <a name="authenticating-the-application"></a><span data-ttu-id="a40d8-109">Authentification de l’application</span><span class="sxs-lookup"><span data-stu-id="a40d8-109">Authenticating the Application</span></span>

<span data-ttu-id="a40d8-110">La première étape que votre application doit effectuer est l’authentification.</span><span class="sxs-lookup"><span data-stu-id="a40d8-110">The first step your application must perform is authentication.</span></span> <span data-ttu-id="a40d8-111">L’authentification vérifie l’identité de l’application auprès de Windows Media Gestionnaire de périphériques.</span><span class="sxs-lookup"><span data-stu-id="a40d8-111">Authentication verifies the application's identity to Windows Media Device Manager.</span></span> <span data-ttu-id="a40d8-112">Une fois que vous avez authentifié votre application, vous pouvez appeler **QueryInterface** pour obtenir l’interface [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) racine, qui peut être interrogée pour d’autres interfaces requises, qui peuvent eux-mêmes être interrogées pour toutes les autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="a40d8-112">Once you authenticate your application, you can call **QueryInterface** to get the root [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) interface, which can be queried for other required interfaces, which can themselves be queried for all other interfaces.</span></span> <span data-ttu-id="a40d8-113">L’authentification n’a besoin d’être effectuée qu’une seule fois, au démarrage.</span><span class="sxs-lookup"><span data-stu-id="a40d8-113">Authentication need only take place once, on startup.</span></span>

<span data-ttu-id="a40d8-114">Pour authentifier votre application, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a40d8-114">To authenticate your application, perform these steps:</span></span>

1.  <span data-ttu-id="a40d8-115">Cocréez l’objet **MediaDevMgr** (ID de classe MediaDevMgr) et demandez une interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .</span><span class="sxs-lookup"><span data-stu-id="a40d8-115">CoCreate the **MediaDevMgr** object (class ID MediaDevMgr), and request an [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface.</span></span>
2.  <span data-ttu-id="a40d8-116">Créez un objet [CSecureChannelClient](csecurechannelclient-class.md) pour gérer l’authentification.</span><span class="sxs-lookup"><span data-stu-id="a40d8-116">Create a [CSecureChannelClient](csecurechannelclient-class.md) object to handle the authentication.</span></span>
3.  <span data-ttu-id="a40d8-117">Transmettez votre clé d’application et transférez le certificat à l’objet de canal sécurisé.</span><span class="sxs-lookup"><span data-stu-id="a40d8-117">Pass your application key and transfer certificate to the secure channel object.</span></span> <span data-ttu-id="a40d8-118">Vous pouvez utiliser la clé factice/certificat indiquée dans l’exemple de code suivant pour bénéficier des fonctionnalités de base des fonctions du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="a40d8-118">You can use the dummy key/certificate shown in the following example code to get basic functionality from SDK functions.</span></span> <span data-ttu-id="a40d8-119">Toutefois, pour obtenir toutes les fonctionnalités (importantes pour le transfert de fichiers vers et depuis l’appareil), vous devez demander une clé et un certificat auprès de Microsoft, comme décrit dans [outils pour le développement](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="a40d8-119">However, to get full functionality (important for passing files to and from the device), you must request a key and certificate from Microsoft as described in [Tools for Development](tools-for-development.md).</span></span>
4.  <span data-ttu-id="a40d8-120">Transmettez l’interface **IComponentAuthenticate** que vous avez créée à l’étape 1 à l’objet de canal sécurisé.</span><span class="sxs-lookup"><span data-stu-id="a40d8-120">Pass the **IComponentAuthenticate** interface you created in step 1 to the secure channel object.</span></span>
5.  <span data-ttu-id="a40d8-121">Appelez [**CSecureChannelClient :: Authenticate**](/previous-versions/ms983906(v=msdn.10)) pour authentifier votre application.</span><span class="sxs-lookup"><span data-stu-id="a40d8-121">Call [**CSecureChannelClient::Authenticate**](/previous-versions/ms983906(v=msdn.10)) to authenticate your application.</span></span>
6.  <span data-ttu-id="a40d8-122">Interrogez **IComponentAuthenticate** pour l’interface **IWMDeviceManager** .</span><span class="sxs-lookup"><span data-stu-id="a40d8-122">Query **IComponentAuthenticate** for the **IWMDeviceManager** interface.</span></span>

<span data-ttu-id="a40d8-123">Ces étapes sont présentées dans le code C++ suivant.</span><span class="sxs-lookup"><span data-stu-id="a40d8-123">These steps are shown in the following C++ code.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a40d8-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a40d8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a40d8-125">**Création d’une application Windows Media Gestionnaire de périphériques**</span><span class="sxs-lookup"><span data-stu-id="a40d8-125">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 