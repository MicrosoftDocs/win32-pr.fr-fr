---
title: Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media 9,5
description: Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media 9,5
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Kit de développement logiciel (SDK) Windows Media format, fonctionnalités
- Windows Media Format SDK, nouvelles fonctionnalités
- Windows Media Format SDK, interface pour le traitement propre à l’application
- Windows Media Format SDK, DirectX Video Acceleration (DXVA)
- Windows Media Format SDK, interface IWMPlayerHook
- IWMPlayerHook
- Windows Media Format SDK, versions x64 de Windows
- Windows Media Format SDK, Windows Media Video codec d’image
- Windows Media Format SDK, codecs audio
- Windows Media Format SDK, DRM 10 pour les périphériques réseau
- Windows Media Format SDK, licences DRM
- Windows Media Format SDK, Advanced Profile codec
- Windows Media Format SDK, Sony/Philips Digital Interconnect format (S/PDIF)
- Windows Media Format SDK, formats à faible délai
- Windows Media Format SDK, mode de recherche approximatif
- Kit de développement logiciel (SDK) Windows Media format, gravure de playlist
- Windows Media Format SDK, prise en charge de plusieurs langues
- Windows Media Format SDK, Windows Media Gestionnaire de périphériques SDK
- Windows Media Format SDK, interfaces de codec
- codecs, image Windows Media Video
- gestion des droits numériques (DRM), protocole de transfert sécurisé des périphériques réseau
- DRM (gestion des droits numériques), protocole de transfert sécurisé des périphériques réseau
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- codecs, codec de profil avancé
- Sony/Philips Digital Interconnect format (S/PDIF), transfert ou transmission à l’aide de
- S/PDIF (format d’interconnexion numérique Sony/Philips), transfert ou transmission à l’aide de
- mode de recherche approximatif
- métadonnées, prise en charge de plusieurs langues
- SDK Windows Media Gestionnaire de périphériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101301"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a>Fonctionnalités ajoutées au kit de développement logiciel (SDK) Windows Media 9,5

Le kit de développement logiciel (SDK) Windows Media Format 9,5 a introduit de nouvelles fonctionnalités pour améliorer la sécurité et la flexibilité du contenu. Les modifications suivantes ont été apportées au kit de développement logiciel depuis la version 9 Series.

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a>Nouvelle interface pour le traitement propre à l’application pendant l’accélération vidéo DirectX

Les applications de lecteur qui prennent en charge l’accélération vidéo DirectX peuvent désormais implémenter l’interface [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) pour effectuer un traitement propre à l’application pendant le décodage DirectX va. Le lecteur appelle la méthode de rappel [**IWMPLayerHook ::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) avant de passer des exemples vidéo compressés au processeur vidéo pour le décodage.

> [!Note]  
> Pour utiliser l’interface **IWMPlayerHook** et l’interface [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associée, vous devez avoir installé le numéro de mise à jour 888656 dans le kit de développement logiciel (SDK) du format Windows Media. Vous pouvez télécharger la mise à jour à partir du [site Web Microsoft](https://support.microsoft.com/?id=888656).

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a>Version du kit de développement logiciel (SDK) Windows Media format pour les versions x64 de Windows

Une version x64 du kit de développement logiciel (SDK) du format Windows Media est disponible. Cette documentation s’applique à la fois aux versions 32 bits et à la version x64 du kit de développement logiciel (SDK). Toutefois, la gestion des droits numériques (DRM) n’est pas prise en charge dans le kit de développement logiciel (SDK) Windows Media format x64.

## <a name="new-version-of-the-windows-media-video-image-codec"></a>Nouvelle version du codec d’image Windows Media Video

Le codec Windows Media Video 9 image v2 simplifie les exemples de calculs de géométrie pour le panoramique et le zoom. Le nouveau codec prend également en charge plusieurs transitions complexes entre les images.

## <a name="new-version-of-the-windows-media-audio-codecs"></a>Nouvelle version des codecs de Windows Media Audio

Le kit de développement logiciel (SDK) Windows Media Format 9,5 comprend les codecs audio mis à jour suivants :

-   Windows Media Audio 9,1
-   Windows Media Audio 9,1 professionnel
-   Windows Media Audio 9,1 sans perte

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a>Prise en charge du protocole Windows Media DRM 10 pour les périphériques réseau

Le kit de développement logiciel (SDK) Windows Media Format 9,5 prend en charge le nouveau Windows Media DRM 10 pour le protocole de transfert sécurisé de périphériques réseau. Ce protocole peut être utilisé pour diffuser en continu du contenu chiffré sur un réseau local vers un périphérique de lecture, tel qu’un récepteur vidéo de type Set-Top.

La plupart des procédures utilisées pour implémenter la prise en charge de Windows Media DRM 10 pour les périphériques réseau doivent être effectuées par l’application. Toutefois, vous pouvez utiliser les méthodes du kit de développement logiciel (SDK) Windows Media format pour fournir les fonctionnalités suivantes :

-   Gérer une base de données d’appareils, y compris ceux qui sont activés pour Windows Media DRM 10 pour les périphériques réseau.
-   Validez les appareils pour vous assurer qu’ils sont « presque » suffisants pour le client sur le réseau pour la diffusion en continu sécurisée.
-   Convertit les fichiers protégés par DRM en Windows Media DRM 10 pour les flux de périphériques réseau.
-   Écrire des fichiers à l’aide de données précédemment chiffrées.

## <a name="support-for-new-drm-licenses"></a>Prise en charge de nouvelles licences DRM

Les nouvelles licences créées à l’aide du kit de développement logiciel (SDK) Windows Media Rights Manager utilisent des niveaux de protection de sortie (OPLs) pour spécifier les droits et restrictions relatifs à la reproduction et à la copie de contenu. Le kit de développement logiciel (SDK) Windows Media format prend en charge la lecture des OPLs à partir d’une licence.

## <a name="new-video-codec"></a>Nouveau codec vidéo

Le codec de profil avancé Windows Media Video 9 s’appuie sur la haute qualité du codec Windows Media Video 9 tout en ajoutant la prise en charge de l’encodage entrelacé.

## <a name="spdif-output"></a>Sortie S/PDIF

Le contenu encodé avec l’un des codecs Windows Media Audio Professional peut désormais être transféré ou transmis à l’aide du format S/PDIF de Sony/Philips.

## <a name="low-delay-audio"></a>Audio Low-Delay

Les codecs Windows Media Audio 9,1 et Windows Media Audio 9,1 Professional prennent désormais en charge plusieurs formats à faible délai. Ces formats produisent des flux audio qui peuvent être démarrés plus rapidement, ce qui réduit la latence dans les scénarios de commutation de flux. La latence globale des diffusions en direct est également améliorée en utilisant des formats à faible retard.

## <a name="approximate-seeking-mode"></a>Mode de recherche approximatif

Vous pouvez maintenant rechercher une heure approximative dans un fichier ASF avec le lecteur. Ce mode améliore les performances lorsque vous effectuez une recherche imprécise, par exemple quand un utilisateur clique sur la barre de recherche dans le lecteur Windows Media. La recherche approximative retourne l’échantillon de support pour le Cleanpoint précédent au lieu de reconstruire l’exemple pour l’heure précise demandée.

## <a name="playlist-burning"></a>Gravure de playlist

Windows Media DRM 10 prend en charge les droits de copie de fichiers audio dans un CD Red Book dans le cadre d’une sélection. Le kit de développement logiciel (SDK) Windows Media Format fournit des méthodes pour vérifier si les fichiers d’une sélection sont autorisés à être copiés.

## <a name="improved-multiple-language-support-for-metadata"></a>Prise en charge améliorée des Multiple-Language pour les métadonnées

Dans le kit de développement logiciel (SDK) Windows Media Format 9 Series, toutes les métadonnées ajoutées à un fichier ont été affectées à une liste de langues ayant reçu l’identificateur de langue de la langue par défaut. Cela provoquait des problèmes lorsque les serveurs de distribution de contenu de différents paramètres régionaux ajoutaient des métadonnées, car les utilisateurs des paramètres régionaux du serveur de distribution voient uniquement les attributs ajoutés pour leur langue. Le kit de développement logiciel (SDK) Windows Media Format 9,5 résout ce problème en ne créant pas de liste de langues tant qu’il n’y a pas d’attributs de deux langages présents dans le fichier. À ce stade, toutes les métadonnées sont associées aux paramètres régionaux de la deuxième langue, qui devient alors la valeur par défaut. De cette façon, un serveur de distribution de contenu peut conserver toutes les métadonnées d’origine d’un fichier, telles que le titre et l’auteur, tout en ajoutant des attributs pertinents pour leurs paramètres régionaux.

## <a name="windows-media-device-manager-sdk-included-in-installation"></a>Kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques inclus dans l’installation

Le package d’installation du kit de développement logiciel (SDK) Windows Media Format 9,5 installe le kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques. La documentation du kit de développement logiciel (SDK) Windows Media Gestionnaire de périphériques se trouve dans le dossier C : \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (votre dossier sera différent si vous n’installez pas le kit de développement logiciel (SDK) Windows Media format dans le dossier par défaut).

## <a name="codec-interface-documentation"></a>Documentation sur l’interface de codec

Cette documentation contient des informations sur l’utilisation du Windows Media Audio et des codecs vidéo en dehors du kit de développement logiciel (SDK) de format Windows Media. Cette documentation a été publiée à l’origine dans le cadre d’un téléchargement à partir du Microsoft Developer Network. Les exemples d’applications qui illustrent l’utilisation directe du codec DMOs sont inclus dans l’installation du kit de développement logiciel (SDK) du format Windows Media avec les en-têtes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du kit de développement logiciel (SDK) Windows Media format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




