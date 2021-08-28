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
ms.openlocfilehash: dc780ec299c3249006085d348d983f8dab5b76a462c991a2d3665fed7d18f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733799"
---
# <a name="winrm-best-practices"></a>Bonnes pratiques WinRM

Cette rubrique décrit quelques-unes des meilleures pratiques pour l’utilisation des différentes fonctionnalités de l’API WinRM.

## <a name="quotas"></a>Quotas

Lorsqu’un quota est atteint, le service WinRM retourne une erreur au client. Par conséquent, la logique du client doit retenter explicitement l’opération en fonction de l’erreur retournée.

## <a name="event-subscriptions"></a>Abonnements à des événements

lorsque vous utilisez des abonnements déclenchés par le collecteur, limitez le nombre d’ordinateurs distants à 500 et isolez Windows le service wecsvc [Event Collector](/windows/desktop/WEC/windows-event-collector) () dans un processus hôte distinct.

Une erreur de connexion contiendra un thread jusqu’à ce qu’il expire. Un grand nombre d’erreurs de connexion simultanées peuvent entraîner l’épuisement du pool de threads et rendre le serveur sans réponse.

 

 