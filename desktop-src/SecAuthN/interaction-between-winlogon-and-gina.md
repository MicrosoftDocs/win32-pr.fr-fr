---
description: Winlogon et GINA doivent communiquer les informations d’initialisation, gérer la surveillance et la notification des séquences de touches sécurisées et autoriser les activités de fermeture de session et d’arrêt.
ms.assetid: ea45cd5f-9cb0-41bb-99bf-f84781ae9604
title: Interaction entre Winlogon et GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60781a51ae2c99df25e30b7119dde086b5d6e1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011279"
---
# <a name="interaction-between-winlogon-and-gina"></a>Interaction entre Winlogon et GINA

[*Winlogon*](../secgloss/w-gly.md) et [*Gina*](../secgloss/g-gly.md) doivent communiquer les informations d’initialisation, gérer la surveillance et la notification des [*séquences de touches sécurisées*](../secgloss/s-gly.md) et autoriser les activités de fermeture de session et d’arrêt. L’état de Winlogon détermine la fonction GINA appelée pour traiter tout événement SAS donné. Les communications se produisent dans l’ordre indiqué ici.

> [!Note]  
> les dll GINA sont ignorées dans Windows Vista.

 




| Événement | Description | 
|-------|-------------|
| Démarrage de station de travail | <ol><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate"><strong>WlxNegotiate</strong></a> de Gina pour notifier à Gina la version de Winlogon en cours d’utilisation.</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize"><strong>WlxInitialize</strong></a> de la Gina pour fournir à la Gina les adresses des fonctions de prise en charge, un handle vers Winlogon et pour obtenir les informations de <a href="/windows/desktop/SecGloss/c-gly"><em>contexte</em></a> de la Gina (à utiliser dans tous les appels futurs à Gina).<br /> Winlogon est dans l’état déconnecté.<br /></li></ol> | 
| Personne n’est connecté | (Le GINA analyse les appareils pour les événements SAS).<ol><li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon lorsqu’un événement SAS a été reçu.</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas"><strong>WlxLoggedOutSAS</strong></a> de la Gina, ce qui permet à Gina de traiter les informations d’identification et d’authentification d’un utilisateur.<br /> Une fois l’ouverture de session réussie, Winlogon est dans l’état connecté.<br /></li></ol> | 
| L’utilisateur a ouvert une session | (Le GINA analyse les appareils pour les événements SAS).<ol><li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> de Winlogon lorsqu’un événement SAS a été reçu.</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de Gina, ce qui permet à Gina de présenter des options à l’utilisateur actuellement connecté.</li></ol> | 
| L’utilisateur a ouvert une session et souhaite verrouiller l’ordinateur | (Le GINA analyse les appareils pour les événements SAS).<ol><li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</li><li>GINA retourne WLX_SAS_ACTION_LOCK_WKSTA.<br /> Winlogon est dans l’état verrouillé de la station de travail.<br /></li></ol> | 
| L’utilisateur a ouvert une session, la station de travail est verrouillée et l’utilisateur souhaite déverrouiller l’ordinateur | (Le GINA analyse les appareils pour les événements SAS).<ol><li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxwkstalockedsas"><strong>WlxWkstaLockedSAS</strong></a> de la Gina.</li><li>GINA retourne WLX_SAS_ACTION_UNLOCK_WKSTA.</li></ol> | 
| L’utilisateur a ouvert une session et le programme appelle la fonction <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"><strong>ExitWindowsEx</strong></a> | Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina. | 
| L’utilisateur a ouvert une session et souhaite se déconnecter à l’aide d’une signature d’accès partagé | (Le GINA analyse les appareils pour les événements SAS).<ol><li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</li><li>GINA retourne WLX_SAS_ACTION_LOGOFF.</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</li></ol> | 
| L’utilisateur a ouvert une session et souhaite se déconnecter et s’arrêter à l’aide de <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex"> <strong>ExitWindowsEx</strong></a> | <ol><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de la Gina.</li></ol> | 
| L’utilisateur a ouvert une session et souhaite se déconnecter et s’arrêter à l’aide d’une signature d’accès partagé | (Le GINA analyse les appareils pour les événements SAS).<ol><li>GINA appelle la fonction <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify"><strong>WlxSasNotify</strong></a> .</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedonsas"><strong>WlxLoggedOnSAS</strong></a> de la Gina.</li><li>GINA retourne WLX_SAS_ACTION_SHUTDOWN.</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxlogoff"><strong>WlxLogoff</strong></a> de la Gina.</li><li>Winlogon appelle la fonction <a href="/windows/desktop/api/Winwlx/nf-winwlx-wlxshutdown"><strong>WlxShutdown</strong></a> de la Gina.</li></ol> | 




 

 

 
