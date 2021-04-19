---
description: L’objectif de ce guide est d’aider les utilisateurs à résoudre les problèmes rencontrés lors de l’utilisation des API de découverte WSDAPI, lors de la création d’un hôte ou d’un proxy d’appareil WSDAPI, ou lors de l’utilisation de fonctions du système d’exploitation (telles que la découverte des fonctions ou l’Explorateur réseau) qui reposent sur WSDAPI.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: Guide de résolution des problèmes WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c28e9a1fe4cc5b24b386cfb88e39276edc14cb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516979"
---
# <a name="wsdapi-troubleshooting-guide"></a>Guide de résolution des problèmes WSDAPI

L’objectif de ce guide est d’aider les utilisateurs à résoudre les problèmes rencontrés lors de l’utilisation des API de découverte WSDAPI, lors de la création d’un hôte ou d’un proxy d’appareil WSDAPI, ou lors de l’utilisation de fonctions du système d’exploitation (telles que la [découverte des fonctions](/previous-versions/windows/desktop/fundisc/fd-portal) ou l’Explorateur réseau) qui reposent sur wsdapi. L’objectif principal est de vous aider à résoudre les problèmes lorsqu’un client et un hôte ne peuvent pas se voir sur le réseau.

Pour les utilisateurs de WSDAPI, ce guide contient des informations qui vous aideront à résoudre correctement un proxy d’appareil (à l’aide de [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)), un fournisseur de détection (à l’aide de [**WSDCreateDiscoveryProvider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)) ou un serveur de publication de découverte (à l’aide de [**WSDCreateDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)).

Ce guide part du principe que le client et l’hôte peuvent interagir correctement avec WSDAPI dans un environnement contrôlé. En conséquence, ce guide n’a pas pour but de vous aider à résoudre les problèmes liés aux piles DPWS susceptibles de générer des messages WS incorrects. Pour plus d’informations sur l’interopérabilité des tests avec WSDAPI, consultez l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) dans le kit de pilotes Windows (WDK).

Avant de commencer à dépanner votre application, vous devez vous familiariser avec les [modèles de message d’échange de métadonnées et de découverte](discovery-and-metadata-exchange-message-patterns.md).

Ce guide contient les sections suivantes.

-   [Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
-   [Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
