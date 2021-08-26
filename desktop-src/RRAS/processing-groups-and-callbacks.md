---
title: Traitement des groupes et des rappels
description: Le tableau suivant résume une série d’étapes dans une interaction opérationnelle entre un protocole de routage et le gestionnaire de groupe de multidiffusion.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3315f0a5db0dbcef9ac13e07ff9b9a2bb0b476be
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479685"
---
# <a name="processing-groups-and-callbacks"></a>Traitement des groupes et des rappels

Le tableau suivant résume une série d’étapes dans une interaction opérationnelle entre un protocole de routage et le gestionnaire de groupe de multidiffusion. La première colonne décrit les actions effectuées par le protocole de routage et les réponses du protocole de routage au gestionnaire de groupe de multidiffusion. La deuxième colonne décrit les réponses du gestionnaire de groupe de multidiffusion au protocole de routage et toutes les actions effectuées par le gestionnaire de groupe de multidiffusion, telles que les rappels. La troisième colonne présente des informations supplémentaires.

Chaque ligne de la table représente une étape.

Les tâches listées dans ce tableau ne se produisent pas dans un ordre spécifique. au lieu de cela, ils se produisent en fonction de l’état des appartenances aux groupes de multidiffusion. Le tableau ci-dessous montre un exemple d’ordre.




| Action de protocole de routage | Action du gestionnaire de groupe de multidiffusion | Notes | 
|-------------------------|--------------------------------|-------|
| Gérer les appartenances aux groupes en fonction des informations de protocole reçues sur les interfaces que le protocole possède. La gestion s’effectue à l’aide des fonctions suivantes :<ul><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li><li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li></ul> | Ajoutez et supprimez dans la liste des interfaces sortantes pour les entrées (s, g), (*, g) et (*, *) spécifiées. Cette liste représente l’ensemble des interfaces sur lesquelles les données de ce groupe sont transférées. Les données de ce groupe proviennent de la source spécifiée. | 
| Envoyer des alertes aux protocoles de routage sous forme de rappels. Les événements suivants déclenchent le gestionnaire de groupe de multidiffusion pour appeler un rappel :<ul><li>Joindre ou conserver des groupes ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li><li>L’appartenance au groupe a changé par IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li><li>Données reçues sur une interface incorrecte ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li><li>Données reçues à partir de nouvelles sources ou à un nouveau groupe ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> et <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</li></ul> | À l’aide de ces rappels, le gestionnaire de groupe de multidiffusion est en mesure de coordonner le transfert de paquets lorsque plusieurs protocoles de routage de multidiffusion sont présents sur un routeur. | 
| Énumérer les entrées de transfert de multidiffusion (MFEs) à l’aide des fonctions <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>et <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> . Prendre des décisions sur les données multidiffusion en fonction des résultats de l’énumération. | Retourne le MFEs demandé. Retourne ERROR_NO_MORE éléments lorsqu’il n’y a plus de MFEs à retourner.<br /> | Utilisez les fonctions <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> pour énumérer les statistiques MFE. Pour obtenir un exemple complet de l’utilisation de ces fonctions, consultez <a href="administrative-application-scenario.md">scénario d’application administrative</a> .<br /> | 
| Modifiez le voisin en amont dans un MFE à l’aide de la fonction <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> . | Les clients utilisent cette fonction pour modifier les informations relatives à l’interface entrante. | 




 

 

