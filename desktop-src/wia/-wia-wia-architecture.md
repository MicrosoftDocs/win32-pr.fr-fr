---
description: WIA est implémenté en tant que serveur hors processus COM (Component Object Model) pour garantir le bon fonctionnement des applications clientes.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Architecture WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a6bb88fba5a79f2915500786bbfcf8d531bfe0170ec6c6841f419425ee296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813262"
---
# <a name="wia-architecture"></a>Architecture WIA

WIA est implémenté en tant que serveur hors processus COM (Component Object Model) pour garantir le bon fonctionnement des applications clientes. contrairement à la plupart des applications serveur de processus, Windows Acquisition d’images (WIA) évite les pénalités de performances lors du transfert de données d’image en fournissant son propre mécanisme de transfert de données, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer). Cette interface haute performance utilise une fenêtre de mémoire partagée pour transférer des données vers le client.

WIA comporte trois composants principaux : un Gestionnaire de périphériques, une bibliothèque du service de minipilote et un minipilote d’appareil.

-   Le Gestionnaire de périphériques énumère les périphériques d’acquisition d’images, récupère les propriétés de l’appareil, configure les événements pour les appareils et crée des objets d’appareil.
-   La bibliothèque du service de minipilote implémente tous les services indépendants de l’appareil.
-   Le minipilote d’appareil mappe les propriétés et les commandes WIA à l’appareil spécifique.

Le diagramme suivant illustre l’architecture WIA :

![architecture WIA](images/wiarch.gif)

 

 



