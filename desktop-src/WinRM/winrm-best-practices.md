---
title: Bonnes pratiques WinRM
description: Cette rubrique décrit quelques-unes des meilleures pratiques pour l’utilisation des différentes fonctionnalités de l’API WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941043"
---
# <a name="winrm-best-practices"></a>Bonnes pratiques WinRM

Cette rubrique décrit quelques-unes des meilleures pratiques pour l’utilisation des différentes fonctionnalités de l’API WinRM.

## <a name="quotas"></a>Quotas

Lorsqu’un quota est atteint, le service WinRM retourne une erreur au client. Par conséquent, la logique du client doit retenter explicitement l’opération en fonction de l’erreur retournée.

## <a name="event-subscriptions"></a>Abonnements à des événements

Lorsque vous utilisez des abonnements déclenchés par le collecteur, limitez le nombre d’ordinateurs distants à 500 et isolez le service [collecteur d’événements Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) dans un processus hôte distinct.

Une erreur de connexion contiendra un thread jusqu’à ce qu’il expire. Un grand nombre d’erreurs de connexion simultanées peuvent entraîner l’épuisement du pool de threads et rendre le serveur sans réponse.

 

 