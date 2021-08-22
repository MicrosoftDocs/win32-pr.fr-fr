---
description: Windows Les sockets activent la détection d’écouteur multidiffusion (MLD) sur IPv6 et le protocole IGMP (Internet Group Management Protocol) sur IPv4 pour les applications de multidiffusion par le biais de l’utilisation des options de socket et des ioctl.
ms.assetid: a5de4273-e86e-4f13-b068-256cb38706d4
title: MLD et IGMP à l’aide de sockets Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2c550cf2c1463f5b646efc286c05010274d3cb44e13b9559302452bccb81c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051647"
---
# <a name="mld-and-igmp-using-windows-sockets"></a>MLD et IGMP à l’aide de sockets Windows

Windows Les sockets activent la détection d’écouteur multidiffusion (MLD) sur IPv6 et le protocole IGMP (Internet Group Management Protocol) sur IPv4 pour les applications de multidiffusion par le biais de l’utilisation des options de socket et des ioctl. Cette page décrit les options de socket qui permettent la programmation de la multidiffusion et décrit comment elles sont utilisées. Pour obtenir la définition de chaque option de socket, consultez la page [options de socket](socket-options.md) .

Pour plus d’informations sur l’utilisation d’IOCTL pour la programmation de multidiffusion, consultez programmation de la [multidiffusion basée sur l’état final](final-state-based-multicast-programming.md) plus loin dans cette section.

sur Windows Vista et versions ultérieures, un ensemble d’options de socket est disponible pour la programmation de multidiffusion qui prend en charge les adresses IPv6 et IPv4. Ces options de socket sont indépendantes des adresses IP et peuvent être utilisées sur les protocoles IPv6 et IPv4. Sur IPv6, ces options de socket utilisent MLDv2. Sur IPv4, ces options de socket utilisent IGMPv3. ces options IP agnostiques sont les options de socket préférées pour la programmation multidiffusion sur Windows Vista et versions ultérieures. Windows Sockets utilise les options de socket suivantes : 

| Option de socket               | Type d’argument                                            |
|-----------------------------|----------------------------------------------------------|
| \_source de bloc MCAST \_        | [**Groupe \_ Structure \_ req source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| \_groupe de jointure MCAST \_          | [**Groupe \_ Structure REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| \_ \_ groupe source MCAST \_ join  | [**Groupe \_ Structure \_ req source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| MCAST \_ - \_ groupe de sortie         | [**Groupe \_ Structure REQ**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_req)                |
| MCAST- \_ abandonner le \_ \_ groupe source | [**Groupe \_ Structure \_ req source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |
| \_source de déblocage MCAST \_      | [**Groupe \_ Structure \_ req source**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_source_req) |



 

Un ensemble d’options de socket est disponible pour la programmation de multidiffusion qui prend uniquement en charge les adresses IPv6. Ces options de socket utilisent MLDv1 ou MLDv2. La version de MLD utilisée dépend de la version de Windows. MLDv2 est pris en charge sur Windows Vista et versions ultérieures. Windows Sockets utilise les options de socket suivantes : 

| Option de socket          | Type d’argument                             |
|------------------------|-------------------------------------------|
| \_Ajouter une \_ appartenance IPv6  | [**structure \_ mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |
| \_Adhésion à Drop IPv6 \_ | [**structure \_ mreq IPv6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ipv6_mreq) |



 

Un ensemble d’options de socket est disponible pour la programmation de multidiffusion qui prend en charge les adresses IPv4 uniquement. Ces options de socket utilisent IGMPv3 ou IGMPv2. La version de l’IGMP utilisé dépend de la version de Windows. IGMPv3 est pris en charge sur Windows Vista et versions ultérieures. Windows Sockets utilise les options de socket suivantes :

| Option de socket                | Type d’argument                                        |
|------------------------------|------------------------------------------------------|
| \_Ajout d' \_ un abonnement IP          | structure [**IP \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| appartenance à une source d’ajout d’adresses IP \_ \_ \_  | [**structure \_ \_ source mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_source de bloc IP \_            | [**structure \_ \_ source mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_appartenance IP Drop \_         | structure [**IP \_ mreq**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq)                |
| appartenance à la \_ source de suppression IP \_ \_ | [**structure \_ \_ source mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |
| \_source de déblocage IP \_          | [**structure \_ \_ source mreq IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_mreq_source) |



 

Lorsque le protocole IGMPv3 est disponible, les \_ options ajouter l’appartenance à la \_ source \_ , source de \_ bloc IP, appartenance à la source de \_ \_ suppression IP \_ \_ et \_ débloquer IP \_ sont gérées de manière plus efficace, car le routeur peut gérer le filtrage. Lorsque seul IGMPv2 est disponible, l’hôte doit gérer le filtrage.

Il existe deux catégories dans lesquelles la plupart des applications sont susceptibles de tomber en cause : n’importe quelle source et source contrôlée.

-   Toutes les applications **source** acceptent toutes les sources par défaut, ce qui permet aux sources individuelles d’être désactivées en fonction des besoins. Un exemple d’application n’appartenant à aucune source est un appel de vidéoconférence qui permet à tous les destinataires de participer.
-   Les applications à **source contrôlée** limitent les sources à une liste donnée, telle qu’une station de radio Internet, ou la diffusion d’un événement notable. Le processus d’utilisation des options de socket est légèrement différent pour chacun.

sur Windows Vista et versions ultérieures, les étapes suivantes s’appliquent aux applications n’importe quelle source :

- Utilisez **le \_ \_ groupe de jonction MCAST** pour joindre un groupe.  
- Utilisez **la \_ \_ source de bloc MCAST** pour désactiver une source donnée, si nécessaire.  
- Utilisez **la \_ \_ source de déblocage MCAST** pour réactiver une source bloquée, si nécessaire.  
- Utilisez **MCAST \_ Leave \_ Group** pour sortir le groupe.  

sur Windows Vista et versions ultérieures, les étapes suivantes s’appliquent aux applications à source contrôlée :

- Utilisez **le \_ \_ \_ groupe source MCAST Join** pour joindre chaque paire groupe/source.  
- Utilisez **MCAST \_ Leave \_ source \_ Group** pour conserver chaque groupe/source, ou utilisez **MCAST \_ Leave \_ Group** pour conserver toutes les sources, si la même adresse de groupe est utilisée par toutes les sources.  

Les étapes suivantes s’appliquent aux applications n’importe quelle source :

- Utilisez **IP \_ Add \_ membership** pour rejoindre un groupe (**IPv6 \_ Add \_ membership** for IPv6).  
- Utilisez **la \_ \_ source de bloc IP** pour désactiver une source donnée, si nécessaire.  
- Utilisez **la \_ \_ source de déblocage IP** pour réactiver une source bloquée, si nécessaire.  
- Utilisez **l' \_ \_ appartenance à Drop IP** pour conserver le groupe (**\_ \_ adhésion IPv6 Drop** pour IPv6).  

Les étapes suivantes s’appliquent aux applications à source contrôlée :

- Utilisez **l’adresse IP \_ Ajouter une \_ \_ appartenance** à une source pour joindre chaque paire groupe/source.  
- Utilisez **l' \_ \_ \_ appartenance IP Drop source** pour conserver chaque groupe/source, ou utilisez l' **\_ \_ appartenance IP Drop** pour conserver toutes les sources, si la même adresse de groupe est utilisée par toutes les sources.  

L’ordre dans lequel ces options de socket sont définies est associé à des règles. Pour obtenir des informations et des informations de dépannage sur les options de socket de multidiffusion, consultez comportement de l' [option de socket de multidiffusion](multicast-socket-option-behavior.md).
