---
description: Cette section décrit les pratiques recommandées pour le portage d’une application de diffusion IPv6 vers les fonctionnalités de multidiffusion disponibles avec Windows Sockets.
ms.assetid: 12e491fd-650f-43b4-afa1-9f37b1c30240
title: Portage d’applications de diffusion vers IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7dce09db6822a6f9b0a61873ca6bbff5a256b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484920"
---
# <a name="porting-broadcast-applications-to-ipv6"></a>Portage d’applications de diffusion vers IPv6

Cette section décrit les pratiques recommandées pour le portage d’une application de diffusion IPv6 vers les fonctionnalités de multidiffusion disponibles avec Windows Sockets.

## <a name="comparing-ipv4-to-ipv6"></a>Comparaison de IPv4 et IPv6

La considération la plus notable lors de la préparation du Portage d’une application de diffusion IPv4 vers IPv6 est la suivante : IPv6 n’a aucun concept de diffusion implémenté. Au lieu de cela, IPv6 utilise la multidiffusion.

La multidiffusion pour IPv6 peut émuler les fonctionnalités de diffusion traditionnelles disponibles dans IPv4. La définition de l’option [IPv6 \_ ajouter \_ un](ipproto-ipv6-socket-options.md) socket d’appartenance avec l’adresse IPv6 définie sur l’adresse de l’étendue lien-local de l’ensemble des nœuds (FF02 :: 1) équivaut à diffuser sur les adresses de diffusion IPv4 à l’aide de l’option de socket de [ \_ diffusion so](socket-options.md) . Cette adresse est parfois appelée *groupe de multidiffusion tous les nœuds*. Pour les applications qui veulent simplement une émulation de diffusion pour IPv6, cette approche est fonctionnellement équivalente. Toutefois, il existe une différence notable avec IPv6 : les multidiffusions sur l’adresse du groupe de multidiffusion tous les nœuds ne sont pas reçues par défaut (les diffusions IPv4 sont reçues par défaut). Les programmeurs d’applications doivent utiliser \_ l' \_ option IPv6 ajouter un socket d’appartenance pour activer la réception par multidiffusion à partir de n’importe quelle source, y compris l’adresse du groupe de multidiffusion tous les nœuds.

> [!Note]  
> Dans IPv6, la sélection de l’interface est spécifiée dans la structure d’arguments passée à l’option de socket multidiffusion ou IOCTL.

 

Mais pour des transmissions plus riches, plus robustes, plus sélectives et plus faciles à gérer sur plusieurs hôtes, les développeurs d’applications doivent envisager de passer à un modèle de multidiffusion.

## <a name="moving-to-multicast"></a>Passage à la multidiffusion

Avec la multidiffusion, les programmeurs d’applications peuvent choisir de manière sélective une paire source/groupe particulière, en activant un modèle de réception sélective. La découverte de l’écouteur de multidiffusion (MLD) sur IPv6 et la version 3 du protocole IGMPv3 (Internet Group Management Protocol) sur IPv4 prennent en charge la programmation de la multidiffusion. En outre, la multidiffusion permet aux applications de bloquer spécifiquement (ou débloquer) des expéditeurs dans un groupe, et de protéger les applications contre les diffuseurs non autorisés. Cette fonctionnalité est disponible pour IPv4 (requiert IGMPv3) et IPv6 (nécessite MLDv2).

Il existe deux principaux scénarios pour les programmeurs d’applications utilisant la multidiffusion : le portage d’applications de diffusion IPv4 (ou de multidiffusion) vers IPv6, et ceux qui créent de nouvelles applications de multidiffusion IPv6.

Pour le portage des applications existantes, vous pouvez passer à la multidiffusion IPv6 en utilisant les options de socket et les IOCTL.

-   L’utilisation des options de socket est une approche basée sur les modifications, qui permet aux développeurs de modifier les propriétés de socket en fonction des besoins (tels que le blocage ou le déblocage d’un expéditeur, l’ajout d’une nouvelle source, etc.). Cette approche est plus intuitive et l’approche recommandée. Pour plus d’informations sur l’approche basée sur les modifications de la programmation de multidiffusion, consultez [MLD et IGMP à l’aide de Windows Sockets](igmp-and-windows-sockets.md).
-   L’utilisation d’IOCTL est une approche basée sur l’état final, car elle permet aux développeurs de fournir un état de socket entièrement configuré, y compris des listes d’inclusion et d’exclusion, avec un appel. Pour plus d’informations sur l’approche basée sur l’état final, consultez programmation de la [multidiffusion basée sur l’état final](final-state-based-multicast-programming.md).

Pour les utilisateurs qui créent de nouvelles applications de multidiffusion IPv6, la pratique recommandée consiste à utiliser des options de socket plutôt que des ioctl.

Il existe une autre approche pour créer des applications de multidiffusion avec IPv6, et cela implique l’utilisation de la fonction [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) . Bien que l’utilisation de la fonction **WSAJoinLeaf** ne soit pas la pratique recommandée, il existe des situations qui peuvent en imposer l’utilisation. Par exemple, l’un des inconvénients de l’utilisation des options de socket sur Windows Server 2003 et versions antérieures est qu’elles sont spécifiques à la version IP. Sur ces versions antérieures de Windows, les différentes options de sockets doivent être pour IPv6 et IPv4. Sur Windows Vista et versions ultérieures, les nouvelles options de socket sont prises en charge et peuvent être utilisées avec IPv4 et IPv6. La fonction **WSAJoinLeaf** , en revanche, est dépendante de la version IP et du protocole, et il peut donc s’agir d’une approche utile pour créer une application qui doit fonctionner avec plusieurs versions d’IP sur Windows Server 2003 et versions antérieures. L’utilisation de la fonction **WSAJoinLeaf** peut être plus appropriée dans certaines situations où le agnostique protocole et IP-version est requis.

 

 



