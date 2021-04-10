---
description: À propos de la session multimédia
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: À propos de la session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953342"
---
# <a name="about-the-media-session"></a>À propos de la session multimédia

La session multimédia expose l’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . Il existe deux façons de créer la session multimédia, selon que votre application prendra en charge le contenu protégé :

-   Si votre application ne prend pas en charge le contenu protégé, vous pouvez créer la session multimédia en appelant [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession). Cette fonction crée la session multimédia à l’intérieur du processus d’application.
-   Pour prendre en charge le contenu protégé, créez la session multimédia en appelant [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Cette fonction crée la session multimédia à l’intérieur du processus PMP (Protected Media Path). L’application reçoit un pointeur vers un objet proxy qui marshale les appels de méthode à travers la limite de processus. Notez que la session de média PMP peut être utilisée pour lire du contenu clair, ainsi que du contenu protégé.

Toute application qui utilise la session multimédia suit les étapes générales suivantes :

1.  Créer une topologie.
2.  Met en file d’attente la topologie sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).
3.  Contrôlez le workflow de données en appelant [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
4.  Avant de quitter l’application, appelez [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) pour fermer la session multimédia.
5.  Arrêtez toutes les sources multimédias créées par l’application, en appelant [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
6.  Arrêtez la session multimédia en appelant [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).

Lors de l’utilisation de la session multimédia, l’application ne doit pas démarrer, suspendre ou arrêter directement la source du média. Toutes les modifications d’État doivent être lancées en appelant les méthodes [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) . Les changements d’État dans la source du média sont gérés par la session multimédia.

De nombreux autres détails dépendent des fonctionnalités spécifiques de votre application.

## <a name="protected-content"></a>Contenu protégé

Pour lire du contenu protégé, vous devez créer la session multimédia à l’intérieur du chemin d’accès de média protégé (PMP), en appelant [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession). Cette fonction crée une instance de la session multimédia à l’intérieur de l’PMP et retourne un pointeur vers un objet proxy qui marshale les interfaces à travers la limite de processus.

Dans la plupart des aspects, l’utilisation de la session multimédia à l’intérieur du PMP est transparente pour l’application. Toutefois, l’application peut avoir besoin d’appeler certaines actions qui permettent à l’utilisateur de lire le contenu. Par exemple, l’utilisateur peut avoir besoin d’obtenir une licence DRM. Media Foundation définit un mécanisme générique pour ces actions à l’aide de l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .

Pour plus d'informations, voir les rubriques suivantes :

-   [Chemin du média protégé](protected-media-path.md)
-   [Comment lire des fichiers multimédias protégés](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Horloge de présentation

La session multimédia gère tous les aspects de l’horloge de présentation :

-   Création de l’horloge de présentation.

-   Sélection de la source de temps.

-   Notification des récepteurs de médias sur l’horloge

-   Le démarrage, l’arrêt et la suspension de l’horloge, si nécessaire.

-   Arrêt de l’horloge.

Pour obtenir un pointeur vers l’horloge de présentation, appelez [**IMFMediaSession :: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) sur la session multimédia. L’horloge de présentation ne retourne pas d’heure valide tant que la session multimédia n’envoie pas l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec l' \_ \_ indicateur prêt TOPOSTATUS Ready. Jusqu’à présent, **GetClock** retourne MF \_ E \_ Clock \_ no \_ Time \_ source.

Une application qui utilise la session de média ne doit jamais démarrer, arrêter ou suspendre l’horloge de la présentation ; modifier la fréquence d’horloge ; ou arrêtez l’horloge.

Lorsque l’application appelle [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la session multimédia démarre l’horloge de la présentation avec une heure de début égale à la position de départ spécifiée dans la méthode **Start** . Pour plus d’informations sur la session multimédia, consultez [session multimédia](media-session.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> </dl>

 

 



