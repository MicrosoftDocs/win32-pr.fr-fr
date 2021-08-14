---
description: Cette rubrique explique comment créer en tant que profil ASF dans Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Création d’un profil ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a0225a6ff17f68c5443fce15f9bdc196901313ccaaebdde2f7f34c49860538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743246"
---
# <a name="creating-an-asf-profile"></a>Création d’un profil ASF

Cette rubrique explique comment créer en tant que profil ASF dans Microsoft Media Foundation.

-   [Créer un nouveau profil](#create-a-new-profile)
-   [Récupérer le profil à partir de l’objet ASF ContentInfo](#get-the-profile-from-the-asf-contentinfo-object)
-   [Obtenir le profil à partir d’un descripteur de présentation](#get-the-profile-from-a-presentation-descriptor)
-   [Rubriques connexes](#related-topics)

## <a name="create-a-new-profile"></a>Créer un nouveau profil

Pour créer un profil ASF vide, appelez la fonction [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) . Cette fonction retourne un pointeur vers l’interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) . L’application peut utiliser cette interface pour ajouter des flux au profil et configurer chacun des flux. Pour plus d’informations, consultez [création et configuration d’flux ASF](creating-and-configuring-asf-streams.md).

L’application peut éventuellement ajouter des objets d’exclusion mutuelle à deux flux ou plus. Consultez [utilisation de l’exclusion mutuelle pour les flux ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Récupérer le profil à partir de l’objet ASF ContentInfo

Une application peut récupérer le profil ASF d’un fichier ASF existant à partir de l' [objet ASF ContentInfo](asf-contentinfo-object.md). Le profil est déjà configuré et contient des paramètres pour tous les flux du fichier.

Initialisez l’objet ContentInfo en analysant l’objet d’en-tête ASF du fichier. Cela s’effectue par le biais de la méthode [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . Une fois tous les objets d’en-tête lus et la bibliothèque ASF remplie, le profil de ce fichier est généré. L’application peut obtenir un pointeur vers ce profil initialisé en appelant [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Obtenir le profil à partir d’un descripteur de présentation

Vous pouvez obtenir l’objet de profil d’un fichier ASF existant à partir du [descripteur de présentation](presentation-descriptors.md) pour le fichier ou à partir de l’objet [ASF ContentInfo](asf-contentinfo-object.md) . Dans ce cas, le profil est déjà configuré et contient des paramètres pour tous les flux du fichier. Cela peut être utile si vous souhaitez modifier un profil ASF existant. par exemple, vous souhaiterez peut-être recoder un fichier de Windows Media Video à une vitesse de transmission inférieure.

Pour récupérer le profil à partir du descripteur de présentation, appelez [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). Cette fonction analyse le descripteur de présentation et remplit un profil ASF avec des informations sur le fichier multimédia. La fonction retourne un pointeur vers l’interface IMFASFProfile. Vous pouvez ensuite utiliser cette interface pour modifier le profil.

Pour récupérer le descripteur de présentation, appelez l’une des méthodes suivantes :

-   À partir de la source de média ASF, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   À partir de l’objet [ASF ContentInfo](asf-contentinfo-object.md) , appelez [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Avant d’appeler cette méthode, assurez-vous que l’objet ContentInfo est initialisé pour la lecture. Pour plus d’informations, consultez « initialisation de l’objet ContentInfo à partir d’un fichier ASF existant » dans [lecture de l’objet d’en-tête ASF d’un fichier existant](reading-the-asf-header-object-of-an-existing-file.md). Toutefois, si vous disposez déjà d’un objet ContentInfo initialisé, vous pouvez obtenir le profil directement à partir de celui-ci. Cela est décrit dans la section « obtention du profil à partir de l’objet ContentInfo », plus loin dans cette rubrique.

L’exemple suivant montre comment créer un profil à partir d’un descripteur de présentation. La fonction crée une source de média pour le fichier, obtient le descripteur de présentation à partir de la source du média et crée un profil. Cet exemple suppose que *pszFileName* spécifie l’URL d’un fichier ASF.


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



Cet exemple utilise [SafeRelease](saferelease.md) pour libérer des pointeurs d’interface.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Profil ASF](asf-profile.md)
</dt> </dl>

 

 



