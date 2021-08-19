---
title: Services Bureau à distance les fonctions de l’API
description: Les fonctions suivantes sont utilisées avec Services Bureau à distance.
ms.assetid: e99a86ee-af0e-46db-8dad-69703ca84fa0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5434f009d15bccc1db8279e576b71f079c8d73119a2d82bb8fd313dcc1837c47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000249"
---
# <a name="remote-desktop-services-api-functions"></a>Services Bureau à distance les fonctions de l’API

Les fonctions suivantes sont utilisées avec Services Bureau à distance.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid)
</dt> <dd>

Récupère la session de Services Bureau à distance associée à un processus spécifié.

</dd> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dd>

Ouvre un handle vers le serveur de licences de Bureau à distance spécifié.

</dd> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> <dd>

Ferme un handle ouvert sur un serveur de licences Bureau à distance.

</dd> <dt>

[**TLSGetServerCertificate**](tlsgetservercertificate.md)
</dt> <dd>

Retourne le certificat du serveur de licences Bureau à distance.

</dd> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dd>

Commence l’énumération par le biais de tous les jeux de clés installés sur un serveur de licences Bureau à distance en fonction des critères de recherche.

</dd> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> <dd>

Continue à partir d’un appel précédent à la fonction [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) et met fin à l’énumération.

</dd> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dd>

Continue à partir d’un appel précédent à la fonction [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) et retourne le prochain Pack de clés installé sur un serveur de licences bureau à distance qui correspond aux critères de recherche.

</dd> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dd>

Commence l’énumération des licences émises par le serveur de licences Bureau à distance en fonction des critères de recherche.

</dd> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> <dd>

Continue à partir d’un appel précédent à la fonction [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) et met fin à l’énumération.

</dd> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dd>

Continue à partir d’un appel précédent à la fonction [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) et retourne la licence suivante qui est installée sur un serveur de licences bureau à distance qui correspond aux critères de recherche.

</dd> <dt>

[**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)
</dt> <dd>

Ferme l’extrémité client d’un canal virtuel.

</dd> <dt>

[**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry)
</dt> <dd>

Point d’entrée défini par l’application pour la DLL côté client d’une application qui utilise Services Bureau à distance canaux virtuels.

</dd> <dt>

[**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)
</dt> <dd>

Initialise l’accès d’une DLL client à Services Bureau à distance canaux virtuels.

</dd> <dt>

[*VirtualChannelInitEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn)
</dt> <dd>

Fonction de rappel définie par l’application qui Services Bureau à distance appelle pour notifier la DLL client des événements de canal virtuel.

</dd> <dt>

[**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)
</dt> <dd>

Ouvre l’extrémité client d’un canal virtuel.

</dd> <dt>

[*VirtualChannelOpenEvent*](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn)
</dt> <dd>

Fonction de rappel définie par l’application qui Services Bureau à distance appelle pour notifier la DLL client des événements pour un canal virtuel spécifique.

</dd> <dt>

[**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)
</dt> <dd>

Envoie des données de l’extrémité client d’un canal virtuel à une application partenaire côté serveur.

</dd> <dt>

[**WTSCloseServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscloseserver)
</dt> <dd>

Ferme un handle ouvert sur un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).

</dd> <dt>

[**WTSConnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsconnectsessiona)
</dt> <dd>

Connecte une session de Services Bureau à distance à une session existante sur l’ordinateur local.

</dd> <dt>

[**WTSCreateListener**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtscreatelistenera)
</dt> <dd>

Crée un écouteur de Services Bureau à distance ou configure un écouteur existant.

</dd> <dt>

[**WTSDisconnectSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsdisconnectsession)
</dt> <dd>

Déconnecte l’utilisateur connecté de la session de Services Bureau à distance spécifiée sans fermer la session.

</dd> <dt>

[**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
</dt> <dd>

Active ou désactive les [sessions enfants](child-sessions.md).

</dd> <dt>

[**WTSEnumerateListeners**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratelistenersa)
</dt> <dd>

Énumère tous les écouteurs Services Bureau à distance sur un serveur hôte de session Bureau à distance.

</dd> <dt>

[**WTSEnumerateProcesses**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesa)
</dt> <dd>

Récupère des informations sur les processus actifs sur un serveur hôte de session Bureau à distance spécifié.

</dd> <dt>

[**WTSEnumerateProcessesEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateprocessesexa)
</dt> <dd>

Récupère des informations sur les processus actifs sur le serveur hôte de session Bureau à distance ou le serveur serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance) spécifié.

</dd> <dt>

[**WTSEnumerateServers**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumerateserversa)
</dt> <dd>

Retourne une liste de tous les serveurs hôtes de session Bureau à distance dans le domaine spécifié.

</dd> <dt>

[**WTSEnumerateSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsa)
</dt> <dd>

Récupère une liste de sessions sur un serveur hôte de session Bureau à distance.

</dd> <dt>

[**WTSEnumerateSessionsEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenumeratesessionsexa)
</dt> <dd>

Récupère une liste de sessions sur un serveur hôte de session Bureau à distance spécifié ou un serveur hôte de virtualisation des services Bureau à distance.

</dd> <dt>

[**WTSFreeMemory**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememory)
</dt> <dd>

Libère la mémoire allouée par une fonction Services Bureau à distance.

</dd> <dt>

[**WTSFreeMemoryEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsfreememoryexa)
</dt> <dd>

libère de la mémoire qui contient [**WTS les \_ informations de processus \_ \_ EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa) ou [**WTS structures informations de \_ SESSION \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a) allouées par une fonction Services Bureau à distance.

</dd> <dt>

[**WTSGetActiveConsoleSessionId**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid)
</dt> <dd>

Récupère l’identificateur de session de la session de console.

</dd> <dt>

[**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
</dt> <dd>

Récupère l’identificateur de session enfant, le cas échéant.

</dd> <dt>

[**WTSGetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetlistenersecuritya)
</dt> <dd>

Récupère le descripteur de sécurité d’un écouteur de Services Bureau à distance.

</dd> <dt>

[**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
</dt> <dd>

Détermine si les sessions enfants sont activées.

</dd> <dt>

[**WTSLogoffSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtslogoffsession)
</dt> <dd>

Déconnecte une session de Services Bureau à distance spécifiée.

</dd> <dt>

[**WTSOpenServer**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenservera)
</dt> <dd>

Ouvre un handle vers le serveur hôte de session Bureau à distance spécifié.

</dd> <dt>

[**WTSOpenServerEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsopenserverexa)
</dt> <dd>

Ouvre un handle vers le serveur hôte de session Bureau à distance spécifié ou le serveur hôte de virtualisation des services Bureau à distance.

</dd> <dt>

[**WTSQueryListenerConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerylistenerconfiga)
</dt> <dd>

Récupère les informations de configuration d’un écouteur de Services Bureau à distance.

</dd> <dt>

[**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa)
</dt> <dd>

Récupère les informations de session pour la session spécifiée sur le serveur hôte de session Bureau à distance spécifié.

</dd> <dt>

[**WTSQueryUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryuserconfiga)
</dt> <dd>

Récupère les informations de configuration pour l’utilisateur spécifié sur le contrôleur de domaine spécifié ou le serveur hôte de session Bureau à distance.

</dd> <dt>

[**WTSQueryUserToken**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsqueryusertoken)
</dt> <dd>

Obtient le jeton d’accès principal de l’utilisateur connecté spécifié par l’ID de session.

</dd> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dd>

Inscrit la fenêtre spécifiée pour recevoir des notifications de modification de session.

</dd> <dt>

[**WTSRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotificationex)
</dt> <dd>

Inscrit la fenêtre spécifiée pour recevoir des notifications de modification de session.

</dd> <dt>

[**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea)
</dt> <dd>

Affiche une boîte de message sur le Bureau du client d’une session de Services Bureau à distance spécifiée.

</dd> <dt>

[**WTSSetListenerSecurity**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetlistenersecuritya)
</dt> <dd>

Configure le descripteur de sécurité d’un écouteur de Services Bureau à distance.

</dd> <dt>

[**WTSSetUserConfig**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssetuserconfiga)
</dt> <dd>

Modifie les informations de configuration pour l’utilisateur spécifié sur le contrôleur de domaine spécifié ou le serveur hôte de session Bureau à distance.

</dd> <dt>

[**WTSShutdownSystem**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsshutdownsystem)
</dt> <dd>

Arrête (et éventuellement redémarre) le serveur hôte de session Bureau à distance spécifié.

</dd> <dt>

[**WTSStartRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstartremotecontrolsessiona)
</dt> <dd>

Démarre le contrôle à distance d’une autre session de Services Bureau à distance. Vous devez appeler cette fonction à partir d’une session à distance.

</dd> <dt>

[**WTSStopRemoteControlSession**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsstopremotecontrolsession)
</dt> <dd>

Arrête une session de contrôle à distance.

</dd> <dt>

[**WTSTerminateProcess**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsterminateprocess)
</dt> <dd>

Termine le processus spécifié sur le serveur hôte de session Bureau à distance spécifié.

</dd> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> <dd>

Annule l’inscription de la fenêtre spécifiée afin qu’elle ne reçoive plus de notifications de modification de session.

</dd> <dt>

[**WTSUnRegisterSessionNotificationEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotificationex)
</dt> <dd>

Annule l’inscription de la fenêtre spécifiée afin qu’elle ne reçoive plus de notifications de modification de session.

</dd> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Ferme un handle de canal virtuel ouvert.

</dd> <dt>

[**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen)
</dt> <dd>

Ouvre un handle vers l’extrémité serveur d’un canal virtuel spécifié.

</dd> <dt>

[**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
</dt> <dd>

Crée un canal virtuel d’une manière similaire à [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen).

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Supprime toutes les données d’entrée mises en file d’attente envoyées du client au serveur sur un canal virtuel spécifié.

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Supprime toutes les données de sortie en file d’attente envoyées du serveur au client sur un canal virtuel spécifié.

</dd> <dt>

[**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

Retourne des informations sur un canal virtuel spécifié.

</dd> <dt>

[**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

Lit les données à partir de l’extrémité serveur d’un canal virtuel.

</dd> <dt>

[**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

Écrit des données à l’extrémité serveur d’un canal virtuel.

</dd> <dt>

[**WTSWaitSystemEvent**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtswaitsystemevent)
</dt> <dd>

Attend un événement Services Bureau à distance avant de retourner à l’appelant.

</dd> </dl>

 

 