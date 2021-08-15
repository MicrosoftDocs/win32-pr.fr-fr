---
description: API Sensor
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: API Sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5c3fd3cbdbf2aac9a161a6cb8bc150d2828c2d48a346b94843878cda49a6a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889670"
---
# <a name="sensor-api"></a>API Sensor

## <a name="purpose"></a>Objectif

Windows 7 offre une prise en charge native des capteurs, qui sont des appareils qui peuvent mesurer des phénomènes physiques tels que la température ou l’emplacement. Cette documentation décrit l’API de capteur, qui permet aux applications d’obtenir et d’utiliser les données des capteurs de manière standardisée.

En tant qu’humains, nous nous appuyons sur nos sens pour nous fournir des informations sur le monde. Lorsque nous créons des machines pour effectuer une partie de notre travail, nous ajoutons des mécanismes de capteur afin que les ordinateurs puissent répondre de manière appropriée aux conditions fluctuantes.

Par exemple, les moteurs automobiles utilisent généralement divers capteurs. Ces capteurs sont surveillés par un ordinateur intégré qui ajuste continuellement les paramètres, tels que le minutage du moteur, afin d’optimiser la puissance et l’efficacité. Une télévision peut utiliser un capteur de lumière ambiante pour ajuster la luminosité de l’image afin de correspondre aux conditions de la salle de modification. Même un simple bouton Doorbell agit comme un capteur rudimentaire pour détecter une présence humaine à la porte.

Alors que le Doorbell purement mécanique répond à son objectif, les informations fournies par les capteurs complexes deviennent beaucoup plus puissantes lorsqu’il est associé à un logiciel. Les capteurs modernes peuvent fournir beaucoup de données très rapidement et dans différents formats, de sorte que les logiciels fournissent un mécanisme naturel pour la prise en main des données de capteur.

Aujourd’hui, les développeurs de logiciels peuvent écrire des programmes qui utilisent des capteurs, mais un manque de normalisation rend la programmation des capteurs une tâche ardue. Une fois qu’un programme basé sur un capteur est terminé, il est généralement toujours dépendant d’un type de matériel particulier. l’utilisation d’une ou de plusieurs solutions verticales pour permettre le déploiement d’un système basé sur des logiciels a limité l’intégration des capteurs au matériel informatique et, jusqu’à présent, les ordinateurs Windows ne sont pas une exception.

Windows 7 inclut la prise en charge native des capteurs, développée par une nouvelle plateforme de développement pour l’utilisation de capteurs, y compris les capteurs d’emplacement, tels que les périphériques GPS. le capteur de Windows et la plateforme d’emplacement offrent aux fabricants de périphériques un moyen standard d’exposer des appareils de capteur à des développeurs de logiciels et à des consommateurs, tout en offrant aux développeurs une interface de programmation d’applications (API) standardisée pour l’utilisation des capteurs et des données de capteur.

Les capteurs sont des appareils ou des mécanismes qui peuvent mesurer des phénomènes physiques, fournir des données descriptives ou fournir des informations sur l’état d’un objet ou d’un environnement physique. Les ordinateurs peuvent utiliser des capteurs intégrés, des capteurs connectés via des connexions câblées ou sans fil, ou des capteurs qui fournissent des données via un réseau ou Internet.

L’API de capteur offre un moyen standard d’accéder par programme aux données fournies par les capteurs. L’API de capteur standard :

-   Catégories, types et propriétés de capteur.
-   Formats de données pour les types de capteurs standard.
-   Interfaces COM pour l’utilisation de capteurs et de regroupements de capteurs.
-   Mécanismes d’événements pour la réception asynchrone des données de capteur.

L’API de capteur vous permet également de définir des catégories, des types, des propriétés, des formats de données et des événements personnalisés.

## <a name="developer-audience"></a>Développeurs concernés

L’API de capteur fournit ses fonctionnalités via un ensemble d’interfaces COM. Cette documentation suppose que vous avez une connaissance pratique de la programmation à l’aide du langage de programmation C++, et que vous avez une compréhension élémentaire de l’utilisation des objets et des interfaces COM. Par souci de concision, de nombreux exemples de code dans cette documentation (ainsi que dans les exemples de code) utilisent des objets Active Template Library (ATL) pour implémenter les fonctionnalités COM.

## <a name="in-this-section"></a>Dans cette section

-   [Prise en main](getting-started.md)
-   [À propos de l’API de capteur](about-the-sensor-api.md)
-   [Guide de programmation de l’API de capteur](sensor-api-programming-guide.md)
-   [Référence de programmation de l’API de capteur](sensor-api-programming-reference.md)

 

 



