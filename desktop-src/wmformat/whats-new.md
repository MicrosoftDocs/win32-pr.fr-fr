---
title: nouveautés (kit de développement logiciel (SDK) Windows Media Format 11)
description: Nouveautés
ms.assetid: af04b99a-4653-4c82-944a-7005cf1181fe
keywords:
- Windows Media Format SDK, nouveautés
- Windows Media Format SDK, fonctionnalités
- Windows Media Format SDK, nouvelles fonctionnalités
- Windows Media Format SDK, API étendues du client
- Windows Kit de développement logiciel (SDK) Media format, mises à jour DRM
- Windows Media Format SDK, mises à jour de codec
- Windows Media Format SDK, images miniatures
- gestion des droits numériques (DRM), nouvelles fonctionnalités
- DRM (gestion des droits numériques), nouvelles fonctionnalités
- images miniatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63d85f00f89f940ab22754d1f6f458430868d7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225772"
---
# <a name="whats-new-windows-media-format-11-sdk"></a>nouveautés (kit de développement logiciel (SDK) Windows Media Format 11)

le kit de développement logiciel (SDK) Windows Media Format 11 introduit de nouvelles fonctionnalités de gestion des droits numériques (DRM). Les modifications suivantes ont été apportées au kit de développement logiciel depuis la version 9,5.

## <a name="windows-media-drm-client-extended-apis"></a>Windows API étendues du client DRM Media

le kit de développement logiciel (SDK) Windows Media Format 11 est fourni avec un nouvel ensemble d’api DRM. Ces API sont implémentées dans leur propre bibliothèque. la plupart des fonctionnalités DRM prises en charge par les objets du kit de développement logiciel (SDK) Windows media Format sont également prises en charge par les api étendues du Client media DRM Windows. La principale différence dans les nouvelles API est qu’elles ne s’appuient pas sur la présence d’un fichier ASF. Au lieu de cela, les nouvelles API traitent le magasin de licences local directement, en utilisant souvent l’ID de clé pour identifier les licences.

pour plus d’informations, consultez la documentation sur les [api étendues du Client Media DRM Windows](windows-media-drm-client-extended-apis.md) .

## <a name="updated-codecs"></a>Codecs mis à jour

le codec du profil avancé Windows Media Video 9 a été mis à jour pour produire un flux binaire compressé conforme à la norme SMPTE VC-1.

le codec Windows Media Audio 10 Professional est également inclus dans cette version du kit de développement logiciel (SDK). Le nouveau codec audio offre une qualité améliorée aux taux de bits inférieurs.

## <a name="thumbnail-right"></a>Miniature droite

Les applications peuvent demander une nouvelle action DRM pour lire à partir de la vidéo afin de créer une image miniature. Cela permet aux applications de créer et d’afficher des images miniatures pour les fichiers vidéo sans ouvrir le fichier pour la lecture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**à propos du kit de développement logiciel (SDK) Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




