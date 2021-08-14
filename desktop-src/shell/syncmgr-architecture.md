---
description: Le gestionnaire de synchronisation comprend des composants de l’interface utilisateur, tels que les boîtes de dialogue à onglets du service SyncMgr, des boîtes de dialogue d’erreur et des boîtes de dialogue de progression.
title: Architecture du gestionnaire de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 584329a06ee9df80558d9961b734b62a57d5ebccd83f200690812fa99132b06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451865"
---
# <a name="synchronization-manager-architecture"></a>Architecture du gestionnaire de synchronisation

Le gestionnaire de synchronisation comprend des composants de l’interface utilisateur, tels que les boîtes de dialogue à onglets du service SyncMgr, des boîtes de dialogue d’erreur et des boîtes de dialogue de progression. Avec les composants de l’interface utilisateur, l’utilisateur final peut planifier des applications pour la synchronisation et configurer la synchronisation automatique pour qu’elle se produise conjointement avec les événements système spécifiés. Par exemple, le SyncMgr peut être appelé lors de l’ouverture de session de l’utilisateur ou de l’arrêt du système. L’utilisateur peut également appeler une synchronisation manuelle.

L’utilisateur sélectionne une application et spécifie les éléments de l’application à synchroniser et définit un événement déclencheur. Par exemple, dans une application de messagerie, la boîte de réception, la boîte d’envoi ou un autre dossier contenant des messages peut être un élément distinct pour l’application.

SyncMgr comprend également une interface de programmation qui permet aux applications de s’inscrire pour utiliser les fonctionnalités de synchronisation, de traiter les erreurs et de recevoir des informations de progression et des notifications pendant le processus de synchronisation.

 

 



