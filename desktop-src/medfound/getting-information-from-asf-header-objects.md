---
description: Les informations d’en-tête ASF sont stockées dans les objets d’en-tête ASF d’un fichier multimédia.
ms.assetid: 1654af97-f4fe-427f-b562-3b109e921719
title: Obtention d’informations à partir d’objets d’en-tête ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25155929c9e3ba7e59ee1b5f46ea7c5930c3e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531928"
---
# <a name="getting-information-from-asf-header-objects"></a>Obtention d’informations à partir d’objets d’en-tête ASF

Les informations d’en-tête ASF sont stockées dans les objets d’en-tête ASF d’un fichier multimédia. Media Foundation fournit l' [objet ASF ContentInfo](asf-contentinfo-object.md) pour fonctionner avec l’objet d’en-tête. Un objet ContentInfo rempli est requis pour permettre à l’application de lire les informations d’en-tête d’un fichier existant. Pour ce faire, appelez [**IMFASFContentInfo ::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader). Si l’analyse se termine correctement, la bibliothèque ASF du fichier, qui est géré en interne par Media Foundation, est remplie avec les informations d’en-tête de divers objets d’en-tête. Certaines de ces propriétés sont exposées à l’application, qu’elle peut récupérer via des attributs du descripteur de présentation, du descripteur de flux, du profil et des propriétés de métadonnées.

Pour obtenir la liste complète des attributs, consultez [Media Foundation attributs pour les objets d’en-tête ASF](media-foundation-attributes-for-asf-header-objects.md).

## <a name="retrieving-header-information-from-a-presentation-descriptor"></a>Récupération d’informations d’en-tête à partir d’un descripteur de présentation

Un objet descripteur de présentation contient la description d’une source multimédia particulière, dans ce cas, la source du média ASF. Si l’appel **ParseHeader** se termine correctement, les informations au niveau du fichier de l’objet d’en-tête sont stockées en tant qu’attributs sur le descripteur de présentation. Pour créer le descripteur de présentation, appelez [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Cette méthode retourne un pointeur vers un objet de descripteur de présentation rempli qui contient ces attributs pour le fichier ASF associé à l’objet ContentInfo. Pour obtenir des valeurs pour des attributs spécifiques, appelez les méthodes **IMFAttributes :: GetXXX** sur le descripteur de présentation et spécifiez l’attribut **MF \_ PD \_ ASF \_ xxx** .

L’exemple de code suivant récupère la durée de lecture d’un fichier ASF, spécifiée par un objet ContentInfo.


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



Pour plus d’informations sur les descripteurs de présentation en général, consultez [descripteurs de présentation](presentation-descriptors.md).

Pour obtenir l’ensemble complet des attributs du descripteur de présentation, consultez [attributs du descripteur de présentation](presentation-descriptor-attributes.md).

## <a name="retrieving-header-information-from-a-stream-descriptor"></a>Récupération d’informations d’en-tête à partir d’un descripteur de flux

Un objet descripteur de flux expose l’interface [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) et décrit les caractéristiques des flux dans le fichier. Le descripteur de présentation pour le contenu ASF contient un ou plusieurs descripteurs de flux qui représentent les flux listés dans l’objet d’en-tête. Une fois l’appel à [**IMFASFContentInfo :: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) terminé, les descripteurs de flux sous-jacents sont remplis avec les informations au niveau du flux des différents objets d’en-tête. Pour obtenir un descripteur de flux pour un flux ASF, appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) sur le descripteur de présentation généré à partir de l’objet ContentInfo.

Certaines propriétés de flux sont définies en tant qu’attributs sur les descripteurs de flux. Appelez les méthodes **IMFAttributes :: GetXXX** sur un descripteur de flux et spécifiez l’attribut **MF \_ SD \_ ASF \_ xxx** .

Pour obtenir l’ensemble complet des attributs du descripteur de flux, consultez « descripteur de flux spécifique aux ASF » dans [attributs du descripteur de flux](stream-descriptor-attributes.md).

## <a name="retrieving-header-information-from-the-profile-object"></a>Récupération des informations d’en-tête de l’objet de profil

Outre les descripteurs de flux, l’objet de profil ASF décrit également les propriétés de flux. Pour récupérer le profil d’un fichier ASF existant, appelez [**IMFASFContentInfo :: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). L’objet de profil ASF retourné par cette méthode n’inclut aucun des attributs **MF \_ PD \_ ASF \_ xxx** . Ces attributs sont disponibles pour l’application uniquement après avoir appelé [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor) pour générer l’objet de profil à partir d’un descripteur de présentation. Vous pouvez utiliser le profil pour atteindre des pointeurs vers les objets d’exclusion mutuelle et de priorité de flux.

Pour plus d’informations sur l’objet profil, consultez [ASF Profile](asf-profile.md) .

## <a name="retrieving-metadata-from-header-objects"></a>Récupération de métadonnées à partir d’objets d’en-tête

Un fichier ASF peut contenir plusieurs propriétés de métadonnées qui sont définies lors de l’encodage du fichier. Une application peut énumérer ces propriétés avec l’objet ContentInfo. Certaines de ces propriétés, telles que les informations VBR (variable bit rate), sont disponibles pour l’application via des attributs sur le descripteur de présentation, les descripteurs de flux et les types de média pour le fichier multimédia. Ces attributs sont définis sur l’objet ContentInfo pendant l’initialisation via l’appel [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objet ASF ContentInfo](asf-contentinfo-object.md)
</dt> </dl>

 

 



