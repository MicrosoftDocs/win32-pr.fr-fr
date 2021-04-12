---
title: Traitement des groupes et des rappels
description: Le tableau suivant résume une série d’étapes dans une interaction opérationnelle entre un protocole de routage et le gestionnaire de groupe de multidiffusion.
ms.assetid: 43c1dc12-70fd-4e02-a7b1-5818e6d7ddc6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2878ec15cfb663353f3dd0bc1dc5aeadbd2e1e7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316637"
---
# <a name="processing-groups-and-callbacks"></a>Traitement des groupes et des rappels

Le tableau suivant résume une série d’étapes dans une interaction opérationnelle entre un protocole de routage et le gestionnaire de groupe de multidiffusion. La première colonne décrit les actions effectuées par le protocole de routage et les réponses du protocole de routage au gestionnaire de groupe de multidiffusion. La deuxième colonne décrit les réponses du gestionnaire de groupe de multidiffusion au protocole de routage et toutes les actions effectuées par le gestionnaire de groupe de multidiffusion, telles que les rappels. La troisième colonne présente des informations supplémentaires.

Chaque ligne de la table représente une étape.

Les tâches listées dans ce tableau ne se produisent pas dans un ordre spécifique. au lieu de cela, ils se produisent en fonction de l’état des appartenances aux groupes de multidiffusion. Le tableau ci-dessous montre un exemple d’ordre.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Action de protocole de routage</th>
<th>Action du gestionnaire de groupe de multidiffusion</th>
<th>Notes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gérer les appartenances aux groupes en fonction des informations de protocole reçues sur les interfaces que le protocole possède. La gestion s’effectue à l’aide des fonctions suivantes :
<ul>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry"><strong>MgmAddGroupMembershipEntry</strong></a></li>
<li><a href="/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry"><strong>MgmDeleteGroupMembershipEntry</strong></a></li>
</ul></td>
<td>Ajoutez et supprimez dans la liste des interfaces sortantes pour les entrées (s, g), (*, g) et (*, *) spécifiées. Cette liste représente l’ensemble des interfaces sur lesquelles les données de ce groupe sont transférées. Les données de ce groupe proviennent de la source spécifiée.</td>

</tr>
<tr class="even">

<td>Envoyer des alertes aux protocoles de routage sous forme de rappels. Les événements suivants déclenchent le gestionnaire de groupe de multidiffusion pour appeler un rappel :
<ul>
<li>Joindre ou conserver des groupes ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_join_alert_callback"><strong>PMGM_JOIN_ALERT_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_prune_alert_callback"><strong>PMGM_PRUNE_ALERT_CALLBACK</strong></a>).</li>
<li>L’appartenance au groupe a changé par IGMP ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_join_callback"><strong>PMGM_LOCAL_JOIN_CALLBACK</strong></a>, <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_local_leave_callback"><strong>PMGM_LOCAL_LEAVE_CALLBACK</strong></a>).</li>
<li>Données reçues sur une interface incorrecte ( <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_wrong_if_callback"><strong>PMGM_WRONG_IF_CALLBACK</strong></a>).</li>
<li>Données reçues à partir de nouvelles sources ou à un nouveau groupe ( <a href="/windows/desktop/api/mgm/nc-mgm-pmgm_creation_alert_callback"><strong>PMGM_CREATION_ALERT_CALLBACK</strong></a> et <a href="/windows/desktop/api/Mgm/nc-mgm-pmgm_rpf_callback"><strong>PMGM_RPF_CALLBACK</strong></a>).</li>
</ul></td>
<td>À l’aide de ces rappels, le gestionnaire de groupe de multidiffusion est en mesure de coordonner le transfert de paquets lorsque plusieurs protocoles de routage de multidiffusion sont présents sur un routeur.</td>
</tr>
<tr class="odd">
<td>Énumérer les entrées de transfert de multidiffusion (MFEs) à l’aide des fonctions <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe"><strong>MgmGetFirstMfe</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe"><strong>MgmGetNextMfe</strong></a>et <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe"><strong>MgmGetMfe</strong></a> . Prendre des décisions sur les données multidiffusion en fonction des résultats de l’énumération.</td>
<td>Retourne le MFEs demandé. Retourne ERROR_NO_MORE éléments lorsqu’il n’y a plus de MFEs à retourner.<br/></td>
<td>Utilisez les fonctions <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats"><strong>MgmGetFirstMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats"><strong>MgmGetNextMfeStats</strong></a>, <a href="/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats"><strong>MgmGetMfeStats</strong></a> pour énumérer les statistiques MFE. Pour obtenir un exemple complet de l’utilisation de ces fonctions, consultez <a href="administrative-application-scenario.md">scénario d’application administrative</a> .<br/></td>
</tr>
<tr class="even">
<td>Modifiez le voisin en amont dans un MFE à l’aide de la fonction <a href="/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe"><strong>MgmSetMfe</strong></a> .</td>

<td>Les clients utilisent cette fonction pour modifier les informations relatives à l’interface entrante.</td>
</tr>
</tbody>
</table>



 

 

