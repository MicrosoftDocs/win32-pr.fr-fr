---
description: La liste suivante contient les fonctionnalités prises en charge par le MSP TAPI.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Fonctionnalités prises en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201462"
---
# <a name="features-supported"></a>Fonctionnalités prises en charge

La liste suivante contient les fonctionnalités prises en charge par le MSP TAPI.

-   Implémente un MSP qui gère une seule adresse par instance du MSP. Plusieurs adresses similaires sont gérées en instanciant le MSP plusieurs fois. Cela simplifie grandement l’implémentation du MSP et des classes de base.
-   Implémente toutes les interfaces MSPI, y compris [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)et [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).
-   Implémente des terminaux statiques prêts à l’emploi pour l’audio et la vidéo.
-   Implémente les classes de base de terminal génériques. Ces classes de base de terminal sont utilisées par les implémentations de terminal statique mentionnées ci-dessus et les implémentations de terminaux dynamiques qui se trouvent dans Termmgr.dll. Le MSP peut également les utiliser pour implémenter des terminaux supplémentaires.
-   Utilise le gestionnaire de terminal pour gérer les terminaux dynamiques. Crée des terminaux dynamiques sur un thread de travail avec une pompe de messages (pour empêcher les applications de console de traiter les messages de fenêtre pour les terminaux de rendu vidéo et simplifier les problèmes de synchronisation).
-   Prend en charge les appels qui utilisent un graphique de filtre par flux.
-   Implémente la gestion des événements de graphique.
-   Utilise les API de regroupement de threads, conjointement avec un thread de travail qui lui est propre, pour gérer les événements.
-   Utilise les API de suivi de Windows 2000 (développée à l’origine pour le projet de routage) ainsi que la logique supplémentaire pour fournir un mécanisme de journalisation générique et flexible qui peut simultanément se connecter à n’importe quelle combinaison des éléments suivants : un débogueur en mode utilisateur ou en mode noyau ; fenêtre de console distincte avec des messages de journal séparés par un composant ; un fichier journal.
-   Exécute un thread libre.

 

 
