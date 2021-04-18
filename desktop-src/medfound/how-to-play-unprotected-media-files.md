---
description: Ce didacticiel montre comment lire des fichiers multimédias à l’aide de l’objet Media session.
ms.assetid: cdd67082-8153-4f48-abc5-278be82ae082
title: Comment lire des fichiers multimédias avec Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163dba2f9f67139ce7477470889e13a54e2c8b5d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104558385"
---
# <a name="how-to-play-media-files-with-media-foundation"></a>Comment lire des fichiers multimédias avec Media Foundation

Ce didacticiel montre comment lire des fichiers multimédias à l’aide de l’objet [Media session](media-session.md) .

## <a name="prerequisites"></a>Prérequis

Avant de lire cette rubrique, vous devez être familiarisé avec les concepts de Media Foundation suivants :

-   [Session multimédia](media-session.md)
-   [Résolveur source](source-resolver.md)
-   [Topologies](topologies.md)
-   [Générateurs d’événements de média](media-event-generators.md)
-   [Descripteurs de présentation](presentation-descriptors.md)

> [!Note]  
> Cette rubrique ne décrit pas comment lire des fichiers protégés par la gestion des droits numériques (DRM). Pour plus d’informations sur DRM dans Microsoft Media Foundation, consultez [Comment lire des fichiers multimédias protégés](how-to-play-protected-media-files.md).

 

## <a name="overview"></a>Vue d’ensemble

Les objets suivants sont utilisés pour lire un fichier multimédia avec la session multimédia :

-   Une *source de média* est un objet qui analyse un fichier multimédia ou une autre source de données multimédias. La source du média crée des objets de *flux* pour chaque flux audio ou vidéo dans le fichier. Les *décodeurs* convertissent les données multimédias encodées en vidéo et audio non compressés.
-   Le programme de *résolution source* crée une source de média à partir d’une URL.
-   Le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR) affiche la vidéo à l’écran.
-   Le [convertisseur audio de streaming](streaming-audio-renderer.md) (SAR) restitue l’audio sur un haut-parleur ou un autre périphérique de sortie audio.
-   Une *topologie* définit le workflow des données de la source du média vers les EVR et SAR.
-   La *session multimédia* contrôle le workflow et envoie des événements d’État à l’application. Le diagramme suivant illustre ce processus.

![Diagramme montrant la lecture à l’aide de la session multimédia](images/session-playback.gif)

Voici un aperçu général des étapes nécessaires pour lire un fichier multimédia à l’aide de la session de média :

1.  Appelez la fonction [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) pour initialiser la plateforme Media Foundation.
2.  Appelez [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) pour créer une nouvelle instance de la session multimédia.
3.  Utilisez le programme de résolution source pour créer une source de média. Pour plus d’informations, consultez [utilisation du programme de résolution source](using-the-source-resolver.md).
4.  Créez une topologie qui connecte la source du média aux EVR et aux SAR. Dans cette étape, l’application crée une topologie *partielle* qui n’inclut pas les décodeurs. Pour plus d’informations, consultez [création de topologies de lecture](creating-playback-topologies.md).
5.  Appelez [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) pour définir la topologie sur la session multimédia.
6.  Utilisez l’interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) pour récupérer les événements de la session multimédia.
7.  Appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour démarrer la lecture. Une fois la lecture démarrée, vous pouvez la suspendre en appelant [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou l’arrêter en appelant [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
8.  Lorsque l’application se ferme, libérer les ressources :

    1.  Appelez [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) pour fermer la session multimédia. Cette méthode est asynchrone. Une fois l’opération terminée, la session multimédia envoie un événement [MESessionClosed](mesessionclosed.md) . Ensuite, il est possible d’effectuer les étapes restantes.
    2.  Appelez [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) pour arrêter la source du média.
    3.  Appelez [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) pour arrêter la session multimédia.
    4.  Appelez [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) pour arrêter la plateforme Media Foundation.

Les sections suivantes présentent un exemple de code complet :

-   [Étape 1 : déclarer la classe CPlayer](step-1--declare-the-cplayer-class.md)
-   [Étape 2 : créer l’objet CPlayer](step-2--create-the-cplayer-object.md)
-   [Étape 3 : ouvrir un fichier multimédia](step-3--open-a-media-file.md)
-   [Étape 4 : créer la session multimédia](step-4--create-the-media-session.md)
-   [Étape 5 : gérer les événements de session multimédia](step-5--handle-media-session-events.md)
-   [Étape 6 : contrôler la lecture](step-6--control-playback.md)
-   [Étape 7 : arrêter la session multimédia](step-7--shut-down-the-media-session.md)
-   [Exemple de lecture de session multimédia](media-session-playback-example.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Lecture audio/vidéo](audio-video-playback.md)
</dt> </dl>

 

 



