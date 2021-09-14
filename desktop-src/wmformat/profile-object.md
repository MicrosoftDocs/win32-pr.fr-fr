---
title: Profile (objet)
description: Profile (objet)
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media Format SDK, objets de profil
- ASF (Advanced Systems Format), objets de profil
- ASF (format des systèmes avancés), objets de profil
- objets, objets de profil
- profils, objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234534"
---
# <a name="profile-object"></a>Profile (objet)

Un objet de profil gère les paramètres d’un profil. Vous pouvez créer des objets de profil pour les données de profil existantes ou les créer vides, prêts à recevoir de nouvelles données. Un objet de profil est également créé par l’objet lecteur (et l’objet lecteur synchrone) lorsqu’un fichier est chargé pour la lecture. Dans ce cas, l’objet est rempli avec les informations de profil stockées dans l’en-tête du fichier.

Pour enregistrer le contenu d’un objet de profil, vous devez appeler [**IWMProfileManager :: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).

Un profil contient plusieurs objets qui contrôlent différents aspects du profil (tels que les flux). Tous ces objets sont subordonnés à l’objet de profil. Vous ne créez pas ces objets avec les fonctions de création, comme vous le feriez avec les principaux objets de ce kit de développement logiciel (SDK). Au lieu de cela, les interfaces de l’objet de profil contiennent des méthodes qui créent les objets subordonnés.

Pour créer un objet de profil, appelez l’une des méthodes suivantes.



| Méthode                                                                                | Description                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | Crée un objet de profil sans données de profil.                                                                                                              |
| [**IWMProfileManager::LoadProfileByData**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | Crée un objet de profil rempli avec les données d’un profil enregistré en tant que chaîne. Il s’agit de la seule façon de créer un objet de profil avec les données d’un profil personnalisé. |
| [**IWMProfileManager::LoadProfileByID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | Crée un objet de profil rempli avec les données d’un profil système. Utilise le GUID pour identifier le profil système souhaité.                                       |
| [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | Crée un objet de profil rempli avec les données d’un profil système. Utilise l’index de profil pour identifier le profil système souhaité.                              |



 

Toutes les méthodes du tableau précédent définissent un pointeur vers une interface **IWMProfile** . Les autres interfaces de l’objet de profil peuvent être obtenues en appelant la méthode **QueryInterface** .

Les interfaces suivantes sont prises en charge par chaque objet de profil.



| Interface                                  | Description                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | Gère une liste de langues prises en charge par un fichier ASF.                                                                                             |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | Contrôle la taille maximale des paquets dans un fichier.                                                                                                   |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | Contrôle la taille minimale des paquets dans un fichier. Hérite de toutes les méthodes de **IWMPacketSize**.                                                 |
| [**IWMProfile**](iwmprofile.md)           | Contrôle les paramètres de base et les objets inclus dans un profil.                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | Récupère l’identificateur global unique (GUID) associé au profil. Hérite de toutes les méthodes de **IWMProfile**.                       |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | Contrôle le partage de bande passante et les informations de hiérarchisation des flux dans un profil. Hérite de toutes les méthodes de **IWMProfile** et **IWMProfile2**. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Objets**](objects.md)
</dt> <dt>

[**Gestionnaire de profils, objet**](profile-manager-object.md)
</dt> <dt>

[**Profils**](profiles.md)
</dt> </dl>

 

 




