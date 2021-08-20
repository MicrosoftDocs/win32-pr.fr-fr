---
title: Structures d’API Services Bureau à distance
description: Répertorie les structures utilisées avec l’API Services Bureau à distance.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3161d7c8e8b295e42930af1edcc79b7c60d83b61097b4d02661c1b11b5f1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000099"
---
# <a name="remote-desktop-services-api-structures"></a>Structures d’API Services Bureau à distance

Les structures suivantes sont utilisées avec l’API Services Bureau à distance.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**définition de canal \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Contient le nom et les options d’une Services Bureau à distance canal virtuel.

</dd> <dt>

[**\_points d’entrée du canal \_**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Contient des pointeurs vers les fonctions appelées par une DLL côté client pour accéder aux canaux virtuels.

</dd> <dt>

[**\_ \_ en-tête de PDU de canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Contient des informations sur un bloc de données reçu par l’extrémité serveur d’un canal virtuel.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Contient des informations sur un jeu de clés de licence Services Bureau à distance spécifique.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Contient des informations sur une licence de Services Bureau à distance spécifique.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Contient des informations sur un client Connexion Bureau à distance (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Contient des informations sur une session de Services Bureau à distance.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Contient des informations sur une session de Services Bureau à distance.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Contient une Union de [**\_ niveau WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) qui contient des informations étendues sur une session de services Bureau à distance.

</dd> <dt>

[**WTSINFOEX \_ niveau1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Contient des informations étendues sur une session de Services Bureau à distance.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Contient des informations sur un écouteur de Services Bureau à distance.

</dd> <dt>

[**\_adresse IP \_ WTSSBX**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Contient des informations sur l’adresse IP d’une ressource réseau.

</dd> <dt>

[**informations de connexion à la \_ machine WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Contient des informations sur un ordinateur qui accepte les connexions à distance.

</dd> <dt>

[**\_informations sur la machine WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Contient des informations sur un ordinateur et son état actuel.

</dd> <dt>

[**\_informations sur la session WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Contient des informations sur les sessions disponibles pour Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance).

</dd> <dt>

[**\_notification WTSSESSION**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Fournit des informations sur la notification de modification de session. Un service reçoit cette structure dans sa fonction [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) en réponse à un événement de changement de session.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Contient les informations de configuration d’un utilisateur sur un contrôleur de domaine ou un serveur d’hôte de session de Bureau à distance (hôte de session Bureau à distance).

</dd> <dt>

[**WTS \_ adresse du CLIENT \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Contient l’adresse réseau du client d’une session de Services Bureau à distance.

</dd> <dt>

[**WTS \_ affichage du CLIENT \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Contient des informations sur l’affichage d’un client Connexion Bureau à distance (RDC).

</dd> <dt>

[**WTS \_ \_informations sur le processus**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Contient des informations sur un processus en cours d’exécution sur un serveur hôte de session Bureau à distance.

</dd> <dt>

[**WTS \_ \_informations sur le processus \_ ex.**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Contient des informations étendues sur un processus en cours d’exécution sur un serveur hôte de session Bureau à distance.

</dd> <dt>

[**WTS \_ \_informations sur le produit**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Détails de la licence de produit requise pour se connecter à un serveur Terminal Server.

</dd> <dt>

[**WTS \_ \_informations sur le serveur**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Contient des informations sur un serveur de Services Bureau à distance spécifique.

</dd> <dt>

[**WTS \_ adresse de la SESSION \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Contient l’adresse IP virtuelle assignée à une session.

</dd> <dt>

[**WTS \_ \_informations sur la session**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Contient des informations sur une session cliente sur un serveur hôte de session Bureau à distance.

</dd> <dt>

[**WTS \_ Informations de SESSION \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Contient des informations étendues sur une session cliente sur un serveur hôte de session Bureau à distance ou un serveur serveur hôte de virtualisation des services Bureau à distance (hôte de virtualisation des services Bureau à distance).

</dd> </dl>

 

 