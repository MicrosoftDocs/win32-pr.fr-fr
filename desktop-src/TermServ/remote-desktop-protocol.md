---
title: Protocole RDP (Remote Desktop Protocol)
description: le protocole RDP (Bureau à distance Microsoft Protocol) fournit des fonctionnalités d’entrée et d’entrée à distance sur les connexions réseau pour les applications basées sur Windows qui s’exécutent sur un serveur.
ms.assetid: 442c3c7f-d04b-4dcd-945d-f6e0168c59d5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance protocole RDP (Remote Desktop Protocol) (RDP)
- RDP (voir protocole RDP (Remote Desktop Protocol))
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a322e90bd036533e357925607fac6a78c364eababad5f353b4d53dfa51df735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756170"
---
# <a name="remote-desktop-protocol"></a>Protocole RDP (Remote Desktop Protocol)

le protocole RDP (Bureau à distance Microsoft Protocol) fournit des fonctionnalités d’entrée et d’entrée à distance sur les connexions réseau pour les applications basées sur Windows qui s’exécutent sur un serveur. RDP est conçu pour prendre en charge différents types de topologies de réseau et de plusieurs protocoles LAN.

> [!Note]  
> Cette rubrique est destinée aux développeurs de logiciels. si vous recherchez des informations utilisateur pour Bureau à distance, consultez [Windows Support](https://windows.microsoft.com/windows/support#1TC=windows-8). Si vous recherchez des informations destinées aux professionnels de l’informatique pour Bureau à distance, consultez [services Bureau à distance sur TechNet](/windows/deployment/deploy-whats-new).

 

## <a name="basic-architecture"></a>Architecture de base

RDP est basé sur et sur une extension de la famille de protocoles ITU T. 120. RDP est un protocole prenant en charge plusieurs canaux qui autorise des canaux virtuels distincts pour transporter les données de communication et de présentation des appareils à partir du serveur, ainsi que des données de clavier et de souris du client chiffrées. RDP fournit une base extensible et prend en charge jusqu’à 64 000 canaux distincts pour la transmission de données et les dispositions pour la transmission multipoint.

Sur le serveur, RDP utilise son propre pilote vidéo pour restituer la sortie d’affichage en construisant les informations de rendu dans des paquets réseau à l’aide du protocole RDP et en les envoyant au client via le réseau. sur le client, le protocole RDP reçoit les données de rendu et interprète les paquets dans les appels d’API GDI (graphics device interface) de Microsoft Windows correspondants. Pour le chemin d’entrée, les événements de souris et de clavier du client sont redirigés du client vers le serveur. Sur le serveur, RDP utilise son propre pilote de clavier et de souris pour recevoir ces événements de clavier et de souris.

Dans une session Bureau à distance, toutes les variables d’environnement (par exemple, les variables déterminant la profondeur de couleur et l’activation et la désactivation du papier peint) sont déterminées par les paramètres de connexion RCP-Tcp. Cela s’applique à toutes les fonctions et méthodes qui définissent les variables d’environnement dans la [référence connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md) et l' [interface du fournisseur WMI services Bureau à distance](terminal-services-wmi-provider-reference.md).

## <a name="features"></a>Fonctionnalités

Microsoft RDP comprend les fonctionnalités suivantes :

<dl> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>Chiffre
</dt> <dd>

RDP utilise le chiffrement RC4 de RSA Security, un chiffrement de flux conçu pour chiffrer efficacement de petites quantités de données. RC4 est conçu pour sécuriser les communications sur les réseaux. Les administrateurs peuvent choisir de chiffrer les données à l’aide d’une clé 56 ou 128 bits.

</dd> <dt>

<span id="Bandwidth_reduction_features"></span><span id="bandwidth_reduction_features"></span><span id="BANDWIDTH_REDUCTION_FEATURES"></span>Fonctionnalités de réduction de bande passante
</dt> <dd>

RDP prend en charge différents mécanismes pour réduire la quantité de données transmises sur une connexion réseau. Les mécanismes incluent la compression des données, la mise en cache persistante des bitmaps et la mise en cache des glyphes et des fragments dans la RAM. Le cache de bitmaps persistant peut améliorer considérablement les performances par rapport aux connexions à faible bande passante, en particulier lors de l’exécution d’applications qui utilisent intensivement des bitmaps de grande taille.

</dd> <dt>

<span id="Roaming_disconnect"></span><span id="roaming_disconnect"></span><span id="ROAMING_DISCONNECT"></span>Déconnexion itinérante
</dt> <dd>

Un utilisateur peut se déconnecter manuellement d’une session Bureau à distance sans fermer la session. L’utilisateur est automatiquement reconnecté à sa session déconnectée lorsqu’il se reconnecte au système à partir du même appareil ou d’un autre appareil. Lorsque la session d’un utilisateur se termine de façon inattendue par une défaillance du réseau ou du client, l’utilisateur est déconnecté, mais pas déconnecté.

</dd> <dt>

<span id="Clipboard_mapping"></span><span id="clipboard_mapping"></span><span id="CLIPBOARD_MAPPING"></span>Mappage du presse-papiers
</dt> <dd>

Les utilisateurs peuvent supprimer, copier et coller du texte et des graphiques entre les applications qui s’exécutent sur l’ordinateur local et celles qui s’exécutent dans une session Bureau à distance, et entre les sessions.

</dd> <dt>

<span id="Print_redirection"></span><span id="print_redirection"></span><span id="PRINT_REDIRECTION"></span>Redirection d’impression
</dt> <dd>

Les applications qui s’exécutent dans une session Bureau à distance peuvent imprimer sur une imprimante connectée à l’appareil client.

</dd> <dt>

<span id="Virtual_channels"></span><span id="virtual_channels"></span><span id="VIRTUAL_CHANNELS"></span>Canaux virtuels
</dt> <dd>

Grâce à l’architecture de canal virtuel RDP, les applications existantes peuvent être augmentées et de nouvelles applications peuvent être développées pour ajouter des fonctionnalités qui nécessitent des communications entre le périphérique client et une application s’exécutant dans une session Bureau à distance.

</dd> <dt>

<span id="Remote_control"></span><span id="remote_control"></span><span id="REMOTE_CONTROL"></span>Contrôle à distance
</dt> <dd>

Le personnel de support informatique peut afficher et contrôler une session Bureau à distance. Partager des entrées et afficher des graphiques entre deux sessions Bureau à distance permet à une personne du support de diagnostiquer et de résoudre les problèmes à distance.

</dd> <dt>

<span id="Network_load_balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>Équilibrage de la charge réseau
</dt> <dd>

RDP tire parti de l’équilibrage de la charge réseau (NLB), le cas échéant.

</dd> </dl>

En outre, le protocole RDP contient les fonctionnalités suivantes :

-   Prise en charge des couleurs 24 bits.
-   Amélioration des performances par rapport aux connexions d’accès à distance à faible vitesse via une bande passante réduite.
-   Authentification par carte à puce via Services Bureau à distance.
-   Connexion au clavier. possibilité de diriger des combinaisons de touches Windows spéciales, en mode plein écran, sur l’ordinateur local ou sur un ordinateur distant.
-   Le son, le lecteur, le port et la redirection d’imprimante réseau. Les sons qui se produisent sur l’ordinateur distant peuvent être audibles sur l’ordinateur client qui exécute le client RDC, et les lecteurs clients locaux sont visibles par la session Bureau à distance.

 

 