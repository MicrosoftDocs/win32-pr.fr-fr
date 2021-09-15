---
title: Utilisation de types d’exclusion mutuelles personnalisés
description: Utilisation de types d’exclusion mutuelles personnalisés
ms.assetid: 9a4d760c-80af-4c67-823d-6da2732671ff
keywords:
- IWMMutualExclusion
- exclusion mutuelle, interface IWMMutualExclusion
- exclusion mutuelle, types personnalisés
- profils, types d’exclusion mutuelle personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 051e95bfb3f5ef8e39af31368227cf4918b897d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521036"
---
# <a name="using-custom-mutual-exclusion-types"></a>Utilisation de types d’exclusion mutuelles personnalisés

Vous pouvez utiliser des objets d’exclusion mutuelle dans un profil pour répondre aux besoins des scénarios personnalisés. En passant la valeur GUID CLSID \_ WMMUTEX \_ inconnu à [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype), vous indiquez à l’objet d’exclusion mutuelle que vous utilisez un scénario personnalisé.

Vous devez contrôler manuellement la sélection de flux quand vous lisez un fichier avec une valeur d’exclusion mutuelle personnalisée. L’objet lecteur utilise le premier flux que vous ajoutez à l’exclusion mutuelle comme valeur par défaut.

Procédez comme suit pour créer un objet d’exclusion mutuelle personnalisée et l’ajouter à un profil :

1.  Créez un gestionnaire de profils en appelant la fonction [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
2.  Démarrez avec un profil existant, ou créez-en un entièrement nouveau.
    -   Si vous utilisez un profil existant, appelez l’une des méthodes Load de l’interface [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) . Passez ensuite à l’étape 4.
    -   Si vous créez un profil entièrement nouveau, appelez [**IWMProfileManager :: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).
3.  Ajoutez des flux au nouveau profil en appelant [**IWMProfile :: CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream). Configurez les flux en fonction des besoins à l’aide des méthodes de [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig). Vous pouvez également appeler **QueryInterface** pour accéder à d’autres interfaces dans l’objet de configuration Stream.

    **CreateNewStream** crée uniquement un objet de configuration de flux et n’affecte pas le profil. Une fois qu’un flux est correctement configuré, vous devez appeler [**IWMProfile :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) pour ajouter le flux au profil.

4.  Créez un objet d’exclusion mutuelle en appelant [**IWMProfile :: CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion).
5.  Ajoutez les flux souhaités à l’objet exclusion mutuelle en appelant [**IWMStreamList :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamlist-addstream) (disponible directement à partir de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion), qui hérite de [**IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)).
6.  Définissez le type d’exclusion mutuelle sur personnalisé en appelant [**IWMMutualExclusion :: setType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype). Transmettez le CLSID \_ WMMUTEX \_ Unknown comme GUID de type.
7.  Ajoutez l’objet exclusion mutuelle configurée au profil en appelant [**IWMProfile :: AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**Interface IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Interface IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Interface IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Interface IWMStreamList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)
</dt> <dt>

[**Utilisation de l’exclusion mutuelle**](using-mutual-exclusion.md)
</dt> <dt>

[**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
</dt> </dl>

 

 




