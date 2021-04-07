---
title: Fonctionnalités de Rights Management numérique
description: Fonctionnalités de Rights Management numérique
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités DRM
- gestion des droits numériques (DRM), fonctionnalités
- DRM (gestion des droits numériques), fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728012"
---
# <a name="digital-rights-management-features"></a>Fonctionnalités de Rights Management numérique

\[La fonctionnalité Windows Media DRM est déconseillée et ne doit pas être utilisée. Utilisez plutôt [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

La gestion des droits numériques (DRM) est une technologie que les propriétaires de contenu peuvent utiliser pour protéger des fichiers multimédias numériques en les chiffrant à l’aide d’une clé (un élément de données qui verrouille et déverrouille le contenu). Pour lire un fichier ASF protégé, un consommateur doit obtenir une licence distincte contenant la clé. Chaque licence contient également des droits, déterminés par le propriétaire du contenu ou l’émetteur de la licence, qui spécifient comment le consommateur peut utiliser le fichier. Grâce à la technologie DRM, les propriétaires de contenu peuvent diffuser des chansons, des vidéos et d’autres fichiers multimédias numériques sur Internet dans un format de fichier protégé et contrôler l’utilisation de leur contenu numérique. La technologie Microsoft DRM est également prise en charge par Windows Media Rights Manager, Windows Media Encoder et Windows Media Player. Pour plus d’informations générales sur la technologie DRM de Microsoft, consultez le [site Web Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

Les sections suivantes décrivent les principales fonctionnalités DRM du kit de développement logiciel (SDK) de format Windows Media.



| Section                                                                                            | Description                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Notions de base de DRM](drm-basics.md)                                                                       | Fournit une brève vue d’ensemble des fonctionnalités DRM fournies par le kit de développement logiciel (SDK) de format Windows Media.                                         |
| [Versions DRM](drm-versions.md)                                                                   | Décrit les principales différences entre les versions de la protection DRM disponibles pour les applications.                                     |
| [DRM en direct](live-drm.md)                                                                           | Décrit les scénarios rendus possibles par la protection DRM « à la volée ».                                                                |
| [Individualisation DRM](drm-individualization.md)                                                 | Décrit la mise à niveau de sécurité de l’application que les propriétaires de contenu DRM ou les émetteurs de licence peuvent exiger.                                   |
| [Sauvegarde et restauration de licences DRM](backing-up-and-restoring-of-drm-licenses.md)           | Décrit les avantages et les inconvénients de l’autorisation des utilisateurs à sauvegarder et restaurer leurs licences de contenu.                                       |
| [Affichage des attributs DRM dans l’éditeur de métadonnées](viewing-drm-attributes-in-the-metadata-editor.md) | Décrit les fonctionnalités de cet objet d’assistance DRM et les scénarios qu’il a été conçu pour prendre en charge.                                   |
| [Niveaux de protection de sortie](output-protection-levels.md)                                           | Décrit comment les niveaux de protection de sortie rendent les licences DRM version 10 plus flexibles.                                                   |
| [Révocation de licence](license-revocation.md)                                                       | Décrit la révocation de licence.                                                                                                        |
| [Windows Media DRM 10 pour les périphériques réseau](windows-media-drm-10-for-network-devices.md)           | Présente Windows Media DRM 10 pour les périphériques réseau et son implémentation dans ce kit de développement logiciel (SDK).                                              |
| [Chemin d’accès audio sécurisé Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Décrit l’architecture du chemin d’accès audio sécurisé de Microsoft, qui offre le degré de protection le plus élevé pour le contenu audio protégé. |
| [Gravure de playlist](playlist-burning.md)                                                           | Décrit la fonctionnalité de gravure de liste de réécoutes DRM et la façon dont elle est prise en charge dans le kit de développement logiciel (SDK) Windows Media format.                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> <dt>

[**Fonctionnalités**](features.md)
</dt> </dl>

 

 