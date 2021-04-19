---
description: Descripteurs de présentation
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descripteurs de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527358"
---
# <a name="presentation-descriptors"></a>Descripteurs de présentation

Une *Présentation* est un ensemble de flux multimédia associés qui partagent un temps de présentation commun. Par exemple, une présentation peut comporter des flux audio et vidéo provenant d’un film. Un *descripteur de présentation* est un objet qui contient la description d’une présentation particulière. Les descripteurs de présentation sont utilisés pour configurer les sources multimédias et certains récepteurs multimédias.

Chaque descripteur de présentation contient une liste d’un ou plusieurs *descripteurs de flux*. Ils décrivent les flux dans la présentation. Les flux peuvent être sélectionnés ou désélectionnés. Seuls les flux sélectionnés produisent des données. Les flux désélectionnés ne sont pas actifs et ne produisent aucune donnée. Chaque descripteur de flux a un *Gestionnaire de type de média*, qui est utilisé pour modifier le type de média du flux ou obtenir le type de média actuel du flux. (Pour plus d’informations sur les types de médias, consultez [types de média](media-types.md).)

Le tableau suivant présente les interfaces principales exposées par chacun de ces objets.



| Object                  | Interface                                                      |
|-------------------------|----------------------------------------------------------------|
| Descripteur de présentation | [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| Descripteur de flux       | [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| Gestionnaire de type de média      | [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a>Présentations sources multimédias

Chaque source de média fournit un descripteur de présentation qui décrit la configuration par défaut de la source. Dans la configuration par défaut, au moins un flux est sélectionné, et chaque flux sélectionné a un type de média. Pour récupérer le descripteur de présentation, appelez [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). La méthode retourne un pointeur [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .

Vous pouvez modifier le descripteur de présentation de la source pour sélectionner un autre ensemble de flux. Ne modifiez pas le descripteur de présentation, sauf si la source du média est arrêtée. Les modifications sont appliquées quand vous appelez [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) pour démarrer la source.

Pour connaître le nombre de flux, appelez [**IMFPresentationDescriptor :: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount). Pour obtenir le descripteur de flux pour un flux, appelez [**IMFPresentationDescriptor :: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) et transmettez l’index du flux. Les flux sont indexés à partir de zéro. La méthode **GetStreamDescriptorByIndex** retourne un pointeur [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) . Elle retourne également un indicateur booléen qui indique si le flux est sélectionné. Si le flux est sélectionné, la source du média produit des données pour ce flux. Dans le cas contraire, la source ne produit pas de données pour ce flux. Pour sélectionner un flux, appelez [**IMFPresentationDescriptor :: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) avec l’index du flux. Pour désélectionner un flux, appelez [**IMFPresentationDescriptor ::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).

Le code suivant montre comment obtenir le descripteur de présentation à partir d’une source multimédia et comment énumérer les flux.


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a>Gestionnaires de type de média

Pour modifier le type de média du flux ou pour récupérer le type de média actuel du flux, utilisez le gestionnaire de type de média du descripteur de flux. Appelez [**IMFStreamDescriptor :: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) pour accéder au gestionnaire de type de média. Cette méthode retourne un pointeur [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .

Si vous souhaitez simplement connaître le type de données dans le flux, par exemple audio ou vidéo, appelez [**IMFMediaTypeHandler :: GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype). Cette méthode retourne le GUID pour le type de média principal. Par exemple, une application de lecture connecte généralement un flux audio au convertisseur audio et un flux vidéo au convertisseur vidéo. Si vous utilisez la session de média ou le chargeur de topologie pour créer une topologie, le GUID de type principal peut être les seules informations de format dont vous avez besoin.

Si votre application a besoin d’informations plus détaillées sur le format actuel, appelez [**IMFMediaTypeHandler :: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Cette méthode retourne un pointeur vers l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) du type de média. Utilisez cette interface pour récupérer les détails du format.

Le gestionnaire de type de média contient également une liste de types de média pris en charge pour le flux. Pour connaître la taille de la liste, appelez [**IMFMediaTypeHandler :: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount). Pour obtenir un type de média à partir de la liste, appelez [**IMFMediaTypeHandler :: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) avec l’index du type de média. Les types de média sont retournés dans l’ordre de préférence approximatif. Par exemple, pour les formats audio, des taux d’échantillonnage plus élevés sont préférés par rapport aux taux d’échantillonnage inférieurs. Toutefois, il n’existe aucune règle définitive qui régit le classement. vous devez donc le traiter simplement comme une indication.

La liste des types pris en charge peut ne pas contenir tous les types de médias pris en charge par le flux. Pour vérifier si un type de média particulier est pris en charge, appelez [**IMFMediaTypeHandler :: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported). Pour définir le type de média, appelez [**IMFMediaTypeHandler :: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Si la méthode est réussie, le flux contient des données conformes au format spécifié. La méthode **SetCurrentMediaType** ne modifie pas la liste des types préférés.

Le code suivant montre comment récupérer le gestionnaire de type de média, comment énumérer les types de média préférés et comment définir le type de média. Cet exemple suppose que l’application possède un algorithme, non illustré ici, pour la sélection du type de média. Les spécificités dépendent beaucoup de votre application.


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sources multimédias](media-sources.md)
</dt> <dt>

[API de plateforme Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



