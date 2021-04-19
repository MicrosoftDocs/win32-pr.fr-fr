---
description: Comment lire des fichiers qui contiennent des médias protégés par DRM.
ms.assetid: 85d98f49-8af2-42ce-9b36-a025aee93f73
title: Comment lire des fichiers multimédias protégés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f8f7af78881e43f2f7f85e8f333ab31b1bc2de
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537170"
---
# <a name="how-to-play-protected-media-files"></a>Comment lire des fichiers multimédias protégés

Un fichier multimédia protégé est un fichier multimédia associé à des règles d’utilisation du contenu. Dans certains cas, un fichier multimédia protégé est chiffré à l’aide d’une forme de chiffrement DRM (Digital Rights Management). Pour lire un fichier multimédia protégé, la lecture doit être effectuée à l’intérieur du chemin d’accès du support protégé (PMP). En outre, l’utilisateur peut avoir à acquérir des droits sur le contenu.

Le terme acquisition des droits fait référence à toute action que l’application doit exécuter avant que l’utilisateur puisse lire le contenu. L’exemple le plus courant consiste à obtenir une licence DRM, mais Media Foundation définit un mécanisme générique qui peut prendre en charge d’autres types d’acquisition de droits. L’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) définit ce mécanisme générique.

L’acquisition des droits doit être effectuée en dehors du PMP, du processus de l’application. La session multimédia avertit l’application par le biais de l’interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) , qui est implémentée par l’application. La session multimédia utilise l’interface **IMFContentProtectionManager** pour transférer un objet d’activateur de contenu à l’application. Les activateurs de contenu implémentent l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . L’application utilise cette interface pour acquérir les droits nécessaires.

Un activateur de contenu peut prendre en charge l’acquisition de droits automatique, auquel cas l’activateur de contenu implémente l’ensemble du processus, et l’application surveille simplement l’État. Dans le cas contraire, l’application doit utiliser l’acquisition des droits non silencieux, qui est un processus dans lequel l’application envoie des données HTTP après à une URL fournie par l’activateur de contenu.

Pour lire un média protégé, une application suit les mêmes étapes que celles indiquées dans la rubrique [Comment lire des fichiers multimédias avec Media Foundation](how-to-play-unprotected-media-files.md), en suivant les étapes supplémentaires suivantes :

1.  Demander si la source du média contient du contenu protégé. (Facultatif.)
2.  Créez la session multimédia dans le processus PMP au lieu du processus d’application.
3.  Effectuer l’acquisition des droits, si elle est notifiée par la session multimédia. Cette opération est effectuée de façon asynchrone par l’application.
4.  Terminez l’opération asynchrone.

## <a name="query-for-protected-content"></a>Rechercher du contenu protégé

Pour demander si une source multimédia contient du contenu protégé, appelez la fonction [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) sur le descripteur de présentation de la source du média. Si la fonction retourne la valeur \_ OK, vous devez utiliser le PMP pour lire le contenu. Si la fonction retourne la \_ valeur false, l’PMP n’est pas obligatoire et vous pouvez créer la session multimédia dans le processus d’application. Vous pouvez également utiliser le PMP pour lire les deux types de contenu, protégés et non protégés. Dans ce cas, vous n’avez pas besoin d’appeler **MFRequireProtectedEnvironment**.

Pour plus d’informations sur les descripteurs de présentation, consultez [descripteurs de présentation](presentation-descriptors.md).

## <a name="create-the-pmp-media-session"></a>Créer la session de média PMP

Pour créer la session multimédia dans le PMP, appelez [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Cette fonction est similaire à [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession), mais au lieu de créer la session multimédia dans le processus de l’application, elle crée la session multimédia dans le processus PMP. L’application reçoit un pointeur vers un objet proxy pour la session multimédia. L’application appelle les méthodes [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) sur l’objet proxy, tout comme il le ferait sur la session multimédia. L’objet proxy transfère les appels à la session multimédia à travers la limite de processus.

Créez la session de média PMP comme suit :

1.  Créez un nouveau magasin d’attributs en appelant [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).
2.  Définissez l' [**attribut \_ \_ Content \_ protection \_ Manager de la session MF**](mf-session-content-protection-manager-attribute.md) sur le magasin d’attributs. La valeur de cet attribut est un pointeur vers l’implémentation de [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)de votre application. Appelez [**IMFAttributes :: setunknown,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) pour définir l’attribut.
3.  Appelez [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) pour créer la session multimédia dans le processus PMP. Le paramètre *pConfiguration* est un pointeur vers l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) du magasin d’attributs.


```C++
IMFAttributes *pAttributes = NULL;
IMFMediaSession *pSession = NULL;

// Create the attribute store.
hr = MFCreateAttributes(&pAttributes, 1);

// Set the IMFContentProtectionManager pointer.
if (SUCCEEDED(hr))
{
    hr = pAttributes->SetUnknown(
        MF_SESSION_CONTENT_PROTECTION_MANAGER, 
        pCPM  // Your implementation of IMFContentProtectionManager.
        );
}

// Create the Media Session.
if (SUCCEEDED(hr))
{
    hr = MFCreatePMPMediaSession(
        0,
        pAttributes, 
        &pSession,
        NULL
    );
}

SAFE_RELEASE(pAttributes); // Release the attribute store.
// Use the Media Session to control playback (not shown).
```



Ensuite, créez une topologie de lecture et la met en file d’attente sur la session multimédia, comme décrit dans [création de topologies de lecture](creating-playback-topologies.md).

## <a name="perform-rights-acquisition"></a>Effectuer une acquisition de droits

Si la lecture nécessite une acquisition de droits, la session multimédia appelle [**IMFContentProtectionManager :: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Le paramètre *pEnablerActivate* de cette méthode est un pointeur vers l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Utilisez cette interface pour créer l’objet activateur de contenu, qui expose l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) . Utilisez ensuite l’activateur de contenu pour effectuer l’opération d’acquisition de droits.

Pour créer l’activateur de contenu, appelez [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject):


```C++
IMFContentEnabler *pEnabler = NULL;
hr = pEnablerActivate->ActivateObject(
    IID_IMFContentEnabler, 
    (void**)&pEnabler
    );
```



Interrogez le pointeur [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) retourné pour l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Utilisez cette interface pour récupérer des événements de l’objet d’activation du contenu. Pour plus d’informations sur les événements, consultez [Media Event Generator](media-event-generators.md).

Pour déterminer si l’activateur de contenu prend en charge l’acquisition automatique, appelez [**IMFContentEnabler :: IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported). Si cette méthode retourne la valeur **true**, l’application doit utiliser l’acquisition automatique. Dans le cas contraire, utilisez une acquisition non silencieuse.

La méthode [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) est asynchrone. L’application doit effectuer l’étape d’acquisition sur le thread de l’application. Une approche consiste à poster un message de fenêtre privée dans la fenêtre principale de l’application, en notifiant au thread d’application d’effectuer l’acquisition. Pendant que l’opération est en attente, l’application doit stocker le pointeur de rappel et l’objet d’État qu’il a reçu dans les paramètres *pCallback* et *punkState* de **BeginEnableContent**. Elles seront utilisées pour terminer l’opération asynchrone.

### <a name="automatic-acquisition"></a>Acquisition automatique

Pour effectuer une acquisition automatique, appelez [**IMFContentEnabler :: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable). Cette méthode est asynchrone. Une fois l’opération terminée, l’activateur de contenu envoie un événement [MEEnablerCompleted](meenablercompleted.md) . Le code d’état de l’événement indique si l’opération a réussi. Si le code d’état de l’événement MEEnablerCompleted est NS \_ E \_ DRM \_ License \_ NOTACQUIRED, l’application doit essayer d’utiliser une acquisition non silencieuse.

Pendant que l’opération d’acquisition est en cours, l’objet activateur peut envoyer l’événement [MEEnablerProgress](meenablerprogress.md) pour indiquer la progression de l’opération. Pour annuler l’opération, appelez [**IMFContentEnabler :: Cancel**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-cancel).

### <a name="non-silent-acquisition"></a>Acquisition non silencieuse

Si la méthode [**IsAutomaticSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-isautomaticsupported) retourne la **valeur false** ou si la méthode [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) échoue avec le code d’erreur \_ NOTACQUIRED de \_ licence DRM E \_ \_ , l’application doit effectuer une acquisition non silencieuse comme décrit dans les étapes suivantes :

1.  Appelez [**IMFContentEnabler :: GetEnableURL**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl) pour obtenir l’URL de l’acquisition de droits. Cette méthode retourne également un indicateur qui spécifie si l’URL est approuvée.
2.  Appelez [**IMFContentEnabler :: GetEnableData**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata) pour accéder aux données http de publication.
3.  Appelez [**IMFContentEnabler :: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable). Cette méthode permet à l’activateur du contenu de surveiller la progression de l’action d’acquisition des droits.

4.  Envoyer les données à l’URL d’acquisition des droits à l’aide d’une action HTTP POSTALe. Vous pouvez utiliser le contrôle Internet Explorer ou les API Windows Internet (WinINet).

Le code suivant illustre les étapes 1 à 3. L’étape 4 dépend des exigences spécifiques de votre application.


```C++
WCHAR   *sURL = NULL;  // URL.
DWORD   cchURL = 0;    // Size of the URL in characters.

// Trust status of the URL.
MF_URL_TRUST_STATUS  trustStatus = MF_LICENSE_URL_UNTRUSTED;

BYTE    *pPostData = NULL;  // Buffer to hold HTTP POST data.
DWORD   cbPostDataSize = 0; // Size of the buffer, in bytes.

HRESULT hr = S_OK;

// Get the URL. 
hr = m_pEnabler->GetEnableURL(&sURL, &cchURL, &trustStatus);

if (SUCCEEDED(hr))
{
    if (trustStatus != MF_LICENSE_URL_TRUSTED)
    {
        // The URL is not trusted. Do not proceed.
        hr = E_FAIL;
    }
}

// Monitor the rights acquisition. 
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->MonitorEnable();
}

// Get the HTTP POST data.
if (SUCCEEDED(hr))
{
    hr = m_pEnabler->GetEnableData(&pPostData, &cbPostDataSize);
}

// Open the URL and send the HTTP POST data. (Not shown.)

// Release the buffers.
CoTaskMemFree(pPostData);
CoTaskMemFree(sURL);
```



Une fois l’opération terminée, l’activateur de contenu envoie un événement [MEEnablerCompleted](meenablercompleted.md) .

## <a name="complete-the-asynchronous-operation"></a>Terminer l’opération asynchrone

Lorsque l’acquisition des droits est terminée, avec succès ou dans le cas contraire, l’application doit notifier la session multimédia en appelant le pointeur de rappel fourni dans la méthode [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .

1.  Créez un objet de résultat asynchrone en appelant [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult).
2.  Appelez le rappel de la session multimédia en appelant [**MFInvokeCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfinvokecallback).
3.  La session multimédia appellera [**IMFContentProtectionManager :: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent). Dans votre implémentation de cette méthode, libérez tous les pointeurs ou ressources que vous avez alloués dans [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent). Retourne un **HRESULT** qui indique la réussite globale de l’opération. Si l’acquisition des droits a échoué ou si l’utilisateur a annulé son exécution, retournez un code d’erreur.

Le code suivant montre comment créer le résultat asynchrone et appeler le rappel.


```C++
IMFAsyncResult  *pResult = NULL;

// Create the asynchronous result object.
hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);

// Invoke the callback.
if (SUCCEEDED(hr))
{
    pResult->SetStatus(hrStatus);
    hr = MFInvokeCallback(pResult);
}
SAFE_RELEASE(pResult);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> </dl>

 

 



