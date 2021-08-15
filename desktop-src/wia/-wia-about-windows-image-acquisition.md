---
description: l’interface WIA (Windows Image Acquisition) est à la fois une API et une interface de pilote de périphérique (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: à propos de l’Acquisition d’images Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73662083e568a109760a052994bfcbebdfcbe53f858e50a89728a01bba344d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451299"
---
# <a name="about-windows-image-acquisition"></a>à propos de l’Acquisition d’images Windows

l’interface WIA (Windows Image Acquisition) est à la fois une API et une interface de pilote de périphérique (DDI). L’API WIA est conçue pour permettre aux applications d’effectuer les opérations suivantes :

-   S’exécute dans un environnement robuste et stable.
-   Réduire les problèmes d’interopérabilité.
-   Énumérer les appareils d’acquisition d’images disponibles.
-   Créer des connexions à plusieurs appareils simultanément.
-   Interrogez les propriétés des appareils de manière standard et extensible.
-   Acquérir des données d’appareil à l’aide de mécanismes de transfert standard et hautes performances.
-   Conserver les propriétés de l’image entre les transferts de données.
-   Être informé d’un grand nombre d’événements d’appareil.

Le WIADDI est conçu pour réduire la quantité de code qu’un fournisseur de matériel doit écrire, tout en conservant la flexibilité nécessaire pour concevoir des solutions individuelles. Pour ce faire, procédez comme suit :

-   Fournir une bibliothèque de services d’appareils standard qui effectue la plupart des opérations de pilote.
-   Promouvoir les normes de communication des appareils de l’industrie pour qu’un pilote WIA prenne en charge la plupart des appareils WIA. Par exemple, le protocole PTP (Image Transfer Protocol).
-   Autoriser le pilote de périphérique à prendre en charge des interfaces personnalisées, sans exiger qu’il utilise la bibliothèque de service d’appareil standard. Toutefois, les pilotes doivent toujours implémenter les interfaces WIA standard.

Cette section présente une vue d’ensemble de l’interface WIA dans les domaines suivants :

-   [Architecture WIA](-wia-wia-architecture.md)
-   [Compatibilité STI](-wia-sti-compatibility.md)
-   [Compatibilité avec TWAIN](-wia-twain-compatibility.md)
-   [Gestionnaire de périphériques WIA](-wia-wia-device-manager.md)
-   [Bibliothèque du service WIA minipilote](-wia-wia-minidriver-service-library.md)
-   [Minipilote WIA](-wia-wia-minidriver.md)

 

 



