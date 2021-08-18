---
description: Winlogon et GINA doivent communiquer les informations d’initialisation, gérer la surveillance et la notification des séquences de touches sécurisées et autoriser les activités de fermeture de session et d’arrêt.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: Interaction entre Winlogon et GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824c658e4f19b14de339b569a8c9d17992c1b60bb5d4d526de949ce76cd1554d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482359"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interaction entre Winlogon et GINA

[*Winlogon*](../secgloss/w-gly.md) et [*Gina*](../secgloss/g-gly.md) doivent communiquer les informations d’initialisation, gérer la surveillance et la notification des [*séquences de touches sécurisées*](../secgloss/s-gly.md) et autoriser les activités de fermeture de session et d’arrêt. L’état de Winlogon détermine la fonction GINA appelée pour traiter tout événement SAS donné. Les communications se produisent dans l’ordre indiqué ici.

> [!Note]  
> les dll GINA sont ignorées dans Windows Vista.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Événement</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Démarrage de station de travail</td>
<td><ol>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> de Gina pour notifier à Gina la version de Winlogon en cours d’utilisation.</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> de la Gina pour fournir à la Gina les adresses des fonctions de prise en charge, un handle vers Winlogon et pour obtenir les informations de <a href="/windows/desktop/SecGloss/c-gly"><em>contexte</em></a> de la Gina (à utiliser dans tous les appels futurs à Gina).<br/> Winlogon est dans l’état déconnecté.<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>Personne n’est connecté</td>
<td>(Le GINA analyse les appareils pour les événements SAS).
<ol>
<li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon lorsqu’un événement SAS a été reçu.</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> de la Gina, ce qui permet à Gina de traiter les informations d’identification et d’authentification d’un utilisateur.<br/> Une fois l’ouverture de session réussie, Winlogon est dans l’état connecté.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>L’utilisateur a ouvert une session</td>
<td>(Le GINA analyse les appareils pour les événements SAS).
<ol>
<li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon lorsqu’un événement SAS a été reçu.</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina, ce qui permet à Gina de présenter des options à l’utilisateur actuellement connecté.</li>
</ol></td>
</tr>
<tr class="even">
<td>L’utilisateur a ouvert une session et souhaite verrouiller l’ordinateur</td>
<td>(Le GINA analyse les appareils pour les événements SAS).
<ol>
<li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</li>
<li>GINA retourne WLX_SAS_ACTION_LOCK_WKSTA.<br/> Winlogon est dans l’état verrouillé de la station de travail.<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>L’utilisateur a ouvert une session, la station de travail est verrouillée et l’utilisateur souhaite déverrouiller l’ordinateur</td>
<td>(Le GINA analyse les appareils pour les événements SAS).
<ol>
<li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> de la Gina.</li>
<li>GINA retourne WLX_SAS_ACTION_UNLOCK_WKSTA.</li>
</ol></td>
</tr>
<tr class="even">
<td>L’utilisateur a ouvert une session et le programme appelle la fonction <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a></td>
<td>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</td>
</tr>
<tr class="odd">
<td>L’utilisateur a ouvert une session et souhaite se déconnecter à l’aide d’une signature d’accès partagé</td>
<td>(Le GINA analyse les appareils pour les événements SAS).
<ol>
<li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</li>
<li>GINA retourne WLX_SAS_ACTION_LOGOFF.</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</li>
</ol></td>
</tr>
<tr class="even">
<td>L’utilisateur a ouvert une session et souhaite se déconnecter et s’arrêter à l’aide de <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a></td>
<td><ol>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de la Gina.</li>
</ol></td>
</tr>
<tr class="odd">
<td>L’utilisateur a ouvert une session et souhaite se déconnecter et s’arrêter à l’aide d’une signature d’accès partagé</td>
<td>(Le GINA analyse les appareils pour les événements SAS).
<ol>
<li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</li>
<li>GINA retourne WLX_SAS_ACTION_SHUTDOWN.</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</li>
<li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de la Gina.</li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 
