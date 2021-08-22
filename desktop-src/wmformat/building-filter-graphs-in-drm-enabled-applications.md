---
title: Création de graphiques de filtre dans les applications DRM-Enabled
description: Création de graphiques de filtre dans les applications DRM-Enabled
ms.assetid: 447bec2a-0982-4a05-87bb-aed6db684b36
keywords:
- Windows Media Format SDK, création de graphiques de filtres
- Windows Media Format SDK, DirectShow
- Windows Kit de développement logiciel (SDK) Media format, applications compatibles DRM
- ASF (Advanced Systems Format), création de graphiques de filtres
- ASF (format des systèmes avancés), création de graphiques de filtres
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- ASF (Advanced Systems Format), applications compatibles DRM
- ASF (Advanced Systems Format), applications compatibles DRM
- DirectShow, création de graphiques de filtres
- DirectShow, applications compatibles DRM
- gestion des droits numériques (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
- gestion des droits numériques (DRM), création de graphiques de filtres
- DRM (gestion des droits numériques), création de graphiques de filtres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e7f411a52c0ce7c42410c7a901787c7f6d9d7089921019639cb3f5e708dff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447949"
---
# <a name="building-filter-graphs-in-drm-enabled-applications"></a>Création de graphiques de filtre dans les applications DRM-Enabled

si votre application DirectShow prend en charge la lecture de fichiers protégés par drm, vous ne devez généralement pas utiliser **RenderFile** pour créer le graphique de filtre, car il n’existe aucun moyen de spécifier les droits DRM que vous demandez avant l’ouverture du fichier. Par défaut, le lecteur ASF WM demande uniquement des droits de lecture. Le filtre n’est pas ajouté au graphique et n’est donc pas détectable par les applications, jusqu’à ce qu’un fichier soit ouvert avec succès.

Pour créer un graphique de lecture compatible DRM à l’aide du [lecteur ASF WM](wm-asf-reader-filter.md), vous devez instancier le filtre à l’aide de **CoCreateInstance**, l’ajouter au graphique de filtre à l’aide de **IGraphBuilder :: AddFilter**, le configurer, puis restituer ses broches de sortie. Cette technique est illustrée dans l’exemple PlayWndASF. Lorsque vous générez le graphique de cette manière, vous disposez déjà du pointeur **IBaseFilter** qui peut être utilisé pour appeler **QueryService** afin d’obtenir **IWMDRMWriter**. toutefois, cette interface n’est pas disponible tant que l’objet lecteur du kit de développement logiciel (SDK) Windows Media Format n’est pas créé en interne par le lecteur ASF WM. La première opportunité pour laquelle l’application doit définir les droits DRM est dans son WMT \_ aucun \_ Gestionnaire d' \_ événements (par exemple), comme indiqué dans cet extrait de code :


```C++
case WMT_NO_RIGHTS_EX:

    IServiceProvider *pServiceProvider;
    IWMDRMReader pWMDRMReader;
    JIF(g_pReader->QueryInterface(IID_IServiceProvider, (void **) &pServiceProvider));
    JIF(pServiceProvider->QueryService(IID_IWMDRMReader, IID_IWMDRMReader, (void **) &pWMDRMReader)); 
    SAFE_RELEASE(pServiceProvider);

    // Set the rights we want for this file. These are the actions we 
    // might want to perform on the file. Here we ask for two rights only.
    // In a real application you should enable users to select which 
    // rights they want.
    hr = pWMDRMReader->SetDRMProperty(g_wszWMDRM_Rights, WMT_TYPE_STRING,
        BYTE*) wszRights, (sizeof(wszRights) / sizeof(wszRights[0])) * 2);
    SAFE_RELEASE(pWMDRMReader);
    if (FAILED(hr))
    {
       Msg(TEXT("SetDRMProperty Failed!  hr=0x%x\n"), hr);
       return hr;
    }
    // Now proceed with license acqusition.
    if( pEventData->pData )
    {
        hr = HandleNoRightsEx(pEventData->hrStatus, 
        (WM_GET_LICENSE_DATA *)pEventData->pData);
    }
    else
    {
         hr = E_FAIL;
    }
    break;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités de Rights Management numérique**](digital-rights-management-features.md)
</dt> <dt>

[**Liste des attributs DRM**](drm-attribute-list.md)
</dt> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> <dt>

[**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> </dl>

 

 




