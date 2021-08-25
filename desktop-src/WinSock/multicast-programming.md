---
description: la programmation de la multidiffusion est activée par le biais de Windows sockets.
ms.assetid: f729945b-b469-4baf-ac06-2431ee2d0e71
title: Programmation de la multidiffusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0582f9d03cd5614bbe284eb81cdcb40bea8233627564ec2d3603de11fb663e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858159"
---
# <a name="multicast-programming"></a>Programmation de la multidiffusion

la programmation de la multidiffusion est activée par le biais de Windows sockets. Windows Les sockets activent les versions 1 (MLDv1) et 2 (MLDv2) de la détection d’écouteur multidiffusion sur IPv6 et les versions 2 (IGMPv2) et 3 (IGMPv3) par le biais de l’utilisation d’options de socket ou d’IOCTL. cette section décrit l’implémentation de Windows, explique comment activer la programmation multidiffusion à l’aide de Windows sockets et fournit des exemples de programmation pour illustrer son utilisation.

La deuxième version d’IGMP, ci-dessus appelée IGMPv2, permet aux hôtes de joindre et de conserver les groupes de multidiffusion identifiés par une adresse de multidiffusion IPv4 sur une interface réseau spécifique. Windows Sockets permet à une application de joindre et de conserver ces groupes sur des sockets spécifiques. Toutefois, l’inconvénient de IGMPv2, c’est que toute adresse source IPv4 jointe au groupe IGMPv2 peut transmettre à tous les membres, saturer le groupe et le rendre inutilisable pour les transmissions qui nécessitent une source principale, telle qu’une station de radio Internet. Le problème avec IGMPv2 est qu’il ne peut pas choisir de manière sélective une seule adresse source IPv4 (ou même quelques sources), et son incapacité à bloquer les expéditeurs (tels que les pirates ou les attaques par déni de service) pour un groupe de multidiffusion donné. IGMPv3 répond à ces lacunes.

avec Windows sockets et IGMPv3, les applications peuvent sélectionner une paire d’adresses source IPv4 de multidiffusion et de groupe de multidiffusion. en outre, Windows sockets permet aux développeurs d’autoriser de manière sélective d’autres diffuseurs dans une paire source/groupe donnée, ou permet aux applications de bloquer des diffuseurs spécifiques. IGMPv3 est pris en charge sur Windows Vista et versions ultérieures.

La première version de MLD sur IPv6, appelée MLDv1, est très similaire à IGMPv2 et subit les mêmes limitations. MLDv1 permet aux hôtes de joindre et de conserver les groupes de multidiffusion identifiés par une adresse de multidiffusion IPv6 sur une interface réseau spécifique. Windows Sockets permet à une application de joindre et de conserver ces groupes sur des sockets spécifiques. Toutefois, toute adresse source IPv6 jointe au groupe MLDv1 peut transmettre à tous les membres, saturer le groupe et la rendre inutilisable pour les transmissions qui nécessitent une source principale. Le problème avec MLDv1 est qu’il ne peut pas choisir de manière sélective une seule adresse source IPv6 (ou même quelques sources), et son incapacité à bloquer les expéditeurs (tels que les auteurs de radiodiffuseurs ou de déni de service) pour un groupe de multidiffusion donné. MLDv2 répond à ces lacunes.

avec Windows sockets et MLDv2, les applications peuvent sélectionner une adresse source IPv6 de multidiffusion et une paire de groupes de multidiffusion. en outre, Windows sockets permet aux développeurs d’autoriser de manière sélective d’autres diffuseurs dans une paire source/groupe donnée, ou permet aux applications de bloquer des diffuseurs spécifiques. MLDv2 est pris en charge sur Windows Vista et versions ultérieures.

Un programmeur d’applications peut prendre deux approches lors du développement d’applications de multidiffusion dans Windows. La première approche est basée sur les modifications ; les sources de multidiffusion sont ajoutées ou supprimées à l’aide des options de socket, même au cours de la transmission, selon les besoins. La deuxième approche est basée sur l’état final ; les adresses source et toutes les adresses incluses/exclues sont spécifiées avec une IOCTL. Chaque approche est une pratique de multidiffusion valide, mais les développeurs peuvent trouver à l’aide des options de socket et de l’approche basée sur les modifications plus intuitive et flexible.

Cette section contient les pages suivantes : 

| Titre de la page                                                                             | Description                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MLD et IGMP à l’aide de sockets Windows](igmp-and-windows-sockets.md)                     | énumère les options de socket de multidiffusion pouvant être utilisées dans la programmation de Windows sockets, à l’aide d’une approche de programmation basée sur les modifications. Définit deux catégories d’applications de multidiffusion. |
| [Comportement des options de socket de multidiffusion](multicast-socket-option-behavior.md)               | Fournit un tableau complet pour expliquer les implications et les exigences liées à l’appel d’options de socket de multidiffusion dans un ordre particulier.                                                  |
| [Exemple de programmation de multidiffusion](multicast-programming-sample.md)                       | L’extrait de code de programmation illustrant l’utilisation des options de socket pour activer les applications de multidiffusion dans Windows.                                                                        |
| [Programmation de la multidiffusion basée sur l’état final](final-state-based-multicast-programming.md) | explique l’approche à l’état final et comment utiliser des ioctl pour la programmation de la multidiffusion avec Windows sockets.                                                                               |
| [Portage d’applications de diffusion vers IPv6](porting-broadcast-applications-to-ipv6.md)   | Fournit des instructions pour le portage d’applications de diffusion IPv4 vers la multidiffusion IPv6.                                                                                                     |



 

 

 



