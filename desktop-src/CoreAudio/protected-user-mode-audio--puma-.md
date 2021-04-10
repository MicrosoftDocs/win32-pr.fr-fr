---
description: Windows Vista a introduit le moteur PUMA (Protected user mode audio), le moteur audio en mode utilisateur dans l’environnement protégé (PE) qui fournit un environnement plus sûr pour le traitement et le rendu audio.
ms.assetid: 27a50026-9e48-48b1-9249-7528a97333c9
title: PUMA (Protected user mode audio)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233dc82109feb66472e66e4235031696937d70d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861566"
---
# <a name="protected-user-mode-audio-puma"></a>PUMA (Protected user mode audio)

Windows Vista a introduit le moteur PUMA (Protected user mode audio), le moteur audio en mode utilisateur dans l’environnement protégé (PE) qui fournit un environnement plus sûr pour le traitement et le rendu audio. Cela permet d’activer uniquement les sorties audio acceptables et de s’assurer que les sorties sont désactivées de manière fiable. Pour plus d’informations sur le PUMA, consultez [sortie protection du contenu et Windows Vista](https://download.microsoft.com/download/5/D/6/5D6EAF2B-7DDF-476B-93DC-7CF0072878E6/output_protect.doc).

PUMA a été mis à jour pour Windows 7 afin de fournir les fonctionnalités suivantes :

-   Définition des bits SCMS (Serial Copy Management System) sur les points de terminaison S/PDIF et les bits de protection du contenu numérique à bande passante élevée (HDCP) sur les points de terminaison HDMI (High-Definition Multimedia Interface).
-   Activation des contrôles de protection SCMS et HDMI en dehors d’un environnement protégé (PE).

## <a name="drm-protection-in-audio-drivers"></a>Protection DRM dans les pilotes audio

La fonction de Rights Management numérique (DRM) permet d’empaqueter des données multimédias dans un conteneur sécurisé et de joindre des règles d’utilisation au contenu. Par exemple, le fournisseur de contenu peut utiliser la **protection contre la copie** ou la **sortie numérique** pour désactiver les copies numériques directes ou la transmission à partir du système de l’ordinateur.

La pile audio de certains produits Microsoft prend en charge DRM en implémentant les règles d’utilisation qui régissent la lecture du contenu audio. Pour lire le contenu protégé, le pilote audio sous-jacent doit être un *pilote approuvé*. autrement dit, le pilote doit être certifié par un logo pour DRMLevel 1300. Pour plus d’informations sur le développement de pilotes approuvés, vous pouvez utiliser des interfaces définies dans le kit de développement de pilotes Windows 2000 (« DDK ») ou version ultérieure. Les pilotes développés avec le DDK implémenteront les interfaces nécessaires à DRM. Pour plus d’informations, consultez [Rights Management numérique](/windows-hardware/drivers/audio/digital-rights-management).

Pour afficher le contenu protégé, le pilote approuvé doit vérifier si la **protection contre la copie** et la **désactivation de la sortie numérique** sont définies sur le flux de contenu via la pile audio, et répondre aux paramètres en conséquence.

### <a name="copy-protection-rule"></a>Copier la règle de protection

La **protection contre la copie** indique que les copies numériques directes ne sont pas autorisées sur le système. L’exposition B à l’accord de test WHQL a été mise à jour pour refléter les nouvelles attentes et exigences d’un pilote lorsque la **protection contre la copie** est définie sur le contenu. Pour Windows 7, le pilote de classe HD audio intégré est conforme aux exigences les plus récentes.

En plus de s’assurer que le contenu n’est pas autorisé à passer à un autre composant ou à être stocké sur un support de stockage non volatile qui n’est pas authentifié par le système DRM, le pilote audio effectue les tâches suivantes lorsque la **protection de copie** est définie :

-   Le pilote active HDCP sur les points de terminaison HDMI.
-   Pour les interfaces S/PDIF, le pilote vérifie que la combinaison des bits de code de L, CP et de catégorie indique un État SCMS « copie Never », comme défini dans IEC 60958.
-   Le bit L est défini sur 0 et le code de catégorie est défini sur « digital signal mixer ».

La structure **DRMRIGHTS** , utilisée par les pilotes audio approuvés, spécifie les droits de contenu DRM affectés à un code confidentiel audio KS ou à un objet de flux de pilote de classe de port. Le membre **CopyProtect** indique si la **protection de copie** est définie sur le contenu audio.

Pour Windows 7, l’utilisation de **CopyProtect** est plus stricte. Le pilote s’assure que les contrôles de protection sont définis sur les interfaces audio, HDCP est défini pour la sortie HDMI et SCMS est défini pour la sortie S/PDIF en définissant l’État sur « copier jamais ».

### <a name="digital-output-disable-rule"></a>Règle de désactivation de la sortie numérique

La **désactivation de la sortie numérique** indique que le contenu n’est pas autorisé à être transmis hors du système. Dans Windows 7, le pilote de classe HD audio intégré répond à ce paramètre en activant HDCP sur les points de terminaison HDMI. Cela est similaire à la réponse du pilote au paramètre de **protection de copie** .

## <a name="enabling-content-protection-mechanisms-outside-of-a-protected-environment"></a>Activation de mécanismes de protection de contenu en dehors d’un environnement protégé

PUMA réside dans un processus distinct de l’environnement protégé (PE). Dans Windows Vista, pour utiliser les contrôles de protection de contenu audio proposés par PUMA, une application multimédia doit être dans un fichier PE. Étant donné que seules les API Media Foundation peuvent interagir avec un PE, les contrôles de protection de contenu sont limités aux applications qui utilisent des API Media Foundation pour diffuser du contenu audio.

Dans Windows 7, toute application peut accéder aux contrôles de protection de contenu fournis par l’autorité d’approbation de sortie PUMA (OTA), qu’il s’agisse d’un fichier PE ou d’Media Foundation API pour la lecture audio.

## <a name="implementation-instructions"></a>Instructions d’implémentation

Les étapes suivantes sont requises pour qu’une application audio contrôle la protection du contenu SCMS ou HDCP sur un point de terminaison audio. Les API audio prises en charge sont DirectShow, DirectSound et WASAPI.

Cet exemple de code utilise les interfaces suivantes.

-   [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)
-   [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection)
-   [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput)
-   [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy)

L’application multimédia doit effectuer les tâches suivantes.

1.  Configurez l’environnement de développement.
    -   Référencez les interfaces requises, incluez les en-têtes affichés dans le code suivant.
        ```cpp
        #include <MMdeviceapi.h>        // Device endpoint definitions
        #include <Mfidl.h>              // OTA interface definitions
        ```

        

    -   Lien vers Mfuuid. lib pour utiliser les interfaces OTA.
    -   Désactivez le débogueur du noyau et le vérificateur de pilote pour éviter les erreurs de vérification de l’authentification.
2.  Énumérez tous les points de terminaison dans le système et sélectionnez le point de terminaison cible à partir de la collection de points de terminaison, comme indiqué dans le code suivant. Pour plus d’informations sur l’énumération des appareils, consultez [énumération des périphériques audio](/previous-versions//ms678716(v=vs.85)).
    ```cpp
    BOOL IsDigitalEndpoint(IMMDevice *pDevice)
    {
       PROPVARIANT         var;
       IPropertyStore      *pProperties = NULL;
       EndpointFormFactor  formfactor;
       BOOL                bResult = FALSE;
       HRESULT             hr = S_OK;
       PropVariantInit(&var);
       // Open endpoint properties
       hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
       IF_FAILED_JUMP(hr, Exit);

       // get form factor 
       hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
       IF_FAILED_JUMP(hr, Exit);
       formfactor = (EndpointFormFactor)var.uiVal;
       // DigitalAudioDisplayDevice is defined same as HDMI formfactor
       if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
       {
           bResult = TRUE;
       }

    Exit:
       PropVariantClear(&var);
       SAFE_RELEASE(pProperties);
       return bResult;
    }
    ```

    

    ```cpp
    /******************************************************************
    *                                                                 *
    *  GetDevice:  Selects an endpoint that meets the requirements.   *
    *                                                                 *
    *  ppDevice: Receives a pointer to an IMMDevice interface of      *
    *            the device's endpoint object                         *                                             *                                            *
    *                                                                 *
    ******************************************************************/
    HRESULT GetDevice(IMMDevice** ppDevice)
    {
       IMMDeviceEnumerator    *pEnumerator = NULL;
       IMMDevice              *pDevice = NULL;
       IMMDeviceCollection    *pEndpoints = NULL;
       UINT                    cEndpoints = 0;

       const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
       const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

       // Get enumerator for audio endpoint devices
       hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, 
           NULL,
           CLSCTX_ALL, 
           IID_IMMDeviceEnumerator,
           (void**)&pEnumerator));


       EXIT_ON_ERROR(hr)

       // Enumerate all active endpoints,
       hr = pEnumerator->EnumAudioEndpoints (
           eRender,
           DEVICE_STATE_ACTIVE,
           &pEndpoints);
       EXIT_ON_ERROR(hr)

       hr = pEndpoints->GetCount(&cEndpoints);
       EXIT_ON_ERROR(hr)

       for (UINT i = 0; i < cEndpoints; i++)
       {
           hr = pEndpoints->Item(i, &pDevice);
           IF_FAILED_JUMP(hr, Exit);
           {
               // Select the endpoint that meets the requirements.
               // For example, SPDIF analog output or HDMI
               if (IsDigitalEndpoint(pDevice))
               {
                   *(ppDevice) = pDevice;
                   (*ppDevice)->AddRef();
                   break;
               }
           }
           SAFE_RELEASE(pDevice);
       }
    Exit:
       if (FAILED(hr))
       {
           // Notify error.
           // Not Shown.
       }
       SAFE_RELEASE(pEndpoints);
       SAFE_RELEASE(pEnumerator);
    }
    ```

    

3.  Utilisez le pointeur [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) vers le point de terminaison retourné par le processus d’énumération pour activer l’API de diffusion audio en continu souhaitée et préparer la diffusion en continu. Différentes API audio requièrent une préparation légèrement différente.
    -   Pour les applications audio DShow :
        1.  Créez un objet COM DirectShow en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) et en spécifiant IID \_ IBaseFilter comme identificateur d’interface.
            ```cpp
            IUnknown *pDShowFilter = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IBaseFilter,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDShowFilter));
            ```

            

        2.  Générez un graphique de filtre DirectShow avec cet objet COM activé par l’appareil. Pour plus d’informations sur ce processus, consultez « génération du graphique de filtre » dans la documentation du kit de développement logiciel (SDK) DirectShow.
    -   Pour les applications audio DSound :
        1.  Créez un objet COM DSound en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) et en spécifiant IID \_ IDirectSound8 comme identificateur d’interface.
            ```cpp
            IDirectSound8  *pDSSound8;
            ...
            hr = pDevice->Activate (
                              IID_IDirectSound8,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pDSSound8));
            ```

            

        2.  Utilisez l’objet DSound créé ci-dessus pour programmer DSound pour la diffusion en continu. Pour plus d’informations sur ce processus, consultez [DirectSound](/previous-versions//bb219818(v=vs.85)) sur MSDN.
    -   Pour WASAPI :
        1.  Créez un objet com [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) en appelant [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) et en spécifiant IID \_ IAudioClient comme identificateur d’interface.
            ```cpp
            IAudioClient *pIAudioClient = NULL;
            ...
            hr = pDevice->Activate (
                              IID_IAudioClient,
                              CLSCTX_INPROC_SERVER, NULL,
                              reinterpret_cast<void **>(&pIAudioClient));
            ```

            

        2.  Ouvrez le flux audio.
            ```cpp
            hr = pIAudioClient->Initialize(...);
            ```

            
4.  Démarrer la diffusion audio en continu.
5.  Définissez la stratégie de protection sur le flux.
    1.  Pour les clients WASAPI, vous pouvez obtenir une référence à l’interface [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) de l’objet de l’autorité de confiance de sortie (OTA) pour le flux en appelant [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) et en spécifiant IID \_ IMFTrustedOutput comme identificateur d’interface.
        ```cpp
        IMFTrustedOutput*       pTrustedOutput = NULL;
        hr = pIAudioClient>GetService(
                       __uuidof(IMFTrustedOutput),
                       (void**)& pTrustedOutput);
        ```

        

    2.  Récupérez le nombre d’objets OTA disponibles en appelant [**IMFTrustedOutput :: GetOutputTrustAuthorityCount**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount).
        ```cpp
        hr = pTrustedOutput->GetOutputTrustAuthorityCount(&m_dwCountOTA);
        ```

        

    3.  Permet d’énumérer la collection OTA et d’obtenir une référence à l’objet OTA qui prend en charge l’action PEACTION \_ Play. Toutes les OTAs exposent l’interface [**IMFOutputTrustAuthority**](/windows/win32/api/mfidl/nn-mfidl-imfoutputtrustauthority) .
        ```cpp
        hr = pMFTrustedOutput->GetOutputTrustAuthorityByIndex(I, &pMFOutputTrustAuthority);
        hr = pMFOutputTrustAuthority->GetAction(&action) 
        ```

        

    4.  Utilisez l’interface [**IMFTrustedOutput**](/windows/win32/api/mfidl/nn-mfidl-imftrustedoutput) pour définir la stratégie de protection sur le flux.

        ```cpp
        hr = pTrustedOutput ->SetPolicy(&pPolicy, nPolicy, &pbTicket, &cbTicket);
        ```

        

        > [!Note]
        > Si vous utilisez EVR, [**SetPolicy**](/windows/win32/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) déclenche l’événement [MEPOLICYSET](../medfound/mepolicyset.md) et retourne MF \_ S \_ wait \_ pour \_ \_ que la stratégie soit définie pour indiquer que le OTA applique la stratégie de manière asynchrone. Toutefois, dans cet exemple de code, l’application est un client direct WASAPI qui a récupéré l’objet OTA à partir du client audio (étape 5 a). Contrairement à EVR, un client audio et d’autres objets WASAPI n’implémentent pas les générateurs d’événements multimédias. Sans les générateurs d’événements multimédia, **IMFTrustedOutput :: SetPolicy** ne retourne pas MF \_ S \_ wait \_ pour la \_ stratégie \_ définie.
        >
        > Les paramètres de la stratégie audio doivent être définis après le démarrage de la diffusion audio, sinon [**IMFTrustedOutput :: GetOutputTrustAuthorityByIndex**](/windows/win32/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritybyindex) échoue. En outre, pour prendre en charge cette fonctionnalité, le pilote audio sous-jacent doit être un *pilote approuvé*.

         

        Dans l’exemple de code, *pPolicy* est un pointeur vers l’interface [**IMFOutputPolicy**](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy) d’un objet de stratégie implémentée par le client. Pour plus d’informations, consultez la documentation [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) .

        Dans l’implémentation de la méthode [**IMFOutputPolicy :: GenerateRequiredSchemas**](/windows/win32/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) , une collection des systèmes de protection de sortie (schémas) doit être générée et doit être appliquée par le OTA. Chaque schéma est identifié par un GUID et contient des données de configuration pour le système de protection. Assurez-vous que les systèmes de protection de la collection sont limités à l’utilisation de pilotes audio approuvés. Cette restriction est identifiée par le GUID, **MFPROTECTION \_ TRUSTEDAUDIODRIVERS**, Disable ou CONSTRICTAUDIO. Si MFPROTECTION \_ TRUSTEDAUDIODRIVERS est utilisé, les données de configuration de ce schéma sont de valeur DWORD. Pour plus d’informations sur les schémas et les données de configuration associées, consultez documentation du kit de développement logiciel (SDK) de l’environnement protégé.

        Le client doit également fournir la définition de schéma en implémentant l’interface [**IMFOutputSchema**](/windows/win32/api/mfidl/nn-mfidl-imfoutputschema) . [**IMFOutputSchema :: GetSchemaType**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getschematype) récupère **MFPROTECTION \_ TRUSTEDAUDIODRIVERS** comme GUID du schéma. [**IMFOutputSchema :: GetConfigurationData**](/windows/win32/api/mfidl/nf-mfidl-imfoutputschema-getconfigurationdata) retourne un pointeur vers les données de configuration du schéma.

6.  Continuer la diffusion audio.
7.  Assurez-vous que la stratégie de protection est désactivée avant d’arrêter la diffusion en continu.

    Publiez les références de l’interface de stratégie associée ci-dessus.

    Les appels de version décochent les paramètres de stratégie précédemment définis.

    > [!Note]  
    > Chaque fois qu’un flux est redémarré, la stratégie de protection doit être redéfinie sur le flux. La procédure est décrite à l’étape 5-d.

    ```cpp
    pMFOutputTrustAuthority->Release()
    pMFTrustedOutput->Release()
    ```
  

Les exemples de code suivants illustrent un exemple d’implémentation de la stratégie et des objets de schéma.


```cpp
//OTADsoundSample.cpp
#include <stdio.h>
#include <tchar.h>
#include <initguid.h>
#include <windows.h>
#include <mmreg.h>
#include <dsound.h>

#include <mfidl.h>
#include <Mmdeviceapi.h>
#include <AVEndpointKeys.h>
#include "OTADSoundSample.h"

#define STATIC_KSDATAFORMAT_SUBTYPE_AC3\
    DEFINE_WAVEFORMATEX_GUID(WAVE_FORMAT_DOLBY_AC3_SPDIF)
DEFINE_GUIDSTRUCT("00000092-0000-0010-8000-00aa00389b71", KSDATAFORMAT_SUBTYPE_AC3);
#define KSDATAFORMAT_SUBTYPE_AC3 DEFINE_GUIDNAMED(KSDATAFORMAT_SUBTYPE_AC3)


HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy);
HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy);


const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);

BOOL IsDigitalEndpoint(IMMDevice *pDevice)
{
    PROPVARIANT         var;
    IPropertyStore      *pProperties = NULL;
    EndpointFormFactor  formfactor;
    BOOL                bResult = FALSE;
    HRESULT             hr = S_OK;
    PropVariantInit(&var);

    // Open endpoint properties
    hr = pDevice->OpenPropertyStore(STGM_READ, &pProperties);
    IF_FAILED_JUMP(hr, Exit);

    // get form factor 
    hr = pProperties->GetValue(PKEY_AudioEndpoint_FormFactor, &var);
    IF_FAILED_JUMP(hr, Exit);

    formfactor = (EndpointFormFactor)var.uiVal;
    if ((SPDIF == formfactor) || (DigitalAudioDisplayDevice == formfactor))
    {
        bResult = TRUE;
    }

Exit:
    PropVariantClear(&var);
    SAFE_RELEASE(pProperties);

    return bResult;
}


HRESULT GetDigitalAudioEndpoint(IMMDevice** ppDevice)
{
    IMMDeviceEnumerator    *pEnumerator = NULL;
    IMMDevice              *pDevice = NULL;
    IMMDeviceCollection    *pEndpoints = NULL;
    UINT                    cEndpoints = 0;
    HRESULT hr = S_OK;

    *ppDevice = NULL;
    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(CLSID_MMDeviceEnumerator, NULL,
                          CLSCTX_ALL, IID_IMMDeviceEnumerator,
                          (void**)&pEnumerator);
    IF_FAILED_JUMP(hr, Exit);

    // Enumerate all active render endpoints, 
    hr = pEnumerator->EnumAudioEndpoints(eRender, DEVICE_STATE_ACTIVE, &pEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    hr = pEndpoints->GetCount(&cEndpoints);
    IF_FAILED_JUMP(hr, Exit);

    for (UINT i = 0; i < cEndpoints; i++)
    {
        hr = pEndpoints->Item(i, &pDevice);
        IF_FAILED_JUMP(hr, Exit);
        // Select the endpoint that meets the requirements.
        // For example, SPDIF analog output or HDMI
        // Not Shown.
        if (IsDigitalEndpoint(pDevice))
        {
            *ppDevice = pDevice;
            (*ppDevice)->AddRef();
            break;
        }
        SAFE_RELEASE(pDevice);
    }
Exit:
    if (FAILED(hr))
    {
        // Notify error.
        // Not Shown.
    }
    SAFE_RELEASE(pEndpoints);
    SAFE_RELEASE(pEnumerator);
    return hr; 
}


//-------------------------------------------------------------------
int __cdecl wmain(int argc, char* argv[])
{
    IMMDevice *pEndpoint=NULL;
    HRESULT hr = S_OK;

    // DSound related variables
    IDirectSound8*          DSSound8 = NULL; 
    IDirectSoundBuffer*     DSBuffer = NULL; 
    DSBUFFERDESC            DSBufferDesc;
    WAVEFORMATEXTENSIBLE    wfext;
    WORD nChannels = 2;
    DWORD nSamplesPerSec = 48000;
    WORD wBitsPerSample = 16;

    // OTA related variables
    IMFTrustedOutput *pMFTrustedOutput=NULL;
    IMFOutputPolicy *pMFOutputPolicy=NULL;
    IMFOutputTrustAuthority *pMFOutputTrustAuthority=NULL;
    DWORD dwConfigData=0;

    // Initialize COM
    hr = CoInitialize(NULL);
    IF_FAILED_JUMP(hr, Exit);

    printf("OTA test app for DSound\n");

    hr = GetDigitalAudioEndpoint(&pEndpoint);
    IF_FAILED_JUMP(hr, Exit);

    if (pEndpoint)
    {
        printf("Found digital audio endpoint.\n");
    }
    //
    // Active DSound interface
    //
    hr = pEndpoint->Activate(IID_IDirectSound8, CLSCTX_INPROC_SERVER, NULL, reinterpret_cast<void **>(&DSSound8));
    IF_FAILED_JUMP(hr, Exit);

    nChannels = 2;
    nSamplesPerSec = 48000;
    wBitsPerSample = 16;

    ZeroMemory(&wfext, sizeof(wfext));
    wfext.Format.wFormatTag = WAVE_FORMAT_EXTENSIBLE;
    wfext.Format.nChannels = nChannels;
    wfext.Format.nSamplesPerSec = nSamplesPerSec;
    wfext.Format.wBitsPerSample = wBitsPerSample;
    wfext.Format.nBlockAlign = (nChannels * wBitsPerSample) / 8;
    wfext.Format.nAvgBytesPerSec = nSamplesPerSec * ((nChannels * wBitsPerSample) / 8);
    wfext.Format.cbSize = 22;
    wfext.Samples.wValidBitsPerSample = wBitsPerSample;
    wfext.dwChannelMask = 0x3;
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_PCM;
#if 1 
    wfext.SubFormat = KSDATAFORMAT_SUBTYPE_AC3;
#endif

    ZeroMemory(&DSBufferDesc, sizeof(DSBufferDesc));
    DSBufferDesc.dwSize = sizeof(DSBufferDesc);
    DSBufferDesc.dwFlags = DSBCAPS_GLOBALFOCUS | DSBCAPS_LOCSOFTWARE | DSBCAPS_GETCURRENTPOSITION2;
    DSBufferDesc.lpwfxFormat = (WAVEFORMATEX *)&wfext;
    DSBufferDesc.dwBufferBytes = wfext.Format.nAvgBytesPerSec / 100;

    HWND hwnd = GetForegroundWindow();
    hr = DSSound8->SetCooperativeLevel(hwnd, DSSCL_PRIORITY);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSSound8->CreateSoundBuffer(&DSBufferDesc, &DSBuffer, NULL);
    IF_FAILED_JUMP(hr, Exit);

    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    printf("Will set the following audio policy:\n");
    printf("Test Certificate Enable: %s\n", TRUE ? "True" : "False");
    printf("Copy OK: %s\n", FALSE ? "True" : "False");
    printf("Digital Output Disable: %s\n", FALSE ? "True" : "False");
    printf("DRM Level: %u\n", 1300);

    // Set policy when the stream is in RUN state
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    //
    // Perform all the necessary streaming operations here.
    //

    // stop audio streaming
    DSBuffer->Stop();

    // In order for the stream to restart successfully 
    // Need to release the following OutputTrust* interface to release audio endpoint
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // After above release operations, the following Play() will succeed without without device-in-use error message 0x8889000A
    DSBuffer->SetCurrentPosition(0);
    hr = DSBuffer->Play(0, 0, DSBPLAY_LOOPING);
    IF_FAILED_JUMP(hr, Exit);

    // Need to reset the new audio protection state because previous settings were gone with the ClearOTAPolicy call.
    dwConfigData = MAKE_MFPROTECTIONDATA_TRUSTEDAUDIODRIVERS2(TRUE, /*_bTestCertificateEnable*/ 
                                                              FALSE, /*_bDigitalOutputDisable*/ 
                                                              FALSE, /*_bCopyOK*/ 
                                                              1300 /*_dwDrmLevel*/);

    hr = SetOTAPolicy(pEndpoint,dwConfigData, &pMFTrustedOutput, &pMFOutputTrustAuthority,&pMFOutputPolicy); 
    IF_FAILED_JUMP(hr, Exit);

    // Clean up setting before leaving your streaming app.
    hr = ClearOTAPolicy(pMFTrustedOutput,pMFOutputTrustAuthority,pMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    DSBuffer->SetCurrentPosition(0);

Exit:
    SAFE_RELEASE(DSBuffer);
    SAFE_RELEASE(DSSound8);

    SAFE_RELEASE(pEndpoint);

    CoUninitialize();

    return 0;
}
```




```cpp
//OTADSoundSample.h
// Macro defines
#define IF_FAILED_JUMP(_hresult, label)                         \
    if(FAILED(_hresult))                                        \
    {                                                           \
        goto label;                                             \
    }

#define SAFE_RELEASE(p) \
    if (NULL != p) { \
        (p)->Release(); \
        (p) = NULL; \
    }

#define IF_TRUE_ACTION_JUMP(condition, action, label)           \
    if(condition)                                               \
    {                                                           \
        action;                                                 \
        goto label;                                             \
    }
```




```cpp
// outputpolicy.h

class CTrustedAudioDriversOutputPolicy : public CMFAttributesImpl<IMFOutputPolicy> 
{
friend
    HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy);
private:
    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginator;
    IMFOutputSchema *m_pOutputSchema;
    
    CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr);
    ~CTrustedAudioDriversOutputPolicy();

public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(/* [in] */ REFIID riid,/* [out] */ LPVOID *ppvObject);
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();
    
    // IMFOutputPolicy methods
    HRESULT STDMETHODCALLTYPE
        GenerateRequiredSchemas( 
            /* [in] */ DWORD dwAttributes,
            /* [in] */ GUID guidOutputSubType,
            /* [in] */ GUID *rgGuidProtectionSchemasSupported,
            /* [in] */ DWORD cProtectionSchemasSupported,
            /* [annotation][out] */ 
            __out  IMFCollection **ppRequiredProtectionSchemas);

    HRESULT STDMETHODCALLTYPE GetOriginatorID(/* [annotation][out] */ __out  GUID *pguidOriginatorID);

    HRESULT STDMETHODCALLTYPE GetMinimumGRLVersion(/* [annotation][out] */ __out  DWORD *pdwMinimumGRLVersion);
}; // CTrustedAudioDriversOutputPolicy

class CTrustedAudioDriversOutputSchema : public CMFAttributesImpl<IMFOutputSchema> 
{

friend
    HRESULT CreateTrustedAudioDriversOutputSchema(
        DWORD dwConfigData,
        GUID guidOriginatorID,
        IMFOutputSchema **ppMFOutputSchema
    );

private:
    CTrustedAudioDriversOutputSchema(DWORD dwConfigData, GUID guidOriginatorID);
    ~CTrustedAudioDriversOutputSchema();

    ULONG m_cRefCount;
    DWORD m_dwConfigData;
    GUID m_guidOriginatorID;
    
public:
    // IUnknown methods
    HRESULT STDMETHODCALLTYPE QueryInterface(
       /* [in] */ REFIID riid,
       /* [out] */ LPVOID *ppvObject
    );
    ULONG STDMETHODCALLTYPE AddRef();
    ULONG STDMETHODCALLTYPE Release();

    // IMFOutputSchema methods
    HRESULT STDMETHODCALLTYPE GetConfigurationData(__out DWORD *pdwVal);
    HRESULT STDMETHODCALLTYPE GetOriginatorID(__out GUID *pguidOriginatorID);
    HRESULT STDMETHODCALLTYPE GetSchemaType(__out GUID *pguidSchemaType);

}; // CTrustedAudioDriversOutputSchema
```




```cpp
// outputpolicy.cpp

#include <windows.h>
#include <tchar.h>
#include <mfidl.h>
#include <atlstr.h>
#include <attributesbase.h>
#include "OTADSoundSample.h"

#include <Mmdeviceapi.h>
#include "OutputPolicy.h"

#define RETURN_INTERFACE(T, iid, ppOut) \
    if (IsEqualIID(__uuidof(T), (iid))) { \
        this->AddRef(); \
        *(ppOut) = static_cast<T *>(this); \
        return S_OK; \
    } else {} (void)0

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputPolicy
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputPolicy::CTrustedAudioDriversOutputPolicy(DWORD dwConfigData, HRESULT &hr)
: m_cRefCount(1), m_dwConfigData(dwConfigData), m_pOutputSchema(NULL)
{
    hr = CoCreateGuid(&m_guidOriginator);
    IF_FAILED_JUMP(hr, Exit);

    hr = CreateTrustedAudioDriversOutputSchema(dwConfigData, m_guidOriginator, &m_pOutputSchema);
    IF_FAILED_JUMP(hr, Exit);

Exit:
    if (FAILED(hr))
    {
        printf("CreateTrustedAudioDriversOutputSchema failed: hr = 0x%08x", hr);
    }
    return;
}

// destructor
CTrustedAudioDriversOutputPolicy::~CTrustedAudioDriversOutputPolicy()
{
    if (NULL != m_pOutputSchema) 
    {
        m_pOutputSchema->Release();
    }
}


// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE
    CTrustedAudioDriversOutputPolicy::QueryInterface(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject)
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);

    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputPolicy, riid, ppvObject);    

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}

// IMFOutputPolicy::GenerateRequiredSchemas
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GenerateRequiredSchemas
( 
        /* [in] */ DWORD dwAttributes,
        /* [in] */ GUID guidOutputSubType,
        /* [in] */ GUID *rgGuidProtectionSchemasSupported,
        /* [in] */ DWORD cProtectionSchemasSupported,
        /* [annotation][out] */ 
        __out  IMFCollection **ppRequiredProtectionSchemas
)
{
    HRESULT hr = S_OK;
    bool bTrustedAudioDriversSupported = false;
    // if we've made it this far then the Output Trust Authority supports Trusted Audio Drivers
    // create a collection and put our output policy in it
    // then give that collection to the caller
    CComPtr<IMFCollection> pMFCollection;

    // sanity checks
    IF_TRUE_ACTION_JUMP((NULL == ppRequiredProtectionSchemas), hr = E_POINTER, Exit); 
    *ppRequiredProtectionSchemas = NULL;

    IF_TRUE_ACTION_JUMP((NULL == rgGuidProtectionSchemasSupported) && (0 != cProtectionSchemasSupported), 
                    hr = E_POINTER, Exit); 

    // log all the supported protection schemas
    for (DWORD i = 0; i < cProtectionSchemasSupported; i++) 
    {
        if (IsEqualIID(MFPROTECTION_TRUSTEDAUDIODRIVERS, rgGuidProtectionSchemasSupported[i])) 
        {
            bTrustedAudioDriversSupported = true;
        }
    }

    if (!bTrustedAudioDriversSupported) 
    {
        return HRESULT_FROM_WIN32(ERROR_RANGE_NOT_FOUND);
    }


    // create the collection
    hr = MFCreateCollection(&pMFCollection);
    if (FAILED(hr)) 
    {
        return hr;
    }

    // add our output policy to the collection
    hr = pMFCollection->AddElement(m_pOutputSchema);
    if (FAILED(hr)) 
    {
        return hr;
    }
Exit:
    // give the collection to the caller
    return pMFCollection.CopyTo(ppRequiredProtectionSchemas); // increments refcount
}// GenerateRequiredSchemas

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetOriginatorID(__out  GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) 
    {
        return E_POINTER;
    }
    *pguidOriginatorID = m_guidOriginator;
    return S_OK;
}

HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputPolicy::GetMinimumGRLVersion(__out  DWORD *pdwMinimumGRLVersion) 
{
    if (NULL == pdwMinimumGRLVersion) 
    {
        return E_POINTER;
    }
    *pdwMinimumGRLVersion = 0;
    return S_OK;
}

//--------------------------------------------------------------------------
// Implementation for CTrustedAudioDriversOutputSchema
//--------------------------------------------------------------------------
// constructor
CTrustedAudioDriversOutputSchema::CTrustedAudioDriversOutputSchema
(    
    DWORD dwConfigData, 
    GUID guidOriginatorID
)
: m_cRefCount(1)
, m_dwConfigData(dwConfigData)
, m_guidOriginatorID(guidOriginatorID)
{}

// destructor
CTrustedAudioDriversOutputSchema::~CTrustedAudioDriversOutputSchema() {}

// IUnknown::QueryInterface
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::QueryInterface
(
        /* [in] */ REFIID riid,
        /* [out] */ LPVOID *ppvObject
) 
{
    HRESULT hr = E_NOINTERFACE;

    IF_TRUE_ACTION_JUMP((NULL == ppvObject), hr = E_POINTER, Exit);
    *ppvObject = NULL;

    RETURN_INTERFACE(IUnknown, riid, ppvObject);
    RETURN_INTERFACE(IMFAttributes, riid, ppvObject);
    RETURN_INTERFACE(IMFOutputSchema, riid, ppvObject);

Exit:
    return hr;
}

// IUnknown::AddRef
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::AddRef() 
{
    ULONG uNewRefCount = InterlockedIncrement(&m_cRefCount);
    return uNewRefCount;
}

// IUnknown::Release
ULONG STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::Release() 
{
    ULONG uNewRefCount = InterlockedDecrement(&m_cRefCount);
    if (0 == uNewRefCount) 
    {
        delete this;
    }
    return uNewRefCount;
}
// IMFOutputSchema::GetConfigurationData
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetConfigurationData(__out DWORD *pdwVal) 
{
    if (NULL == pdwVal) { return E_POINTER; }
    *pdwVal = m_dwConfigData;
    return S_OK;
}

// IMFOutputSchema::GetOriginatorID
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetOriginatorID(__out GUID *pguidOriginatorID) 
{
    if (NULL == pguidOriginatorID) { return E_POINTER; }
    *pguidOriginatorID = m_guidOriginatorID;
    return S_OK;
}
// IMFOutputSchema::GetSchemaType
HRESULT STDMETHODCALLTYPE CTrustedAudioDriversOutputSchema::GetSchemaType(__out GUID *pguidSchemaType) 
{
    if (NULL == pguidSchemaType) { return E_POINTER; }
    *pguidSchemaType = MFPROTECTION_TRUSTEDAUDIODRIVERS;
    return S_OK;
}

//---------------------------------------------------------------------------------------------------
//
// Other subroutine declarations
//
//---------------------------------------------------------------------------------------------------
HRESULT CreateTrustedAudioDriversOutputPolicy(DWORD dwConfigData, IMFOutputPolicy **ppMFOutputPolicy) 
{
    if (NULL == ppMFOutputPolicy) 
    {
        return E_POINTER;
    }

    *ppMFOutputPolicy = NULL;

    HRESULT hr = S_OK;
    CTrustedAudioDriversOutputPolicy *pPolicy = new CTrustedAudioDriversOutputPolicy(dwConfigData, hr);
    if (NULL == pPolicy) 
    {
        return E_OUTOFMEMORY;
    }
    if (FAILED(hr)) 
    {
        delete pPolicy;
        return hr;
    }
    *ppMFOutputPolicy = static_cast<IMFOutputPolicy *>(pPolicy);
    return S_OK;
}// CreateTrustedAudioDriversOutputPolicy

HRESULT CreateTrustedAudioDriversOutputSchema
(
    DWORD dwConfigData,
    GUID guidOriginatorID,
    IMFOutputSchema **ppMFOutputSchema) 
{
    if (NULL == ppMFOutputSchema) 
    {
        return E_POINTER;
    }

    *ppMFOutputSchema = NULL;

    CTrustedAudioDriversOutputSchema *pSchema =
        new CTrustedAudioDriversOutputSchema(dwConfigData, guidOriginatorID);

    if (NULL == pSchema) 
    {
        return E_OUTOFMEMORY;
    }

    *ppMFOutputSchema = static_cast<IMFOutputSchema *>(pSchema);

    return S_OK;
}// CreateTrustedAudioDriversOutputSchema



HRESULT SetOTAPolicy(IMMDevice *_pMMDevice,
                     DWORD _dwConfigData,
                     IMFTrustedOutput **_ppMFTrustedOutput,
                     IMFOutputTrustAuthority **ppMFOutputTrustAuthority,
                     IMFOutputPolicy **_ppMFOutputPolicy)
{
    HRESULT hr = S_OK;

    DWORD dwCountOfOTAs = 0;
    bool bRet = false;

    hr = CreateTrustedAudioDriversOutputPolicy(_dwConfigData, _ppMFOutputPolicy);
    IF_FAILED_JUMP(hr, Exit);

    // activate IMFTrustedOutput
    hr = _pMMDevice->Activate(__uuidof(IMFTrustedOutput), CLSCTX_ALL, NULL,
                             (void**)_ppMFTrustedOutput);
    IF_FAILED_JUMP(hr, Exit);

    // get count of Output Trust Authorities on this trusted output
    hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityCount(&dwCountOfOTAs);
    IF_FAILED_JUMP(hr, Exit);

    // sanity check - fail on endpoints with no output trust authorities
    IF_TRUE_ACTION_JUMP((0 == dwCountOfOTAs), hr = E_NOTFOUND, Exit);

    printf("dwCountOfOTAs = %d\n", dwCountOfOTAs);

     
    // loop over each output trust authority on the endpoint
    for (DWORD i = 0; i < dwCountOfOTAs; i++) 
    {
        // get the output trust authority
        hr = (*_ppMFTrustedOutput)->GetOutputTrustAuthorityByIndex(i, ppMFOutputTrustAuthority);
        IF_FAILED_JUMP(hr, Exit);


        // log the purpose of the output trust authority
        MFPOLICYMANAGER_ACTION action;
        hr = (*ppMFOutputTrustAuthority)->GetAction(&action);
        if (FAILED(hr)) 
        {
            return hr;
        }

        printf(" It's %s.", (PEACTION_PLAY==action) ? "PEACTION_PLAY" :
                            (PEACTION_COPY==action) ? "PEACTION_COPY" :
                            "Others");
 
        // only PEACTION_PLAY Output Trust Authorities are relevant
        if (PEACTION_PLAY != action) 
        {
            printf("Skipping as the OTA action is not PEACTION_PLAY");
            SAFE_RELEASE(*ppMFOutputTrustAuthority);
            continue;
        }

        BYTE *pbTicket = NULL;
        DWORD cbTicket = 0;
        // audio ota does not support ticket, leaving it NULL is ok.
        hr = (*ppMFOutputTrustAuthority)->SetPolicy(_ppMFOutputPolicy, 1, &pbTicket, &cbTicket);
        IF_FAILED_JUMP(hr, Exit);
        printf("SetPolicy succeeded.\n");

        bRet = true;
        break;

    }// for each output trust authority

Exit:
    if (bRet)
    {
        hr = S_OK;
    }
    if (FAILED(hr))
    {
        printf("failure code is 0x%0x\n", hr);
        SAFE_RELEASE(*ppMFOutputTrustAuthority);
        SAFE_RELEASE(*_ppMFTrustedOutput);
        if (*_ppMFOutputPolicy)
        {
            delete (*_ppMFOutputPolicy);
        }
    }

    return hr;
}


HRESULT ClearOTAPolicy(IMFTrustedOutput *_pMFTrustedOutput,
                       IMFOutputTrustAuthority *_pMFOutputTrustAuthority,
                       IMFOutputPolicy *_pMFOutputPolicy)
{
    SAFE_RELEASE(_pMFOutputTrustAuthority);
    SAFE_RELEASE(_pMFTrustedOutput);
    if (_pMFOutputPolicy)
    {
        delete _pMFOutputPolicy;
    }
    return S_OK;
}
```




```cpp
//OTADSoundSample.rc
#include "windows.h"

/////////////////////////////////////////////////////////////////////////////
// Version
#include <ntverp.h>

#define VER_FILETYPE                VFT_DLL
#define VER_FILESUBTYPE             VFT2_UNKNOWN
#define VER_FILEDESCRIPTION_STR     "Default Device Heuristic Dumper"
#define VER_INTERNALNAME_STR        "DefaultDeviceDump.exe"
#define VER_ORIGINALFILENAME_STR    "DefaultDeviceDump.exe"

#include "common.ver"
```




```cpp
Sources file:

TARGETNAME=OTADSoundSample
TARGETTYPE=PROGRAM
TARGET_DESTINATION=retail
UMTYPE=console
UMENTRY=wmain
UMBASE=0x1000000
#_NT_TARGET_VERSION=$(_NT_TARGET_VERSION_VISTA)
MSC_WARNING_LEVEL=$(MSC_WARNING_LEVEL) /WX
USE_ATL=1
ATL_VER=70
USE_NATIVE_EH=1
USE_MSVCRT=1
C_DEFINES=-DUNICODE -D_UNICODE
INCLUDES=$(INCLUDES);  

SOURCES=OTADSoundSample.cpp \
        OTADSoundSample.rc \
        outputpolicy.cpp\

TARGETLIBS=\
       $(SDK_LIB_PATH)\advapi32.lib         \
       $(SDK_LIB_PATH)\kernel32.lib         \
       $(SDK_LIB_PATH)\User32.lib           \
       $(SDK_LIB_PATH)\shlwapi.lib          \
       $(SDK_LIB_PATH)\ole32.lib            \
       $(SDK_LIB_PATH)\oleaut32.lib         \
       $(SDK_LIB_PATH)\rpcrt4.lib           \
       $(SDK_LIB_PATH)\strmiids.lib         \
       $(SDK_LIB_PATH)\uuid.lib             \
       $(SDK_LIB_PATH)\SetupAPI.lib         \
       $(SDK_LIB_PATH)\mfplat.lib \
```



## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation](programming-guide.md)

[Composants audio en mode utilisateur](user-mode-audio-components.md)
