---
description: Introduction à la programmation d’applications DirectShow
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Introduction à la programmation d’applications DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6218a346a7eb9711259c025aef09133ef2e58f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392556"
---
# <a name="introduction-to-directshow-application-programming"></a>Introduction à la programmation d’applications DirectShow

Cet article présente la terminologie et les concepts de base utilisés dans DirectShow. Après avoir lu cette section, vous serez prêt à écrire votre première application DirectShow.

**Filtres et graphiques de filtre**

Le bloc de construction de DirectShow est un composant logiciel appelé « *filtre*». Un filtre est un composant logiciel qui effectue une opération sur un flux multimédia. Par exemple, les filtres DirectShow peuvent

-   lire les fichiers
-   obtenir de la vidéo à partir d’un appareil de capture vidéo
-   décoder divers formats de flux, tels que MPEG-1 Video
-   transmettre des données à la carte graphique ou audio

Les filtres reçoivent une entrée et produisent une sortie. Par exemple, si un filtre décode une vidéo MPEG-1, l’entrée est le flux codé en MPEG et la sortie est une série de trames vidéo non compressées.

Dans DirectShow, une application effectue une tâche en connectant des chaînes de filtres ensemble, de sorte que la sortie d’un filtre devient l’entrée d’une autre. Un ensemble de filtres connectés est appelé un *graphique de filtre*. Par exemple, le diagramme suivant montre un graphique de filtre pour la diffusion d’un fichier AVI.

![filtrer le graphique pour lire un fichier AVI](images/avi-filter-graph.png)

Le filtre de source de fichier lit le fichier AVI à partir du disque dur. Le filtre de séparateur AVI analyse le fichier en deux flux, un flux vidéo compressé et un flux audio. Le filtre de décompresseur AVI décode les images vidéo. Le filtre de convertisseur vidéo dessine les frames à l’écran à l’aide de DirectDraw ou GDI. Le filtre de périphérique DirectSound par défaut lit le flux audio, à l’aide de DirectSound.

L’application n’a pas à gérer l’ensemble de ce Workflow. Au lieu de cela, les filtres sont contrôlés par un composant de niveau supérieur appelé gestionnaire de graphes de filtres. L’application effectue des appels d’API de haut niveau tels que « exécuter » (pour déplacer des données par le biais du graphique) ou « arrêter » (pour arrêter le workflow de données). Si vous avez besoin de davantage de contrôle sur les opérations de flux, vous pouvez accéder aux filtres directement par le biais des interfaces COM. Le gestionnaire de graphes de filtre transmet également les notifications d’événements à l’application.

Le gestionnaire de graphes de filtre a également une autre fonction : il fournit des méthodes permettant à l’application de générer le graphique de filtre, en connectant les filtres ensemble. (DirectShow fournit également divers objets d’assistance qui simplifient ce processus. Celles-ci sont décrites en détail dans la documentation.)

**Écriture d’une application DirectShow**

En général, il existe trois tâches que toute application DirectShow doit effectuer. Ceux-ci sont illustrés dans le diagramme suivant.

![application DirectShow classique](images/fgm.png)

1.  L’application crée une instance du gestionnaire de graphes de filtre.
2.  L’application utilise le gestionnaire de graphe de filtre pour générer un graphique de filtre. L’ensemble exact de filtres dans le graphique dépend de l’application.
3.  L’application utilise le gestionnaire de graphe de filtre pour contrôler le graphique de filtre et diffuser les données en continu via les filtres. Tout au long de ce processus, l’application répond également aux événements du gestionnaire de graphes de filtre.

Une fois le traitement terminé, l’application libère le gestionnaire de graphique de filtre et tous les filtres.

DirectShow est basé sur COM ; le gestionnaire de graphique de filtre et les filtres sont tous des objets COM. Vous devez avoir une compréhension générale de la programmation du client COM avant de commencer à programmer DirectShow. De nombreux ouvrages sur la programmation COM sont disponibles.

Pour commencer à utiliser DirectShow, lisez l’article [Comment lire un fichier](how-to-play-a-file.md), qui présente une application console simple pour lire un fichier vidéo. La section [relative à DirectShow](about-directshow.md) explique plus en détail l’architecture DirectShow, tandis que la section [utilisation de DirectShow](using-directshow.md) examine les principaux scénarios pris en charge par DirectShow, tels que la capture, la modification vidéo, la lecture de DVD et la télévision.

 

 



