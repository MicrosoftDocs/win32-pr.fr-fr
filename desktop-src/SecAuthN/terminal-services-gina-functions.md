---
description: Lorsque les services Terminal Server sont activés, GINA doit appeler les fonctions de prise en charge de Winlogon pour terminer l’installation de chaque utilisateur, pour interroger les informations d’identification d’une session cliente des services Terminal Server et pour se déconnecter d’une session réseau des services Terminal Server. notez que les dll GINA sont ignorées dans Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Fonctions GINA des services Terminal Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0bdd81d66d88ae280c14d71d7d65385c0d5580b3e28cef9d0f26ed1963bded1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916391"
---
# <a name="terminal-services-gina-functions"></a>Fonctions GINA des services Terminal Server

Lorsque les services Terminal Server sont activés, [*Gina*](../secgloss/g-gly.md) doit appeler les fonctions de prise en charge de [*Winlogon*](../secgloss/w-gly.md) pour terminer l’installation de chaque utilisateur, pour interroger les [*informations d’identification*](../secgloss/c-gly.md) d’une session cliente des services Terminal Server et pour se déconnecter d’une session réseau des services Terminal Server.

> [!Note]  
> les dll GINA sont ignorées dans Windows Vista.

 

Ces fonctions de prise en charge sont les suivantes.



| Fonction                                                                     | Description                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Termine l’installation de l’utilisateur.                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Appelé pour interroger les informations d’identification des clients distants qui n’utilisent pas de licence de connecteur Internet. |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Appelé pour interroger les informations d’identification des clients distants qui utilisent une licence de connecteur Internet.     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Appelé pour récupérer les informations de configuration de l’utilisateur des services Terminal Server.                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Appelé pour se déconnecter d’une session réseau des services Terminal Server.                                      |



 

Pour accéder à ces fonctions de prise en charge de Winlogon, la DLL GINA doit utiliser la structure [**wlx \_ Dispatch \_ version \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) . Dans la fonction [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) de la Gina, les deux paramètres doivent être au moins wlx \_ version \_ 1 \_ 3.

 

 
