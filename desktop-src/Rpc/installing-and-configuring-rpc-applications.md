---
title: Installation et configuration des applications RPC
description: Lorsque le système d’exploitation Microsoft Windows est installé sur un serveur ou un client, le programme d’installation installe automatiquement les fichiers d’exécution RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Appel de procédure distante RPC, tâches, installation et configuration d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462466"
---
# <a name="installing-and-configuring-rpc-applications"></a>Installation et configuration des applications RPC

Lorsque le système d’exploitation Microsoft Windows est installé sur un serveur ou un client, le programme d’installation installe automatiquement les fichiers d’exécution RPC. Aucune autre installation RPC n’est requise. Toutefois, vous devez vous assurer que la version de Windows que vous installez prend en charge toutes les fonctionnalités utilisées dans votre application distribuée.

Lorsque vous utilisez une application RPC sur un système d’exploitation Windows 3. x ou Microsoft MS-DOS, vous devez copier les fichiers exécutables du runtime RPC sur les ordinateurs Windows 3. x ou MS-DOS qui utiliseront l’application. Le répertoire \\ mstools \\ RPC \_ RT16 sur le CD du kit de développement logiciel (SDK) de la plateforme contient une image disque de ces fichiers, ainsi qu’un programme d’installation pour installer les fichiers. Utilisez cette image disque pour créer un disque d’installation à distribuer avec votre application RPC. Vous pouvez également utiliser des applications clientes 16 bits ciblées vers MS-DOS ou Windows sur un système d’exploitation Windows 32 bits/64 bits. Toutefois, le programme d’installation de votre application doit installer les fichiers exécutables contenus dans cette image disque.

Lorsque vous générez une application RPC pour un client Macintosh, vous devez lier les fichiers nécessaires à l’application au moment de la génération. Aucune installation RPC supplémentaire n’est nécessaire.

Pour plus d’informations sur les fichiers redistribuables et les contrats de licence, consultez \\Redist.txt de licence \\ et \\ \\License.txt de licence sur le CD de Platform SDK.

Cette section contient des informations sur la configuration d’applications RPC sur une variété de plateformes matérielles et logicielles. Il présente la discussion dans les sections suivantes :

-   [Configuration du fournisseur de services de noms](configuring-the-name-service-provider.md)
-   [Informations de Registre](registry-information.md)
-   [Utilisation de RPC avec le proxy Winsock](using-rpc-with-winsock-proxy.md)
-   [Installation de SPX/IPX](spx-ipx-installation.md)
-   [Configuration du serveur de sécurité](configuring-the-security-server.md)

 

 




