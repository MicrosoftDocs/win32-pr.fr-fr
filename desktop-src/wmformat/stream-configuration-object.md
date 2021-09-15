---
title: Configuration de flux, objet
description: Configuration de flux, objet
ms.assetid: 228e334c-9d9b-4604-a225-73af7af3255f
keywords:
- Windows Media Format SDK, Stream, objets de configuration
- ASF (Advanced Systems Format), objets de configuration de flux
- ASF (format de systèmes avancés), objets de configuration de flux
- objets, objets de configuration de flux
- objets de configuration de flux
- flux, objets de configuration de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e16a6c2221952e6102b76c49fee660888c9dcbc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525160"
---
# <a name="stream-configuration-object"></a>Configuration de flux, objet

Un objet de configuration de flux est utilisé pour spécifier les propriétés d’un flux de média dans un fichier ASF. Il est possible de créer des objets de configuration de flux pour des flux existants dans un profil ou de les créer vides, prêts à recevoir de nouvelles données. Les objets de configuration de flux ne peuvent pas exister indépendamment d’un objet de profil. Pour enregistrer le contenu d’un objet de configuration de flux, vous devez appeler [**IWMProfile :: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) pour ajouter un nouveau flux ou [**IWMProfile :: ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream) pour enregistrer les modifications apportées à un flux existant.

Pour créer un objet de configuration de flux, utilisez l’une des méthodes suivantes.



| Méthode                                                                | Description                                                                                                                      |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfile::CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)     | Crée un objet de configuration de flux sans aucune donnée.                                                                          |
| [**IWMProfile :: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                 | Crée un objet de configuration de flux rempli avec les données d’un profil. Utilise l’index de flux pour identifier le flux souhaité.  |
| [**IWMProfile::GetStreamByNumber**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) | Crée un objet de configuration de flux rempli avec les données d’un profil. Utilise le numéro de flux pour identifier le flux souhaité. |



 

Toutes les méthodes du tableau précédent définissent un pointeur vers une interface **IWMStreamConfig** . Les autres interfaces de l’objet de configuration Stream peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par l’objet de configuration de flux.



| Interface                                        | Description                                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | Définit et récupère la structure [**du \_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) pour le flux.                                    |
| [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)     | Définit et récupère les propriétés qui ne sont pas requises pour tous les flux, comme les paramètres de vitesse de transmission variable (VBR).                  |
| [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)       | Définit et récupère toutes les informations de base relatives à un flux.                                                              |
| [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)     | Configure les types d’extensions d’unité de données associées au flux. Hérite de toutes les méthodes de **IWMStreamConfig**. |
| [**IWMStreamConfig3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)     | Définit et récupère la langue du flux. Hérite de toutes les méthodes de **IWMStreamConfig** et **IWMStreamConfig2**. |
| [**IWMVideoMediaProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | Gère les propriétés d’un flux vidéo. Il s’agit d’une interface facultative qui est disponible uniquement pour les flux vidéo.            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Configuration de Flux**](configuring-streams.md)
</dt> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Gestionnaire de profils, objet**](profile-manager-object.md)
</dt> </dl>

 

 




