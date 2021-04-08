---
title: Application de serveur de canal virtuel
description: Le module de serveur d’une application qui utilise des canaux virtuels doit être une application en mode utilisateur s’exécutant dans une session cliente sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Notez que vous devez fournir une méthode pour démarrer l’application serveur.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673809"
---
# <a name="virtual-channel-server-application"></a>Application de serveur de canal virtuel

Le module de serveur d’une application qui utilise des canaux virtuels doit être une application en mode utilisateur s’exécutant dans une session cliente sur le serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Notez que vous devez fournir une méthode pour démarrer l’application serveur. Pour ce faire, vous pouvez procéder de plusieurs façons : par exemple, vous pouvez utiliser un script d’ouverture de session ou un programme ou un script dans le dossier de démarrage. Les utilisateurs peuvent également lancer l’application.

Vous devez stocker le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé sous l’emplacement suivant :

**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** de contrôle CurrentControlSet du système de l’ordinateur local Terminal Server

Pour plus d’informations sur la sous-clé, consultez [surveillance des connexions de session et des déconnexions](monitoring-session-connections-and-disconnections.md).

L’application serveur peut appeler la fonction [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) pour ouvrir un handle vers un canal virtuel. L’application peut ensuite utiliser le descripteur dans l’une des fonctions suivantes.

<dl> <dt>

[**WTSVirtualChannelClose**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

Ferme un handle de canal virtuel ouvert.

</dd> <dt>

[**WTSVirtualChannelPurgeInput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

Supprime toutes les données d’entrée mises en file d’attente envoyées du client au serveur sur un canal virtuel spécifique.

> [!Note]  
> Cette fonction n’est actuellement pas utilisée par Services Bureau à distance.

 

</dd> <dt>

[**WTSVirtualChannelPurgeOutput**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

Supprime toutes les données de sortie en file d’attente envoyées du serveur au client sur un canal virtuel spécifique.

> [!Note]  
> Cette fonction n’est actuellement pas utilisée par Services Bureau à distance.

 

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

</dd> </dl>

 

 




