---
title: Récupération et redémarrage d’application
description: Écrire des programmes d’installation personnalisés pour redémarrer automatiquement une application qui a été arrêtée pour terminer une mise à jour. Enregistrez les données et configurez la récupération de l’application avant de quitter les programmes.
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- fiabilité
- fiabilité des logiciels
- récupération d’application
- redémarrage de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840686"
---
# <a name="application-recovery-and-restart"></a>Récupération et redémarrage d’application

## <a name="purpose"></a>Objectif

Une application peut utiliser la récupération et le redémarrage de l’application (ARR) pour enregistrer les données et les informations d’État avant la fermeture de l’application en raison d’une exception non gérée ou lorsque l’application cesse de répondre. L’application est également redémarrée, si nécessaire.

Une application peut également être redémarrée si un programme d’installation met à jour un composant de l’application, ou si l’ordinateur doit redémarrer suite à une mise à jour. Notez que pour prendre en charge le redémarrage automatique de l’application après qu’un programme d’installation a mis à jour une application, l’application et le programme d’installation doivent être correctement créés. Pour plus d’informations, consultez [inscription au redémarrage de l’application](registering-for-application-restart.md).

## <a name="developer-audience"></a>Développeurs concernés

ARR est conçu pour les développeurs C et C++.

## <a name="run-time-requirements"></a>Conditions d’exécution

ARR est disponible à partir du système d’exploitation Windows Vista.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                   | Description                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Utilisation de la récupération et du redémarrage de l’application](using-application-recovery-and-restart.md)<br/>         | Guide de procédures pour l’inscription pour la récupération et le redémarrage.<br/> |
| [Informations de référence sur la récupération et le redémarrage d’application](application-recovery-and-restart-reference.md)<br/> | Informations de référence pour l’API ARR. <br/>                    |



 

 

 





