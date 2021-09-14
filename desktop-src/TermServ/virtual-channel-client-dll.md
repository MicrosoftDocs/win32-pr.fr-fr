---
title: DLL du client du canal virtuel
description: Le client d’une application de canaux virtuels est une DLL qui est chargée pendant l’initialisation Services Bureau à distance sur l’ordinateur client. La DLL doit être inscrite sur l’ordinateur client.
ms.assetid: fca0505c-c4a9-4230-aeaa-ff3dfa62f581
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd7ffccda8b1da7dfc3920b0a47a12e97840e0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217353"
---
# <a name="virtual-channel-client-dll"></a>DLL du client du canal virtuel

Le client d’une application de canaux virtuels est une DLL qui est chargée pendant l’initialisation Services Bureau à distance sur l’ordinateur client. La DLL doit être inscrite sur l’ordinateur client. Pour plus d’informations, consultez [inscription du client du canal virtuel](virtual-channel-client-registration.md).

La DLL cliente doit exporter une fonction [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) , qui services Bureau à distance des appels pendant l’initialisation. Le point d’entrée **VirtualChannelEntry** reçoit un pointeur vers une structure de [**points d' \_ entrée \_ de canal**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points) . Cette structure contient des pointeurs vers les fonctions que la DLL client appelle pour accéder aux canaux virtuels.



| Fonction                                                      | Description                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit)<br/>   | Inscrit les noms des canaux virtuels à utiliser par le client et fournit une fonction de rappel [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) par le biais de laquelle services Bureau à distance notifie au client les événements qui affectent la connexion cliente.<br/> |
| [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen)<br/>   | Ouvre l’extrémité client d’un canal virtuel spécifié et fournit une fonction de rappel [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) par le biais de laquelle services Bureau à distance notifie au client les événements qui affectent le canal virtuel.<br/>                    |
| [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite)<br/> | Écrit des données dans un canal virtuel. Services Bureau à distance envoie ces données à l’extrémité serveur du canal virtuel. Le serveur end appelle la fonction [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) pour lire les données.<br/>                                             |
| [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose)<br/> | Ferme un canal virtuel.<br/>                                                                                                                                                                                                                                                  |



 

La fonction [**VirtualChannelEntry**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelentry) de votre dll doit appeler la fonction [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) pour initialiser l’accès aux canaux virtuels. Quand vous appelez **VirtualChannelInit**, vous devez passer un pointeur vers la fonction de rappel [**VirtualChannelInitEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_init_event_fn) . Services Bureau à distance appelle cette fonction de rappel lorsque l’initialisation est terminée et de nouveau quand une connexion a été établie avec un serveur d’hôte de session Bureau à distance (hôte de session Bureau à distance).

Une fois la connexion établie, vous pouvez appeler la fonction [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) pour ouvrir les canaux virtuels enregistrés par l’appel [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) . L’appel **VirtualChannelOpen** spécifie un pointeur vers votre fonction de rappel [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) .

Après le retour de l’appel [**VirtualChannelOpen**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelopen) , vous pouvez appeler la fonction [**VirtualChannelWrite**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelwrite) pour écrire dans le canal virtuel. L’opération d’écriture étant asynchrone, vous ne devez pas libérer ou réutiliser la mémoire tampon transmise à **VirtualChannelWrite** tant que services Bureau à distance n’a pas appelé votre fonction [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) pour indiquer que l’opération d’écriture est terminée. Quand vous appelez **VirtualChannelWrite**, vous pouvez passer un élément de données utilisateur qui identifie l’opération d’écriture. Services Bureau à distance transmet à nouveau ces données utilisateur lorsqu’il appelle **VirtualChannelOpenEvent** pour vous avertir que l’opération est terminée. À l’extrémité serveur du canal virtuel, le complément serveur appelle la fonction [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread) pour lire les données.

Services Bureau à distance appelle également votre fonction [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) lorsque des données sont écrites sur le canal virtuel par le module de serveur. Le module serveur appelle la fonction [**WTSVirtualChannelWrite**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite) pour écrire des données à l’extrémité serveur du canal virtuel.

Les modules client et serveur peuvent écrire des blocs de données de n’importe quelle taille sur le canal virtuel. Toutefois, avant d’envoyer les données, Services Bureau à distance segmente les données en segments d' \_ octets de longueur de segment de canal \_ . Services Bureau à distance appelle votre fonction [**VirtualChannelOpenEvent**](/windows/desktop/api/Cchannel/nc-cchannel-channel_open_event_fn) une fois pour chaque segment de données, plutôt que de recréer les données dans un bloc de la taille d’origine. Chaque appel à **VirtualChannelOpenEvent** indique la taille du segment, la taille totale écrite par le serveur et indique si les données constituent le début, le milieu ou la fin d’un bloc écrit par le serveur.

Vous pouvez appeler la fonction [**VirtualChannelClose**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelclose) pour fermer un canal. Toutefois, il n’est pas nécessaire de l’appeler, car Services Bureau à distance ferme automatiquement tous les canaux lorsque le client se déconnecte du serveur.

 

 





