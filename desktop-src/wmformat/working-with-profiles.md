---
title: Utilisation des profils
description: Utilisation des profils
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows Media Format SDK, profils
- Windows Media Format SDK, interface IWMCodecInfo3
- profils, à propos de
- profils, Windows Media Format SDK
- profils, IWMCodecInfo3
- IWMCodecInfo3, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664bbafd6c628588aa3b45b0a62a216db7bd7749
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195872"
---
# <a name="working-with-profiles"></a>Utilisation des profils

Cette section décrit comment concevoir, créer et modifier des profils. Chaque profil décrit les flux qui composent un fichier et leurs relations entre eux. Un objet de profil contient des informations de configuration de flux pour chaque flux, des informations d’exclusion mutuelle pour les flux qui ne peuvent pas être remis simultanément, des informations de partage de bande passante et des informations de hiérarchisation de flux.

L’objectif principal des profils est de fournir des informations de configuration de flux à l’objet Writer. Le writer utilise les informations d’un profil pour coordonner avec les codecs le processus de compression des entrées. Quand vous configurez un flux de média compressé, vous spécifiez le codec utilisé pour compresser les données et les paramètres utilisés par le codec. Vous pouvez également créer des profils pour les flux non compressés. Plusieurs types de flux non compressés sont pris en charge. Même s’ils ne nécessitent pas de codec, ces types ont leurs propres exigences en matière de configuration de flux. pour plus d’informations, consultez [configuration de Flux](configuring-streams.md) et utilisation de [Flux Audio et vidéo non compressés](using-uncompressed-audio-and-video-streams.md).

les informations de configuration de flux pour un flux à l’aide de l’un des codecs de média Windows doivent être obtenues à partir du codec à l’aide des méthodes de l’interface [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) . La procédure d’utilisation des formats de flux est différente pour les codecs vidéo que pour les codecs audio, mais dans les deux cas, vous devez commencer par obtenir le format à partir du codec. vous ne devez jamais essayer de configurer manuellement un flux à l’aide de l’un des codecs de média Windows, car de petites erreurs dans le profil peuvent avoir un effet profond sur le fichier ASF.

Les étapes de base pour créer et/ou modifier des profils sont les suivantes :

1.  Créez un profil vide ou chargez un profil existant à modifier.
2.  Configurez chacun des flux, si nécessaire, en fonction des données de profil prises en charge récupérées à partir du codec qui sera utilisé pour encoder le flux.
3.  Configurez l’exclusion mutuelle, si nécessaire.
4.  Configurez le partage de bande passante, si nécessaire.
5.  Définissez la priorité des flux dans le fichier, si nécessaire.

Les sections suivantes expliquent le processus de création et de modification des profils.



| Section                                                        | Description                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Conception de profils](designing-profiles.md)                   | Décrit comment concevoir un profil.                                                                 |
| [Création de profils](creating-profiles.md)                     | Décrit comment créer un profil vide.                                                          |
| [Configuration de Flux](configuring-streams.md)                 | Décrit comment configurer des flux et les inclure dans un profil.                                  |
| [Utilisation de l’exclusion mutuelle](using-mutual-exclusion.md)           | Décrit comment créer des objets d’exclusion mutuelle et les inclure dans un profil.                    |
| [Utilisation du partage de bande passante](using-bandwidth-sharing.md)         | Décrit comment utiliser le partage de bande passante dans un profil.                                               |
| [Utilisation de la hiérarchisation des flux](using-stream-prioritization.md) | Décrit comment utiliser la hiérarchisation des flux dans un profil.                                           |
| [Enregistrement des profils](saving-profiles.md)                         | Décrit comment enregistrer vos profils personnalisés dans un fichier.                                              |
| [Utilisation des profils système](using-system-profiles.md)             | Décrit comment utiliser des profils système pour gagner du temps et des efforts dans la création de profils.           |
| [Gestion de la taille des paquets](managing-packet-size.md)               | Explique comment contrôler la taille des paquets dans les flux de données des fichiers créés à l’aide de votre profil. |



 

**Remarque** les utilisateurs des versions précédentes du kit de développement logiciel (SDK) du Format de média Windows peuvent être habitués à utiliser des profils système sans modification pour créer leurs fichiers. le kit de développement logiciel (SDK) Windows media Format 9 ou version ultérieure n’inclut aucun nouveau profil système utilisant les codecs Windows Media 9 ou ultérieur. Cela est dû au nombre grandissant de profils qui seraient nécessaires pour couvrir les diverses fonctionnalités désormais proposées par les codecs. Vous pouvez toujours utiliser les profils système de la version 8 comme point de départ pour vos profils. Pour plus d’informations, consultez [utilisation des profils système](using-system-profiles.md). Pour plus d’informations sur le nouveau mécanisme de ciblage des profils sur des appareils de remise spécifiques, consultez [utilisation des modèles de conformité des appareils](working-with-device-conformance-templates.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 




