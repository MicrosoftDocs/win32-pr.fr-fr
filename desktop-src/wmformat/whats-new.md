---
title: Nouveautés (kit de développement logiciel (SDK) Windows Media format 11)
description: What's New
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, nouveautés
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- Windows Media Format SDK, nouvelles fonctionnalités
- Windows Media Format SDK, API étendues du client
- Windows Media Format SDK, mises à jour DRM
- Windows Media Format SDK, mises à jour de codec
- Windows Media Format SDK, images miniatures
- gestion des droits numériques (DRM), nouvelles fonctionnalités
- DRM (gestion des droits numériques), nouvelles fonctionnalités
- images miniatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739501"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>Nouveautés (kit de développement logiciel (SDK) Windows Media format 11)

Le kit de développement logiciel (SDK) Windows Media format 11 introduit de nouvelles fonctionnalités de gestion des droits numériques (DRM). Les modifications suivantes ont été apportées au kit de développement logiciel depuis la version 9,5.

## <a name="windows-media-drm-client-extended-apis"></a>API étendues du client Windows Media DRM

Le kit de développement logiciel (SDK) Windows Media format 11 est fourni avec un nouvel ensemble d’API DRM. Ces API sont implémentées dans leur propre bibliothèque. La plupart des fonctionnalités DRM prises en charge par les objets du kit de développement logiciel (SDK) Windows Media format sont également prises en charge par les API étendues du client Windows Media DRM. La principale différence dans les nouvelles API est qu’elles ne s’appuient pas sur la présence d’un fichier ASF. Au lieu de cela, les nouvelles API traitent le magasin de licences local directement, en utilisant souvent l’ID de clé pour identifier les licences.

Pour plus d’informations, consultez la documentation sur les [API étendues du client Windows Media DRM](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Codecs mis à jour

Le codec du profil avancé Windows Media Video 9 a été mis à jour pour produire un flux binaire compressé conforme à la norme SMPTE VC-1.

Le codec Windows Media Audio 10 Professional est également inclus dans cette version du kit de développement logiciel (SDK). Le nouveau codec audio offre une qualité améliorée aux taux de bits inférieurs.

## <a name="thumbnail-right"></a>Miniature droite

Les applications peuvent demander une nouvelle action DRM pour lire à partir de la vidéo afin de créer une image miniature. Cela permet aux applications de créer et d’afficher des images miniatures pour les fichiers vidéo sans ouvrir le fichier pour la lecture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du kit de développement logiciel (SDK) Windows Media format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




