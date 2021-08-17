---
title: Configuration système requise pour les applications RPC-Message Queuing
description: Pour utiliser le transport de mise en file d’attente de messages dans une application client/serveur RPC, le serveur et les ordinateurs clients doivent disposer de la plateforme du système d’exploitation appropriée et du logiciel Message Queuing installé.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46d9775e720c725ad3b0d06a0be0cf67aa438f739c6a0d1162f4940ac59e561e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924646"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a>Configuration système requise pour les applications RPC-Message Queuing

Pour utiliser le transport de mise en file d’attente de messages dans une application client/serveur RPC, le serveur et les ordinateurs clients doivent disposer de la plateforme du système d’exploitation appropriée et du logiciel Message Queuing installé.

La configuration requise pour les ordinateurs serveurs est la suivante :

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou version ultérieure.
-   SQL Server version 6,5 ou ultérieure.
-   Message Queuing contrôleur de Enterprise principal ou le contrôleur de Site principal.
-   DLL de transport RPC côté serveur (RpcMqSvr.dll).

La configuration requise pour les ordinateurs clients est la suivante :

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou version ultérieure.
-   Client Microsoft Message Queuing.
-   DLL de transport RPC côté client (RpcMqCl.dll).

Lorsque les composants MSMQ sont installés sur les ordinateurs clients et serveurs, les registres système sont automatiquement configurés pour inclure le protocole de transport [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq) Message-Queuing pour les appels de procédure distante.

Pour générer votre application RPC-MSMQ, vous devez disposer des éléments suivants :

-   Microsoft Windows Server 2003, Windows XP ou Windows 2000 ou version ultérieure
-   MIDL version 3.1.76 ou ultérieure.

 

 