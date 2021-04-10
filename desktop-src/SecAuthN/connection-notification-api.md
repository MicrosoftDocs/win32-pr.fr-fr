---
description: Le routeur multifournisseur (MPR) appelle les fonctions de notification de connexion lorsqu’il se connecte ou déconnecte une ressource réseau. Pour recevoir ces notifications, vous pouvez implémenter ces fonctions dans une DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API de notification de connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114942"
---
# <a name="connection-notification-api"></a>API de notification de connexion

Le [*routeur multifournisseur*](/windows/desktop/SecGloss/m-gly) (MPR) appelle les fonctions de notification de connexion lorsqu’il se connecte ou déconnecte une ressource réseau. Pour recevoir ces notifications, vous pouvez implémenter ces fonctions dans une DLL.

Le MPR appelle la fonction [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) avant et après chaque opération d’ajout de connexion ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)ou [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Cette fonction n’est pas appelée lorsque le MPR restaure automatiquement les connexions réseau.

Le MPR appelle la fonction [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) avant et après chaque opération d’annulation de connexion ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) ou [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

Pour plus d’informations sur les fonctions WNet, consultez [mise en réseau Windows](/windows/desktop/WNet/windows-networking-wnet-).

Pour plus d’informations sur la création et l’inscription d’une application qui reçoit des notifications de connexion réseau, consultez réception de notifications de [connexion](receiving-connection-notifications.md) et [inscription pour recevoir des notifications de connexion](registering-to-receive-connection-notifications.md).

 

 
