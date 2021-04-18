---
description: Cet article explique comment écrire un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Comment écrire un présentateur EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94933d9eb53b0b03105edc7056ace4fe73238d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564888"
---
# <a name="how-to-write-an-evr-presenter"></a>Comment écrire un présentateur EVR

Cet article explique comment écrire un présentateur personnalisé pour le convertisseur vidéo amélioré (EVR). Un présentateur personnalisé peut être utilisé avec DirectShow et Media Foundation ; les interfaces et le modèle objet sont les mêmes pour les deux technologies, bien que la séquence exacte d’opérations puisse varier.

L’exemple de code de cette rubrique est adapté de l' [exemple EVRPresenter](evrpresenter-sample.md), fourni dans le SDK Windows.

Cette rubrique contient les sections suivantes :

-   [Conditions préalables](#prerequisites)
-   [Modèle objet Presenter](#presenter-object-model)
    -   [Transmission de données à l’intérieur du EVR](#data-flow-inside-the-evr)
    -   [États du présentateur](#presenter-states)
    -   [Interfaces presenter](#presenter-interfaces)
    -   [Implémentation de IMFVideoDeviceID](#implementing-imfvideodeviceid)
    -   [Implémentation de IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)
    -   [Implémentation de IMFVideoPresenter](#implementing-imfvideopresenter)
    -   [Implémentation de IMFClockStateSink](#implementing-imfclockstatesink)
    -   [Implémentation de IMFRateSupport](#implementing-imfratesupport)
    -   [Envoi d’événements à EVR](#sending-events-to-the-evr)
-   [Négociation des formats](#negotiating-formats)
-   [Gestion de l’appareil Direct3D](#managing-the-direct3d-device)
    -   [Allouer des surfaces Direct3D](#allocating-direct3d-surfaces)
    -   [Exemples de suivi](#tracking-samples)
-   [Traitement de la sortie](#processing-output)
    -   [Redessiner des frames](#repainting-frames)
    -   [Exemples de planification](#scheduling-samples)
    -   [Présentation des exemples](#presenting-samples)
    -   [Rectangles de source et de destination](#source-and-destination-rectangles)
    -   [Fin de flux](#end-of-stream)
-   [Pas à pas](#frame-stepping)
    -   [Implémentation du pas à pas de frame](#implementing-frame-stepping)
-   [Définition du présentateur sur le EVR](#setting-the-presenter-on-the-evr)
    -   [Définition du présentateur dans DirectShow](#setting-the-presenter-in-directshow)
    -   [Définition du présentateur dans Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Avant d’écrire un présentateur personnalisé, vous devez être familiarisé avec les technologies suivantes :

-   Convertisseur vidéo amélioré. Consultez [rendu vidéo amélioré](enhanced-video-renderer.md).
-   Graphiques Direct3D. Vous n’avez pas besoin de comprendre les graphiques 3D pour écrire un présentateur, mais vous devez savoir comment créer un appareil Direct3D et gérer des surfaces Direct3D. Si vous n’êtes pas familiarisé avec Direct3D, lisez les sections « périphériques Direct3D » et « ressources Direct3D » dans la documentation du kit SDK DirectX Graphics.
-   Les graphiques de filtre DirectShow ou le pipeline Media Foundation, selon la technologie que votre application utilisera pour afficher la vidéo.
-   [Media Foundation transformations](media-foundation-transforms.md). Le mélangeur EVR est une transformation Media Foundation, et le présenteur appelle des méthodes directement sur le mélangeur.
-   Implémentation d’objets COM. Le présentateur est un objet COM libre-thread dans le processus.

## <a name="presenter-object-model"></a>Modèle objet Presenter

Cette section contient une vue d’ensemble du modèle objet et des interfaces du présentateur.

### <a name="data-flow-inside-the-evr"></a>Transmission de données à l’intérieur du EVR

Le EVR utilise deux composants de plug-in pour afficher la vidéo : le *mélangeur* et le *présentateur*. Le mélangeur fusionne les flux vidéo et désentrelace la vidéo si nécessaire. Le présentateur dessine (ou *présente*) la vidéo sur l’écran et planifie le dessin de chaque image. Les applications peuvent remplacer l’un de ces objets par une implémentation personnalisée.

Le EVR a un ou plusieurs flux d’entrée, et le mélangeur a un nombre correspondant de flux d’entrée. Le flux 0 est toujours le *flux de référence*. Les autres flux sont des sous- *flux*, que le mixer alpha sur le flux de référence. Le flux de référence détermine le taux d’images maître pour la vidéo composite. Pour chaque frame de référence, la fenêtre de mixage prend le frame le plus récent de chaque sous-flux, les mélange alpha sur le frame de référence et génère un seul Frame composite. Le mélangeur effectue également une conversion de désentrelacement et de couleur de YUV en RVB si nécessaire. Le EVR insère toujours le mixer dans le pipeline vidéo, quel que soit le nombre de flux d’entrée ou le format vidéo. L’illustration suivante montre ce processus.

![Diagramme montrant le flux de référence et le sous-flux pointant vers le mélangeur, qui pointe vers le présentateur, qui pointe vers l’affichage](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

Le présentateur effectue les tâches suivantes :

-   Définit le format de sortie sur le mélangeur. Avant le début de la diffusion en continu, le présentateur définit un type de média sur le flux de sortie de la console. Ce type de média définit le format de l’image composite.
-   Crée le périphérique Direct3D.
-   Alloue des surfaces Direct3D. Le mélangeur BLITS les images composites sur ces surfaces.
-   Obtient la sortie du mélangeur.
-   Planifie la présentation des frames. Le EVR fournit l’horloge de présentation et le présentateur planifie les frames en fonction de cette horloge.
-   Présente chaque frame à l’aide de Direct3D.
-   Effectue un pas à pas et un nettoyage de l’image.

### <a name="presenter-states"></a>États du présentateur

À tout moment, le présentateur est dans l’un des États suivants :

-   *Démarré*. L’horloge de présentation de EVR est en cours d’exécution. Le présentateur planifie des images vidéo pour la présentation à mesure qu’elles arrivent.
-   *Suspendu*. L’horloge de la présentation est suspendue. Le présentateur ne présente aucun nouvel exemple, mais conserve sa file d’attente d’exemples planifiés. Si de nouveaux exemples sont reçus, le présentateur les ajoute à la file d’attente.
-   *Arrêté*. L’horloge de la présentation est arrêtée. Le présentateur ignore tous les exemples qui ont été planifiés.
-   *Arrêtez*. Le présentateur libère toutes les ressources liées à la diffusion en continu, telles que les surfaces Direct3D. Il s’agit de l’état initial du présenteur et de l’état final avant la destruction du présentateur.

Dans l’exemple de code présenté dans cette rubrique, l’État présentateur est représenté par une énumération :


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Certaines opérations ne sont pas valides lorsque le présentateur est à l’état d’arrêt. L’exemple de code vérifie cet État en appelant une méthode d’assistance :


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a>Interfaces presenter

Un présentateur est requis pour implémenter les interfaces suivantes :



| Interface                                                                | Description                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Notifie le présenteur lorsque l’horloge du EVR change d’État. Consultez [implémentation de IMFClockStateSink](#implementing-imfclockstatesink).                                   |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Fournit un moyen pour l’application et d’autres composants dans le pipeline d’obtenir des interfaces du présentateur.                                                       |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permet au présenteur d’accéder aux interfaces à partir du EVR ou du mélangeur. Consultez [implémentation de IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient). |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Garantit que le présentateur et le mélangeur utilisent des technologies compatibles. Consultez [implémentation de IMFVideoDeviceID](#implementing-imfvideodeviceid).                          |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Traite les messages à partir du EVR. Consultez [implémentation de IMFVideoPresenter](#implementing-imfvideopresenter).                                                             |



 

Les interfaces suivantes sont facultatives :



| Interface                                                | Description                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Permet au présentateur de travailler avec des médias protégés. Implémentez cette interface si votre présentateur est un composant approuvé conçu pour fonctionner dans le chemin d’accès au média protégé (PMP). |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Indique la plage de vitesses de lecture que le présenteur prend en charge. Consultez [implémentation de IMFRateSupport](#implementing-imfratesupport).                                         |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mappe les coordonnées sur l’image vidéo de sortie à des coordonnées sur l’image vidéo d’entrée.                                                                                       |
| [**IQualProp**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Signale des informations sur les performances. EVR utilise ces informations pour la gestion du contrôle qualité. Cette interface est documentée dans le kit de développement logiciel (SDK) DirectShow.                        |



 

Vous pouvez également fournir des interfaces pour que l’application communique avec le présentateur. Le présentateur standard implémente l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) à cet effet. Vous pouvez implémenter cette interface ou définir les vôtres. L’application obtient les interfaces du présenteur en appelant [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur EVR. Lorsque le GUID du service est **MR_VIDEO_RENDER_SERVICE**, EVR transmet la demande **GetService** au présenteur.

### <a name="implementing-imfvideodeviceid"></a>Implémentation de IMFVideoDeviceID

L’interface [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contient une méthode, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), qui retourne un GUID de périphérique. Le GUID de l’appareil garantit que le présentateur et le mélangeur utilisent des technologies compatibles. Si les GUID d’appareil ne correspondent pas, l’initialisation du EVR échoue.

Le mélangeur et le présentateur standard utilisent Direct3D 9, avec le GUID de l’appareil égal à **IID_IDirect3DDevice9**. Si vous envisagez d’utiliser votre présentateur personnalisé avec le mélangeur standard, le GUID de l’appareil du présentateur doit être **IID_IDirect3DDevice9**. Si vous remplacez les deux composants, vous pouvez définir un nouveau GUID d’appareil. Pour le reste de cet article, il est supposé que le présentateur utilise Direct3D 9. Voici l’implémentation standard de [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid):


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



La méthode doit s’effectuer correctement même lorsque le présentateur est arrêté.

### <a name="implementing-imftopologyservicelookupclient"></a>Implémentation de IMFTopologyServiceLookupClient

L’interface [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) permet au présenteur d’extraire des pointeurs d’interface à partir du EVR et du mélangeur comme suit :

1.  Quand le EVR Initialise le présentateur, il appelle la méthode [**IMFTopologyServiceLookupClient :: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) du présentateur. L’argument est un pointeur vers l’interface [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) de EVR.
2.  Le présentateur appelle [**IMFTopologyServiceLookup :: LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) pour récupérer les pointeurs d’interface à partir de EVR ou du mixer.

La méthode [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) est semblable à la méthode [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) . Les deux méthodes prennent un GUID de service et un identificateur d’interface (IID) comme entrée, mais **LookupService** retourne un tableau de pointeurs d’interface, tandis que **GetService** retourne un pointeur unique. Dans la pratique, toutefois, vous pouvez toujours définir la taille du tableau sur 1. L’objet interrogé dépend du GUID de service :

-   Si le GUID du service est **MR_VIDEO_RENDER_SERVICE**, EVR est interrogé.
-   Si le GUID du service est **MR_VIDEO_MIXER_SERVICE**, le mélangeur est interrogé.

Dans votre implémentation de [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers), récupérez les interfaces suivantes à partir de EVR :



| Interface EVR                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Offre au présenteur un moyen d’envoyer des messages à EVR. Cette interface étant définie dans le kit de développement logiciel (SDK) DirectShow, les messages respectent le modèle pour les événements DirectShow, et non Media Foundation les événements.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**IMFClock**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Représente l’horloge du EVR. Le présentateur utilise cette interface pour planifier des exemples à des fins de présentation. Le EVR peut s’exécuter sans horloge. cette interface peut donc ne pas être disponible. Si ce n’est pas le cas, ignorez le code d’erreur de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice).<br/> L’horloge implémente également l’interface [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) . Dans le pipeline Media Foundation, l’horloge implémente l’interface [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) . Elle n’implémente pas cette interface dans DirectShow.<br/> |



 

Récupérez les interfaces suivantes à partir du mélangeur :



| Interface de mixage                              | Description                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Permet au présenteur de communiquer avec le mélangeur.       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Permet au présenteur de valider le GUID de l’appareil du mélangeur. |



 

Le code suivant implémente la méthode [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Lorsque les pointeurs d’interface obtenus à partir de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) ne sont plus valides, EVR appelle [**IMFTopologyServiceLookupClient :: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers). Dans cette méthode, libérez tous les pointeurs d’interface et définissez l’état du présentateur sur arrêt :


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



EVR appelle [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) pour diverses raisons, notamment :

-   La déconnexion ou la reconnexion des broches (DirectShow), ou l’ajout ou la suppression de récepteurs de flux (Media Foundation).
-   Modification du format.
-   Définition d’une nouvelle horloge.
-   Arrêt final du EVR.

Pendant la durée de vie du présentateur, le EVR peut appeler [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) et [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) plusieurs fois.

### <a name="implementing-imfvideopresenter"></a>Implémentation de IMFVideoPresenter

L’interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) hérite de [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) et ajoute deux méthodes :



| Méthode                                                               | Description                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Retourne le type de média des images vidéo composite. |
| [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Signale au présenteur d’effectuer diverses actions.      |



 

La méthode [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) retourne le type de média du présentateur. (Pour plus d’informations sur la définition du type de support, consultez [négociation de formats](#negotiating-formats).) Le type de média est retourné en tant que pointeur d’interface [**IMFVideoMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) . L’exemple suivant suppose que le présenteur stocke le type de média comme un pointeur [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Pour accéder à l’interface **IMFVideoMediaType** à partir du type de média, appelez **QueryInterface**:


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



La méthode [**ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) est le mécanisme principal de EVR pour communiquer avec le présentateur. Les messages suivants sont définis. Les détails de l’implémentation de chaque message sont donnés dans le reste de cette rubrique.



| Message                                | Description                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | Le type de média de sortie du mélangeur n’est pas valide. Le présentateur doit négocier un nouveau type de média avec le mélangeur. Consultez la page [négociation de formats](#negotiating-formats).                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | La diffusion en continu a démarré. Aucune action particulière n’est requise par ce message, mais vous pouvez l’utiliser pour allouer des ressources.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | La diffusion en continu est terminée. Libère toutes les ressources que vous avez allouées en réponse au message de **MFVP_MESSAGE_BEGINSTREAMING** .                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | Le mélangeur a reçu un nouvel exemple d’entrée et peut être en mesure de générer un nouveau frame de sortie. Le présentateur doit appeler [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mixer. Consultez [traitement](#processing-output)de la sortie. |
| **MFVP_MESSAGE_ENDOFSTREAM**         | La présentation est terminée. Voir la [fin du flux](#end-of-stream).                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | EVR vide les données dans son pipeline de rendu. Le présentateur doit ignorer toutes les images vidéo qui sont planifiées pour la présentation.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Demande au présentateur d’effectuer un pas à pas détaillé dans les N frames. Le présentateur doit ignorer les N-1 frames suivants et afficher le nième Frame. Consultez [exécution pas à pas de la trame](#frame-stepping).                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Annule le pas à pas de la trame.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Implémentation de IMFClockStateSink

Le présentateur doit implémenter l’interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) dans le cadre de son implémentation de [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), qui hérite de **IMFClockStateSink**. EVR utilise cette interface pour notifier le présenteur chaque fois que l’horloge du EVR change d’État. Pour plus d’informations sur les États d’horloge, consultez [Présentation Clock](presentation-clock.md).

Voici quelques recommandations pour implémenter les méthodes dans cette interface. Toutes les méthodes doivent échouer si le présenteur est arrêté.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></td>
<td><ol>
<li>Définissez l’État présentateur sur démarré.</li>
<li>Si le <em>llClockStartOffset</em> n’est pas <strong>PRESENTATION_CURRENT_POSITION</strong>, videz la file d’attente du présentateur des exemples. (Cela équivaut à recevoir un message de <strong>MFVP_MESSAGE_FLUSH</strong> .)</li>
<li>Si une demande d’étape de frame précédente est toujours en attente, traitez la demande (consultez <a href="#frame-stepping">exécution pas à pas de la trame</a>). Sinon, essayez de traiter la sortie à partir du mélangeur (consultez traitement de la <a href="#processing-output">sortie</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></td>
<td><ol>
<li>Définissez l’État présentateur sur arrêté.</li>
<li>Videz la file d’attente du présentateur des exemples.</li>
<li>Annulez toute opération de l’étape de frame en attente.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></td>
<td>Affectez à l’État présentateur la valeur Paused.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></td>
<td>Traitez le même que <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> , mais ne videz pas la file d’attente des exemples.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></td>
<td><ol>
<li>Si le taux passe de zéro à différent de zéro, annulez l’exécution pas à pas de la trame.</li>
<li>Stockez le nouveau taux d’horloge. Le taux d’horloge affecte le moment où les exemples sont présentés. Pour plus d’informations, consultez <a href="#scheduling-samples">planification des exemples</a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>Implémentation de IMFRateSupport

Pour prendre en charge des vitesses de lecture autres que 1 × vitesse, le présentateur doit implémenter l’interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) . Voici quelques recommandations pour implémenter les méthodes dans cette interface. Toutes les méthodes doivent échouer après l’arrêt du présentateur. Pour plus d’informations sur cette interface, consultez la page contrôle de la [fréquence](rate-control.md).



|                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Retourne zéro pour indiquer qu’il n’y a pas de vitesse de lecture minimale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | Pour une lecture non fine, la vitesse de lecture ne doit pas dépasser la fréquence d’actualisation du moniteur :  =  *taux de rafraîchissement* maximal (Hz)/fréquence d' *images vidéo* (FPS). La fréquence d’images vidéo est spécifiée dans le type de média du présentateur. <br/> Pour une lecture fine, le taux de lecture est illimité ; retourne la valeur **FLT_MAX**. Dans la pratique, la source et le décodeur seront les facteurs de limitation lors de la lecture fine. <br/> Pour la lecture inversée, retourne la valeur négative du taux maximal.<br/> |
| [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Retourne **MF_E_UNSUPPORTED_RATE** si la valeur absolue de *flRate* dépasse la vitesse de lecture maximale du présentateur. Calculez la vitesse de lecture maximale comme décrit pour [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).                                                                                                                                                                                                                                                                                    |



 

L’exemple suivant montre comment implémenter la méthode [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



L’exemple précédent appelle une méthode d’assistance, GetMaxRate, pour calculer la vitesse maximale de lecture en avant :

L’exemple suivant montre comment implémenter la méthode [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a>Envoi d’événements à EVR

Le présentateur doit notifier le EVR de divers événements. Pour ce faire, il utilise l’interface [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) de EVR, obtenue lorsque le EVR appelle la méthode [**IMFTopologyServiceLookupClient :: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) du présentateur. (L’interface **IMediaEventSink** est à l’origine une interface DirectShow, mais elle est utilisée à la fois dans le EVR DirectShow et dans le Media Foundation.) Le code suivant montre comment envoyer un événement à EVR :


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



Le tableau suivant répertorie les événements que le présenteur envoie, ainsi que les paramètres d’événement.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Événement</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>Le présentateur a terminé le rendu de toutes les trames après le message de MFVP_MESSAGE_ENDOFSTREAM.<br/>
<ul>
<li><em>Param1</em>: HRESULT indiquant l’état de l’opération.</li>
<li><em>Param2</em>: non utilisé.</li>
</ul>
Pour plus d’informations, consultez <a href="#end-of-stream">fin de flux</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>L’appareil Direct3D a changé.<br/>
<ul>
<li><em>Param1</em>: non utilisé.</li>
<li><em>Param2</em>: non utilisé.</li>
</ul>
Pour plus d’informations, consultez <a href="#managing-the-direct3d-device">gestion du périphérique Direct3D</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>Une erreur s’est produite et nécessite l’arrêt de la diffusion en continu.<br/>
<ul>
<li><em>Param1</em>: <strong>HRESULT</strong> indiquant l’erreur qui s’est produite.</li>
<li><em>Param2</em>: non utilisé.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>Spécifie la durée pendant laquelle le présentateur prend le rendu de chaque image. (Facultatif.)<br/>
<ul>
<li><em>Param1</em>: pointeur vers une valeur <strong>LongLong</strong> constante qui contient la durée de traitement de la trame, en unités de 100 nanosecondes.</li>
<li><em>Param2</em>: non utilisé.</li>
</ul>
Pour plus d’informations, consultez traitement de la <a href="#processing-output">sortie</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>Spécifie le temps de décalage actuel dans les échantillons de rendu. Si la valeur est positive, les exemples sont en arrière-plan. Si la valeur est négative, les échantillons sont en avance sur Schedule. (Facultatif.)<br/>
<ul>
<li><em>Param1</em>: pointeur vers une valeur <strong>LongLong</strong> constante qui contient le temps de retard, en unités de 100 nanosecondes.</li>
<li><em>Param2</em>: non utilisé.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>Envoyé immédiatement après <strong>EC_STEP_COMPLETE</strong> si la vitesse de lecture est égale à zéro. Cet événement contient l’horodatage du frame qui a été affiché.<br/>
<ul>
<li><em>Param1</em>: 32 bits inférieurs de l’horodatage.</li>
<li><em>Param2</em>: 32 bits supérieurs de l’horodatage.</li>
</ul>
Pour plus d’informations, consultez <a href="#frame-stepping">exécution pas à pas de la trame</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>Le présentateur a terminé ou annulé une étape de frame.<br/>
<ul>
<li><em>Param1</em>: non utilisé.</li>
<li><em>Param2</em>: non utilisé.</li>
</ul>
Pour plus d’informations, consultez <a href="#frame-stepping">exécution pas à pas de la trame</a>.<br/>
<blockquote>
[!Note]<br />
Une version précédente de la documentation A décrit <em>param1</em> de manière incorrecte. Ce paramètre n’est pas utilisé pour cet événement.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>Négociation des formats

Chaque fois que le présentateur reçoit un message de **MFVP_MESSAGE_INVALIDATEMEDIATYPE** à partir du EVR, il doit définir le format de sortie sur le mélangeur, comme suit :

1.  Appelez [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) sur le mélangeur pour obtenir un type de sortie possible. Ce type décrit un format que le mélangeur peut produire en fonction des flux d’entrée et des fonctionnalités de traitement vidéo du périphérique graphique.
2.  Vérifiez si le présentateur peut utiliser ce type de média comme format de rendu. Voici quelques éléments à vérifier, bien que votre implémentation puisse avoir ses propres exigences :

    -   La vidéo doit être décompressée.
    -   La vidéo ne doit comporter que des images progressives. Vérifiez que l’attribut [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) est égal à **MFVideoInterlace_Progressive**.
    -   Le format doit être compatible avec le périphérique Direct3D.

    Si le type n’est pas acceptable, revenez à l’étape 1 et récupérez le type proposé suivant de la console.

3.  Créez un nouveau type de média qui est un clone du type d’origine, puis modifiez les attributs suivants :

    -   Définissez l’attribut [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) égal à la largeur et à la hauteur souhaitées pour les surfaces Direct3D que vous allez allouer.
    -   Affectez la valeur **false** à l’attribut [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) .
    -   Affectez à l’attribut [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) égal au-dessus de l’affichage (généralement 1:1).
    -   Affectez à l’ouverture géométrique (attribut [**MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) ) une valeur égale à un rectangle dans la surface Direct3D. Lorsque le mélangeur génère un frame de sortie, il BLITS l’image source sur ce rectangle. L’ouverture géométrique peut être aussi grande que la surface, ou elle peut être un sous-rectangle dans la surface. Pour plus d’informations, consultez [rectangles source et destination](#source-and-destination-rectangles).

4.  Pour vérifier si le mélangeur accepte le type de sortie modifié, appelez [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) avec l’indicateur **MFT_SET_TYPE_TEST_ONLY** . Si le mélangeur rejette le type, revenez à l’étape 1 pour obtenir le type suivant.
5.  Allouez un pool de surfaces Direct3D, comme décrit dans [allocation de surfaces Direct3D](#allocating-direct3d-surfaces). Le mélangeur utilise ces surfaces lorsqu’il dessine les images vidéo composite.
6.  Définissez le type de sortie sur le mélangeur en appelant [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sans indicateurs. Si le premier appel à **SetOutputType** a réussi à l’étape 4, la méthode doit être réexécutée.

Si le mélangeur est en dehors des types, la méthode [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) retourne **MF_E_NO_MORE_TYPES**. Si le présenteur ne parvient pas à trouver un type de sortie approprié pour le mélangeur, le flux ne peut pas être rendu. Dans ce cas, DirectShow ou Media Foundation peuvent essayer un autre format de flux. Par conséquent, le présentateur peut recevoir plusieurs messages de **MFVP_MESSAGE_INVALIDATEMEDIATYPE** dans une ligne jusqu’à ce qu’un type valide soit trouvé.

Le mélangeur cadres automatiquement la vidéo, en tenant compte des proportions en pixels (PAR) de la source et de la destination. Pour de meilleurs résultats, la largeur et la hauteur de la surface et l’ouverture géométrique doivent être égales à la taille réelle dans laquelle vous souhaitez que la vidéo apparaisse sur l’affichage. L’illustration suivante montre ce processus.

![Diagramme montrant un minutage composite menant à une surface Direct3D, qui mène à une fenêtre](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

Le code suivant illustre le plan du processus. Certaines étapes sont placées dans les fonctions d’assistance, dont les détails exacts dépendent des exigences de votre présentateur.


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



Pour plus d’informations sur les types de média vidéo, consultez [Video Media types](video-media-types.md).

## <a name="managing-the-direct3d-device"></a>Gestion de l’appareil Direct3D

Le présentateur crée le périphérique Direct3D et gère toute perte d’appareil pendant la diffusion en continu. Le présentateur héberge également le gestionnaire de périphériques Direct3D, qui permet à d’autres composants d’utiliser le même appareil. Par exemple, le mélangeur utilise le périphérique Direct3D pour mélanger les sous-flux, le désentrelacement et effectuer des ajustements de couleurs. Les décodeurs peuvent utiliser l’appareil Direct3D pour le décodage accéléré vidéo. (Pour plus d’informations sur l’accélération vidéo, consultez [DirectX Video acceleration 2,0](directx-video-acceleration-2-0.md).)

Pour configurer le périphérique Direct3D, procédez comme suit :

1.  Créez l’objet Direct3D en appelant **Direct3DCreate9** ou **Direct3DCreate9Ex**.
2.  Créez l’appareil en appelant **IDirect3D9 :: CreateDevice** ou **IDirect3D9Ex :: CreateDevice**.
3.  Créez le gestionnaire de périphériques en appelant [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).
4.  Définissez l’appareil sur le gestionnaire de périphériques en appelant [**IDirect3DDeviceManager9 :: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).

Si un autre composant de pipeline a besoin du gestionnaire de périphériques, il appelle [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) sur le EVR, en spécifiant **MR_VIDEO_ACCELERATION_SERVICE** pour le GUID du service. Le EVR transmet la requête au présentateur. Une fois que l’objet a obtenu le pointeur [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) , il peut obtenir un handle vers l’appareil en appelant [**IDirect3DDeviceManager9 :: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle). Lorsque l’objet doit utiliser l’appareil, il passe le handle de l’appareil à la méthode [**IDirect3DDeviceManager9 :: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) , qui retourne un pointeur **IDirect3DDevice9** .

Une fois l’appareil créé, si le présentateur détruit l’appareil et en crée un nouveau, le présentateur doit appeler à nouveau [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) . La méthode **ResetDevice** invalide tous les descripteurs d’appareil existants, ce qui amène [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) à retourner **DXVA2_E_NEW_VIDEO_DEVICE**. Ce code d’erreur signale à d’autres objets utilisant l’appareil qu’ils doivent ouvrir un nouveau descripteur d’appareil. Pour plus d’informations sur l’utilisation du gestionnaire de périphériques, consultez [Direct3D gestionnaire de périphériques](direct3d-device-manager.md).

Le présentateur peut créer l’appareil en mode fenêtre ou exclusif en mode plein écran. Pour le mode fenêtre, vous devez fournir à l’application un moyen de spécifier la fenêtre vidéo. Le présentateur standard implémente la méthode [**IMFVideoDisplayControl :: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) à cet effet. Vous devez créer l’appareil lorsque le présentateur est créé pour la première fois. En règle générale, vous ne connaissez pas tous les paramètres de l’appareil à ce stade, tels que la fenêtre ou le format de la mémoire tampon d’arrière-plan. Vous pouvez créer un appareil temporaire et le remplacer ultérieurement&\# ; n’oubliez pas d’appeler [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) sur le gestionnaire de périphériques.

Si vous créez un nouveau périphérique ou si vous appelez **IDirect3DDevice9 :: Reset** ou **IDirect3DDevice9Ex :: ResetEx** sur un appareil existant, envoyez un événement [**EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) au EVR. Cet événement avertit EVR de renégocier le type de média. EVR ignore les paramètres d’événement pour cet événement.

### <a name="allocating-direct3d-surfaces"></a>Allouer des surfaces Direct3D

Une fois que le présentateur a défini le type de média, il peut allouer les surfaces Direct3D qui seront utilisées par le mélangeur pour écrire les images vidéo. La surface doit correspondre au type de média du présentateur :

-   Le format de surface doit correspondre au sous-type de média. Par exemple, si le sous-type est **MFVideoFormat_RGB24**, le format de surface doit être **D3DFMT_X8R8G8B8**. Pour plus d’informations sur les sous-types et les formats Direct3D, consultez [GUID sous-type de vidéo](video-subtype-guids.md).
-   La largeur et la hauteur de la surface doivent correspondre aux dimensions spécifiées dans l’attribut [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) du type de média.

La méthode recommandée pour allouer des surfaces varie selon que le présentateur s’exécute en mode fenêtre ou plein écran.

Si le périphérique Direct3D est fenêtre, vous pouvez créer plusieurs chaînes de permutation, chacune avec une seule mémoire tampon d’arrière-plan. À l’aide de cette approche, vous pouvez présenter chaque surface indépendamment, car la présentation d’une chaîne de permutation n’interfère pas avec les autres chaînes de permutation. Le mélangeur peut écrire des données sur une surface, tandis qu’une autre surface est planifiée pour la présentation.

Tout d’abord, déterminez le nombre de chaînes de permutation à créer. Un minimum de trois est recommandé. Pour chaque chaîne de permutation, procédez comme suit :

1.  Appelez **IDirect3DDevice9 :: CreateAdditionalSwapChain** pour créer la chaîne de permutation.
2.  Appelez **IDirect3DSwapChain9 :: GetBackBuffer** pour obtenir un pointeur vers la surface de mémoire tampon d’arrière-plan de la chaîne d’échange.
3.  Appelez [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) et transmettez un pointeur vers l’aire. Cette fonction retourne un pointeur vers un objet d’exemple vidéo. L’exemple d’objet Video implémente l’interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , et le présenteur utilise cette interface pour remettre la surface au mélangeur lorsque le présenteur appelle la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) du mixer. Pour plus d’informations sur l’exemple d’objet vidéo, consultez [Video Samples](video-samples.md)(en anglais).
4.  Stocke le pointeur [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dans une file d’attente. Le présentateur extraira les exemples de cette file d’attente pendant le traitement, comme décrit dans traitement de la [sortie](#processing-output).
5.  Conservez une référence au pointeur **IDirect3DSwapChain9** pour que la chaîne de permutation ne soit pas libérée.

En mode exclusif plein écran, l’appareil ne peut pas avoir plus d’une chaîne de permutation. Cette chaîne de permutation est créée implicitement lorsque vous créez l’appareil plein écran. La chaîne de permutation peut avoir plus d’une mémoire tampon d’arrière-plan. Malheureusement, toutefois, si vous présentez une mémoire tampon d’arrière-plan pendant que vous écrivez à une autre mémoire tampon d’arrière-plan dans la même chaîne de permutation, il n’existe aucun moyen simple de coordonner les deux opérations. Cela est dû à la façon dont Direct3D implémente la symétrie de surface. Lorsque vous appelez la présente, le pilote Graphics met à jour les pointeurs surface dans la mémoire graphique. Si vous maintenez des pointeurs **IDirect3DSurface9** quand vous appelez la méthode **present**, ceux-ci pointeront vers des mémoires tampons différentes après le retour de l’appel **présent** .

L’option la plus simple consiste à créer un exemple de vidéo pour la chaîne de permutation. Si vous choisissez cette option, suivez les mêmes étapes que pour le mode fenêtre. La seule différence est que la file d’attente de l’exemple contient un seul échantillon vidéo. Une autre option consiste à créer des surfaces hors écran, puis à les confondre avec la mémoire tampon d’arrière-plan. Les surfaces que vous créez doivent prendre en charge la méthode [**IDirectXVideoProcessor :: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) , que le mélangeur utilise pour compositiser les frames de sortie.

### <a name="tracking-samples"></a>Exemples de suivi

Lorsque le présentateur alloue d’abord les échantillons vidéo, il les place dans une file d’attente. Le présentateur dessine à partir de cette file d’attente chaque fois qu’il doit obtenir un nouveau Frame à partir du mélangeur. Une fois le mixage en sortie, le présentateur déplace l’exemple dans une deuxième file d’attente. La deuxième file d’attente est destinée aux exemples qui attendent leurs temps de présentation planifiés.

Pour faciliter le suivi de l’état de chaque exemple, l’objet Video Sample implémente l’interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) . Vous pouvez utiliser cette interface comme suit :

1.  Implémentez l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) dans votre présentateur.
2.  Avant de placer un exemple dans la file d’attente planifiée, interrogez l’exemple d’objet vidéo de l’interface [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) .

3.  Appelez [**IMFTrackedSample :: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) avec un pointeur vers votre interface de rappel.
4.  Lorsque l’exemple est prêt pour la présentation, supprimez-le de la file d’attente planifiée, présentez-le et publiez toutes les références à l’exemple.
5.  L’exemple appelle le rappel. (L’exemple d’objet n’est pas supprimé dans ce cas, car il contient un décompte de références sur lui-même jusqu’à ce que le rappel soit appelé.)
6.  Dans le rappel, retournez l’exemple à la file d’attente disponible.

Il n’est pas nécessaire qu’un présentateur utilise [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) pour suivre les exemples ; vous pouvez implémenter n’importe quelle technique qui fonctionne le mieux pour votre conception. L’un des avantages de **IMFTrackedSample** est que vous pouvez déplacer les fonctions de planification et de rendu du présentateur dans des objets d’assistance, et ces objets n’ont pas besoin d’un mécanisme spécial pour rappeler le présentateur lorsqu’ils déposent des exemples vidéo, car l’exemple d’objet fournit ce mécanisme.

Le code suivant montre comment définir le rappel :


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



Dans le rappel, appelez [**IMFAsyncResult :: GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) sur l’objet de résultat asynchrone pour récupérer un pointeur vers l’exemple :


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock **_/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /_*_ End lock _*_/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a>Traitement de la sortie

Chaque fois que la console reçoit un nouvel exemple d’entrée, EVR envoie un message _ *MFVP_MESSAGE_PROCESSINPUTNOTIFY** au présenteur. Ce message indique que le mélangeur peut avoir une nouvelle image vidéo à remettre. En réponse, le présentateur appelle [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mélangeur. Si la méthode est réussie, le présentateur planifie l’exemple pour la présentation.

Pour extraire la sortie du mélangeur, procédez comme suit :

1.  Vérifiez l’état de l’horloge. Si l’horloge est suspendue, ignorez le **MFVP_MESSAGE_PROCESSINPUTNOTIFY** message, sauf s’il s’agit de la première image vidéo. Si l’horloge est en cours d’exécution, ou s’il s’agit de la première image vidéo, continuez.
2.  Obtenir un exemple à partir de la file d’attente des exemples disponibles. Si la file d’attente est vide, cela signifie que tous les échantillons alloués sont actuellement planifiés pour la présentation. Dans ce cas, ignorez le message **MFVP_MESSAGE_PROCESSINPUTNOTIFY** pour l’instant. Lorsque l’exemple suivant devient disponible, répétez les étapes répertoriées ici.
3.  (Facultatif.) Si l’horloge est disponible, obtient l’heure actuelle de l’horloge (*T1*) en appelant [**IMFClock :: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).
4.  Appelez [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mixer. Si **ProcessOutput** fonctionne, l’exemple contient une image vidéo. Si la méthode échoue, vérifiez le code de retour. Les codes d’erreur suivants de **ProcessOutput** ne sont pas des échecs critiques :

    

    | Code d'erreur                              | Description                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | Le mélangeur a besoin d’une plus grande entrée avant de produire une nouvelle trame de sortie.<br/> Si vous obtenez ce code d’erreur, vérifiez si le EVR a atteint la fin du flux et répond en conséquence, comme décrit dans [fin de flux](#end-of-stream). Sinon, ignorez ce **MF_E_TRANSFORM_NEED_MORE_INPUT** message. Le EVR envoie un autre lorsque le mélangeur obtient davantage d’entrées.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | Le type de sortie du mélangeur est devenu non valide, peut-être en raison d’un changement de format en amont.<br/> Si vous recevez ce code d’erreur, attribuez la valeur **null** au type de média du présentateur. EVR demande un nouveau format.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | Le mélangeur requiert un nouveau type de média.<br/> Si vous recevez ce code d’erreur, renégociez le type de sortie du mélangeur comme décrit dans [négociation des formats](#negotiating-formats).<br/>                                                                                                                                                                                                        |

    

     

    Si [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) fonctionne, continuez.

5.  (Facultatif.) Si l’horloge est disponible, obtient l’heure actuelle de l’horloge (*T2*). La latence introduite par le mélangeur est (*T2*  -  *T1*). Envoie un événement **EC_PROCESSING_LATENCY** avec cette valeur au EVR. EVR utilise cette valeur pour le contrôle de la qualité. Si aucune horloge n’est disponible, il n’y a aucune raison d’envoyer l’événement **EC_PROCESSING_LATENCY** .
6.  (Facultatif.) Interrogez l’exemple pour [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) et appelez [**IMFTrackedSample :: SetAllocator**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) comme décrit dans exemples de [suivi](#tracking-samples).
7.  Planifiez l’exemple pour la présentation.

Cette séquence d’étapes peut se terminer avant que le présentateur ne récupère une sortie à partir du mélangeur. Pour vous assurer qu’aucune demande n’est supprimée, vous devez répéter les mêmes étapes dans les cas suivants :

-   La méthode [**IMFClockStateSink :: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou **IMFClockStateSink :: OnClockStart** du présentateur est appelée. Cela permet de gérer le cas où le mélangeur ignore l’entrée, car l’horloge est suspendue (étape 1).
-   Le rappel [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) est appelé. Cela permet de gérer le cas où le mélangeur reçoit l’entrée, mais tous les exemples vidéo du présentateur sont en cours d’utilisation (étape 2).

Les exemples de code suivants illustrent ces étapes plus en détail. Le présentateur appelle la `ProcessInputNotify` méthode (illustrée dans l’exemple suivant) lorsqu’il obtient le message de **MFVP_MESSAGE_PROCESSINPUTNOTIFY** .


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



Cette `ProcessInputNotify` méthode définit un indicateur booléen pour enregistrer le fait que le mélangeur a une nouvelle entrée. Elle appelle ensuite la `ProcessOutputLoop` méthode, illustrée dans l’exemple suivant. Cette méthode tente d’extraire autant d’échantillons que possible du mélangeur :


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



La `ProcessOutput` méthode, illustrée dans l’exemple suivant, tente d’obtenir une image vidéo unique à partir du mixer. Si aucune image vidéo n’est disponible, `ProcessSample` retourne S_FALSE ou un code d’erreur, l’un des deux qui interrompt la boucle dans `ProcessOutputLoop` . La majeure partie du travail est effectuée à l’intérieur de la `ProcessOutput` méthode :


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



Voici quelques remarques sur cet exemple :

-   La variable *m_SamplePool* est supposée être un objet de collection qui contient la file d’attente des exemples vidéo disponibles. La méthode de l’objet `GetSample` retourne **MF_E_SAMPLEALLOCATOR_EMPTY** si la file d’attente est vide.
-   Si la méthode [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) du mixer retourne MF_E_TRANSFORM_NEED_MORE_INPUT, cela signifie que le mélangeur ne peut pas produire plus de sortie, de sorte que le présenteur efface l’indicateur *m_fSampleNotify* .
-   La `TrackSample` méthode, qui définit le rappel [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) , est présentée dans la section [exemples de suivi](#tracking-samples).

### <a name="repainting-frames"></a>Redessiner des frames

Il peut arriver que le présentateur doive redessiner l’image vidéo la plus récente. Par exemple, le présentateur standard repeint le frame dans les cas suivants :

-   En mode fenêtre, en réponse à **WM_PAINT** messages reçus par la fenêtre de l’application. Consultez [**IMFVideoDisplayControl :: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   Si le rectangle de destination change quand l’application appelle [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Utilisez les étapes suivantes pour demander au mélangeur de recréer la trame la plus récente :

1.  Obtient un échantillon vidéo de la file d’attente.
2.  Interrogez l’exemple de l’interface [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .
3.  Appelez [**IMFDesiredSample :: SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration). Spécifiez l’horodatage de la trame vidéo la plus récente. (Vous devrez mettre en cache cette valeur et la mettre à jour pour chaque frame.)
4.  Appelez [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mixer.

Quand vous repeignez un frame, vous pouvez ignorer l’horloge de présentation et présenter immédiatement le cadre.

### <a name="scheduling-samples"></a>Exemples de planification

Les trames vidéo peuvent atteindre le EVR à tout moment. Le présentateur est responsable de la présentation de chaque frame à l’heure correcte, en fonction de l’horodatage du frame. Lorsque le présenteur obtient un nouvel exemple à partir du mélangeur, il place l’exemple dans la file d’attente planifiée. Sur un thread distinct, le présentateur obtient continuellement le premier échantillon du début de la file d’attente et détermine s’il faut :

-   Présentez l’exemple.
-   Conservez l’exemple dans la file d’attente, car il est précoce.
-   Ignorez l’exemple, car il est tardif. Bien que vous deviez éviter de supprimer des frames si possible, vous devrez peut-être le faire si le présentateur est continuellement en retard.

Pour obtenir l’horodatage d’une image vidéo, appelez [**IMFSample :: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) sur l’exemple vidéo. L’horodatage est relatif à l’horloge de présentation de EVR. Pour connaître l’heure actuelle de l’horloge, appelez [**IMFClock :: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime). Si le EVR n’a pas d’horloge de présentation, ou si un exemple n’a pas d’horodatage, vous pouvez présenter l’exemple immédiatement après l’avoir obtenu.

Pour connaître la durée de chaque exemple, appelez [**IMFSample :: GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration). Si l’exemple n’a pas de durée, vous pouvez utiliser la fonction [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) pour calculer la durée à partir de la fréquence d’images.

Lorsque vous planifiez des exemples, gardez à l’esprit les points suivants :

-   Si la vitesse de lecture est plus rapide ou plus lente que la vitesse normale, l’horloge s’exécute à une vitesse plus rapide ou plus lente. Cela signifie que l’horodatage d’un échantillon donne toujours l’heure cible correcte relative à l’horloge de la présentation. Toutefois, si vous traduisez les temps de présentation dans une autre période (par exemple, le compteur de performances haute résolution), vous devez mettre à l’échelle les heures en fonction de la fréquence d’horloge. Si la vitesse de l’horloge change, EVR appelle la méthode [**IMFClockStateSink :: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) du présentateur.
-   La vitesse de lecture peut être négative pour la lecture inversée. Lorsque la vitesse de lecture est négative, l’horloge de la présentation s’exécute en arrière. En d’autres termes, l’heure *n* + 1 se produit avant l’heure *n*.

L’exemple suivant calcule le début ou la fin d’un exemple, par rapport à l’horloge de présentation :


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



L’horloge de présentation est généralement pilotée par l’horloge système ou le convertisseur audio. (Le convertisseur audio dérive l’heure à partir de la vitesse à laquelle la carte son consomme des données audio.) En général, l’horloge de la présentation n’est pas synchronisée avec la fréquence d’actualisation de l’analyse.

Si vos paramètres de présentation Direct3D spécifient **D3DPRESENT_INTERVAL_DEFAULT** ou **D3DPRESENT_INTERVAL_ONE** pour l’intervalle de présentation, l’opération **actuelle** attend le retraçage vertical de l’analyse. Il s’agit d’un moyen simple d’éviter les déchirures, mais réduit la précision de votre algorithme de planification. À l’inverse, si l’intervalle de présentation est **D3DPRESENT_INTERVAL_IMMEDIATE**, la méthode **présente** s’exécute immédiatement, ce qui entraîne une suppression, à moins que votre algorithme de planification ne soit suffisamment précis pour que vous appeliez **présent** uniquement pendant la période de retrace verticale.

Les fonctions suivantes peuvent vous aider à obtenir des informations de temporisation précises :

-   **IDirect3DDevice9 :: GetRasterStatus** retourne des informations sur le raster, y compris la ligne de numérisation actuelle et si le raster est dans la période vide verticale.
-   **DwmGetCompositionTimingInfo** retourne les informations de minutage du gestionnaire de fenêtrage. Ces informations sont utiles si la composition du Bureau est activée.

### <a name="presenting-samples"></a>Présentation des exemples

Cette section part du principe que vous avez créé une chaîne de permutation distincte pour chaque surface, comme décrit dans [allocation de surfaces Direct3D](#allocating-direct3d-surfaces). Pour présenter un exemple, récupérez la chaîne de permutation de l’exemple de vidéo comme suit :

1.  Appelez [**IMFSample :: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) sur l’exemple de vidéo pour récupérer la mémoire tampon.
2.  Interrogez la mémoire tampon de l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
3.  Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour accéder à l’interface **IDirect3DSurface9** de la surface Direct3D. (Vous pouvez combiner cette étape et l’étape précédente en une en appelant [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)
4.  Appelez **IDirect3DSurface9 :: GetContainer** sur la surface pour obtenir un pointeur vers la chaîne de permutation.
5.  Appelez **IDirect3DSwapChain9 ::P renvoyée** sur la chaîne de permutation.

Le code suivant illustre ces étapes :


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a>Rectangles de source et de destination

Le *rectangle source* est la partie de l’image vidéo à afficher. Elle est définie par rapport à un système de coordonnées normalisé, dans lequel la totalité de la trame vidéo occupe un rectangle avec des coordonnées {0, 0, 1, 1}. Le *rectangle de destination* est la zone dans la surface de destination dans laquelle la vidéo est dessinée. Le présentateur standard permet à une application de définir ces rectangles en appelant [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Il existe plusieurs options pour l’application des rectangles source et de destination. La première option consiste à laisser le mélangeur les appliquer :

-   Définissez le rectangle source à l’aide de l’attribut [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) . Le mélangeur applique le rectangle source lorsqu’il BLITS la vidéo à la surface de destination. Le rectangle source par défaut du mélangeur est le cadre entier.
-   Définissez le rectangle de destination en tant qu’ouverture géométrique dans le type de sortie du mélangeur. Pour plus d’informations, consultez la page relative à la [négociation des formats](#negotiating-formats).

La deuxième option consiste à appliquer les rectangles quand vous **IDirect3DSwapChain9 ::P renvoyé** en spécifiant les paramètres *pSourceRect* et *pDestRect* dans la méthode **présente** . Vous pouvez combiner ces options. Par exemple, vous pouvez définir le rectangle source sur le mélangeur, mais appliquer le rectangle de destination dans la méthode **présente** .

Si l’application modifie le rectangle de destination ou redimensionne la fenêtre, vous devrez peut-être allouer de nouvelles surfaces. Dans ce cas, vous devez veiller à synchroniser cette opération avec votre thread de planification. Videz la file d’attente de planification et ignorez les anciens exemples avant d’allouer de nouvelles surfaces.

### <a name="end-of-stream"></a>Fin de flux

Lorsque chaque flux d’entrée sur le EVR est terminé, EVR envoie un message **MFVP_MESSAGE_ENDOFSTREAM** au présenteur. Toutefois, lorsque vous recevez le message, il se peut qu’il reste quelques images vidéo à traiter. Avant de répondre au message de fin de flux, vous devez décharger toute la sortie du mélangeur et présenter tous les autres frames. Une fois la dernière image présentée, envoyez un événement **EC_COMPLETE** à l’EVR.

L’exemple suivant montre une méthode qui envoie l’événement **EC_COMPLETE** si différentes conditions sont remplies. Sinon, elle retourne S_OK sans envoyer l’événement :


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



Cette méthode vérifie les États suivants :

-   Si la variable *m_fSampleNotify* a la **valeur true**, cela signifie que le mélangeur a une ou plusieurs trames qui n’ont pas encore été traitées. (Pour plus d’informations, consultez traitement de la [sortie](#processing-output).)
-   La variable *m_fEndStreaming* est un indicateur booléen dont la valeur initiale est **false**. Le présentateur affecte la **valeur true** à l’indicateur lorsque EVR envoie le MESSAGE de **MFVP_MESSAGE_ENDOFSTREAM** .
-   La `AreSamplesPending` méthode est supposée retourner la **valeur true** tant qu’un ou plusieurs frames sont en attente dans la file d’attente planifiée.

Dans la méthode [**IMFVideoPresenter ::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) , affectez la valeur **true** à *M_FENDSTREAMING* et appelez `CheckEndOfStream` lorsque le EVR envoie le message **MFVP_MESSAGE_ENDOFSTREAM** :


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



En outre, appelez `CheckEndOfStream` si la méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) du mixer retourne **MF_E_TRANSFORM_NEED_MORE_INPUT**. Ce code d’erreur indique que le mélangeur n’a plus d’exemples d’entrée (voir [traitement de sortie](#processing-output)).

## <a name="frame-stepping"></a>Pas à pas

Le EVR est conçu pour prendre en charge le pas à pas détaillé dans DirectShow et le nettoyage dans Media Foundation. L’exécution pas à pas et le nettoyage des images sont similaires d’un plan conceptuel. Dans les deux cas, l’application demande une image vidéo à la fois. En interne, le présenteur utilise le même mécanisme pour implémenter les deux fonctionnalités.

Le pas à pas détaillé dans DirectShow fonctionne comme suit :

-   L’application appelle [**IVideoFrameStep :: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step). Le nombre d’étapes est indiqué dans le paramètre *dwSteps* . EVR envoie un message **MFVP_MESSAGE_STEP** au présenteur, où le paramètre de message (*ulParam*) est le nombre d’étapes.
-   Si l’application appelle [**IVideoFrameStep :: CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) ou modifie l’état du graphique (en cours d’exécution, suspendu ou arrêté), le EVR envoie un MESSAGE de **MFVP_MESSAGE_CANCELSTEP** .

Le nettoyage dans Media Foundation fonctionne comme suit :

-   L’application définit la vitesse de lecture sur zéro en appelant [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)se.
-   Pour afficher un nouveau Frame, l’application appelle [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) avec la position souhaitée. EVR envoie un message de **MFVP_MESSAGE_STEP** avec *ulParam* égal à 1.
-   Pour arrêter le nettoyage, l’application définit la vitesse de lecture sur une valeur différente de zéro. EVR envoie le message **MFVP_MESSAGE_CANCELSTEP** .

Après avoir reçu le message **MFVP_MESSAGE_STEP** , le présentateur attend l’arrivée du frame cible. Si le nombre d’étapes est *N*, le présentateur ignore les exemples (*n* -1) suivants et présente le *N* ième échantillon. Lorsque le présenteur termine l’étape de frame, il envoie un événement [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) à l’EVR avec *LParam1* défini sur **false**. En outre, si la vitesse de lecture est égale à zéro, le présentateur envoie un événement [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) . Si le EVR annule le pas à pas de la trame pendant qu’une opération de l’étape de frame est toujours en attente, le présentateur envoie un événement **EC_STEP_COMPLETE** avec *LParam1* défini sur **true**.

L’application peut effectuer un frame ou un nettoyage à plusieurs moments. le présentateur peut donc recevoir plusieurs messages de **MFVP_MESSAGE_STEP** avant d’obtenir un message **MFVP_MESSAGE_CANCELSTEP** . En outre, le présentateur peut recevoir le message de **MFVP_MESSAGE_STEP** avant le démarrage de l’horloge ou pendant l’exécution de l’horloge.

### <a name="implementing-frame-stepping"></a>Implémentation du pas à pas de frame

Cette section décrit un algorithme permettant d’implémenter l’exécution pas à pas de frame. L’algorithme d’exécution pas à pas de Frame utilise les variables suivantes :

-   *step_count*. Entier non signé qui spécifie le nombre d’étapes dans l’opération de pas à pas de l’image en cours.
-   *step_queue*. Une file d’attente de pointeurs [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) .
-   *step_state*. À tout moment, le présentateur peut être dans l’un des États suivants en ce qui concerne le pas à pas détaillé de la trame : 

    | State         | Description                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Pas de cadre pas à pas.                                                                                                                                                                                             |
    | WAITING       | Le présentateur a reçu le message **MFVP_MESSAGE_STEP** , mais l’horloge n’a pas démarré.                                                                                                                  |
    | PENDING       | Le présentateur a reçu le message **MFVP_MESSAGE_STEP** et l’horloge a démarré, mais le présentateur attend de recevoir le frame cible.                                                             |
    | PLANIFIÉE     | Le présentateur a reçu le frame cible et l’a planifié pour la présentation, mais le cadre n’a pas été présenté.                                                                                        |
    | Remplissez      | Le présentateur a présenté le frame cible et a envoyé l’événement [**EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) et attend le MESSAGE de **MFVP_MESSAGE_STEP** ou de **MFVP_MESSAGE_CANCELSTEP** suivant. |

    

     

    Ces États sont indépendants des États de présenteur répertoriés dans la section [États du présentateur](#presenter-states).

Les procédures suivantes sont définies pour l’algorithme de pas à pas :

Procédure PrepareFrameStep

1.  Incrémente *step_count*.
2.  Définissez *step_state* sur Waiting.
3.  Si l’horloge est en cours d’exécution, appelez StartFrameStep.

Procédure StartFrameStep

1.  Si *step_state* est égal à en attente, affectez la valeur en attente à *step_state* . Pour chaque exemple dans *step_queue*, appelez DeliverFrameStepSample.
2.  Si *step_state* est égal à NOT_STEPPING, supprimez les exemples de *step_queue* et planifiez-les pour la présentation.

Procédure CompleteFrameStep

1.  Définissez *step_state* sur terminé.
2.  Envoyez l’événement EC_STEP_COMPLETE avec *lParam1*  =  **false**.
3.  Si la fréquence d’horloge est égale à zéro, envoyez l’événement **EC_SCRUB_TIME** avec l’heure de l’exemple.

Procédure DeliverFrameStepSample

1.  Si la fréquence d’horloge est égale à zéro et *échantillonner*  +  la *durée* de l’exemple de temps  <  *horloge*, ignorez l’exemple. Quitter.
2.  Si *step_state* est égal à planifié ou terminé, ajoutez l’exemple à *step_queue*. Quitter.
3.  Décrémenter *step_count*.
4.  Si *step_count* > 0, ignorez l’exemple. Quitter.
5.  Si *step_state* est égal à Waiting, ajoutez l’exemple à *step_queue*. Quitter.
6.  Planifiez l’exemple pour la présentation.
7.  Définissez *step_state* sur planifié.

Procédure CancelFrameStep

1.  Définissez *step_state* sur NOT_STEPPING
2.  Réinitialisez *step_count* à zéro.
3.  Si la valeur précédente de *step_state* était en attente, en attente ou planifiée, envoyez EC_STEP_COMPLETE avec *lParam1*  =  **true**.

Appelez ces procédures comme suit :



| Message ou méthode presenter                                                   | Procédure           |
|-------------------------------------------------------------------------------|---------------------|
| MESSAGE **MFVP_MESSAGE_STEP**                                               | `PrepareFrameStep`  |
| MESSAGE **MFVP_MESSAGE_STEP**                                               | `CancelStep`        |
| [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| Rappel [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)                         | `CompleteFrameStep` |
| [**IMFClockStateSink::OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

L’organigramme suivant présente les procédures pas à pas.

![organigramme indiquant les chemins qui commencent par mfvp \- message \- Step et mfvp \- message \- processinputnotify et se terminent par « State = Complete »](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Définition du présentateur sur le EVR

Après avoir implémenté le présentateur, l’étape suivante consiste à configurer le EVR pour l’utiliser.

### <a name="setting-the-presenter-in-directshow"></a>Définition du présentateur dans DirectShow

Dans une application DirectShow, définissez le présentateur sur le EVR comme suit :

1.  Créez le filtre EVR en appelant **CoCreateInstance**. Le CLSID est **CLSID_EnhancedVideoRenderer**.
2.  Ajoutez le EVR au graphique de filtre.
3.  Créez une instance de votre présentateur. Votre présentateur peut prendre en charge la création d’objets COM standard via **IClassFactory**, mais ce n’est pas obligatoire.
4.  Interrogez le filtre EVR pour l’interface [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
5.  Appelez [**IMFVideoRenderer :: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

### <a name="setting-the-presenter-in-media-foundation"></a>Définition du présentateur dans Media Foundation

Dans Media Foundation, vous avez plusieurs options, selon que vous créez le récepteur multimédia EVR ou l’objet d’activation EVR. Pour plus d’informations sur les objets d’activation, consultez [objets d’activation](activation-objects.md).

Pour le récepteur multimédia EVR, procédez comme suit :

1.  Appelez [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) pour créer le récepteur multimédia.
2.  Créez une instance de votre présentateur.
3.  Interrogez le récepteur multimédia EVR pour l’interface [**IMFVideoRenderer**](/windows/desktop/api/evr/nn-evr-imfvideorenderer) .
4.  Appelez [**IMFVideoRenderer :: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer).

Pour l’objet d’activation EVR, procédez comme suit :

1.  Appelez [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) pour créer l’objet d’activation.
2.  Définissez l’un des attributs suivants sur l’objet d’activation : 

    | Attribut                                                                                                         | Description                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Pointeur vers un objet d’activation pour le présentateur.<br/> Avec cet indicateur, vous devez fournir un objet d’activation pour votre présentateur. L’objet d’activation doit implémenter l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID du présentateur.<br/> Avec cet indicateur, votre présentateur doit prendre en charge la création d’objets COM standard via **IClassFactory**.<br/>                                                                                         |

    

     

3.  Si vous le souhaitez, définissez l’attribut [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) sur l’objet d’activation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> <dt>

[Exemple EVRPresenter](evrpresenter-sample.md)
</dt> </dl>

 

 
