---
title: Sélection d’une séquence de protocole
description: Une séquence de protocole est la langue utilisée par un système d’exploitation réseau pour communiquer sur le réseau à d’autres ordinateurs.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029662"
---
# <a name="selecting-a-protocol-sequence"></a>Sélection d’une séquence de protocole

Une séquence de protocole est la langue utilisée par un système d’exploitation réseau pour communiquer sur le réseau à d’autres ordinateurs. Dans des conditions plus spécifiques, les applications RPC doivent spécifier une chaîne qui représente une combinaison d’un protocole RPC, d’un protocole de transport et d’un protocole réseau.

Microsoft RPC prend en charge trois protocoles RPC :

-   Protocole NCACN (Network Computing Architecture connexion)
-   Protocole NCADG (Network Computing Architecture Datagram Protocol)
-   Appel de procédure distante locale de l’architecture réseau informatique (NCALRPC)

Les applications RPC peuvent utiliser le protocole NCALRPC pour appeler des procédures proposées par les programmes serveur s’exécutant sur le même ordinateur que celui sur lequel le programme client s’exécute. C’est, de loin, la méthode la plus efficace pour appeler des fonctionnalités dans un processus différent sur le même ordinateur.

Les protocoles de transport et de réseau utilisés par votre application dépendent des protocoles pris en charge par le réseau. De nombreux réseaux actuels, y compris Internet, prennent en charge TCP/IP. Les autres protocoles de transport et de réseau courants sont IPX/SPX, NetBIOS et le DSP AppleTalk. Microsoft RPC prend en charge ces protocoles de transport et de réseau. Pour obtenir une liste complète, consultez [constantes de séquence de protocole](protocol-sequence-constants.md).

Lorsque votre application utilise des handles de liaison automatiques, elle n’a pas besoin de spécifier la séquence de protocole. Si elle utilise des handles implicites ou explicites, elle doit obtenir ou spécifier la séquence de protocole. Chaque système distribué doit examiner l’environnement dans lequel il sera déployé pour déterminer la séquence de protocole la mieux adaptée à cet environnement.

Toutes les séquences de protocole ont des fonctionnalités équivalentes. Les développeurs doivent vérifier que la séquence de protocole choisie prend en charge les fonctionnalités requises. En général, **Ncalrpc** pour les communications locales et **ncacn \_ IP \_ TCP** ou **ncacn \_ http** pour les communications à distance sont recommandés. ils fonctionnent dans tous les environnements, ils offrent des performances optimales et prennent en charge toutes les fonctionnalités nécessaires, meilleures pratiques.

Les clients peuvent également spécifier les informations de séquence de protocole qu’ils obtiennent à partir de Active Directory, le registre, les variables d’environnement créées et initialisées par le programme d’installation, les fichiers de configuration spécifiques à l’application ou des chaînes littérales dans le code source du programme.

Une fois que votre programme client dispose d’une chaîne de séquence de protocole valide, il peut transmettre ces informations aux fonctions [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) et [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour créer le handle de liaison.

 

 




