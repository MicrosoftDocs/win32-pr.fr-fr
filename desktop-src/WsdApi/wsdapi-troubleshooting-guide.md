---
description: L’objectif de ce guide est d’aider les utilisateurs à résoudre les problèmes rencontrés lors de l’utilisation des API de découverte WSDAPI, lors de la création d’un hôte ou d’un proxy d’appareil WSDAPI, ou lors de l’utilisation de fonctions du système d’exploitation (telles que la découverte des fonctions ou l’Explorateur réseau) qui reposent sur WSDAPI.
ms.assetid: fc01fc66-627a-497f-98dd-613f5d85f6cb
title: Guide de résolution des problèmes WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a904b2bf4072721e6c0e9c01191aa1b3d5f55224b096434062b7aa8535fa5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860030"
---
# <a name="wsdapi-troubleshooting-guide"></a>Guide de résolution des problèmes WSDAPI

L’objectif de ce guide est d’aider les utilisateurs à résoudre les problèmes rencontrés lors de l’utilisation des API de découverte WSDAPI, lors de la création d’un hôte ou d’un proxy d’appareil WSDAPI, ou lors de l’utilisation de fonctions du système d’exploitation (telles que la [découverte des fonctions](/previous-versions/windows/desktop/fundisc/fd-portal) ou l’Explorateur réseau) qui reposent sur wsdapi. L’objectif principal est de vous aider à résoudre les problèmes lorsqu’un client et un hôte ne peuvent pas se voir sur le réseau.

Pour les utilisateurs de WSDAPI, ce guide contient des informations qui vous aideront à résoudre correctement un proxy d’appareil (à l’aide de [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)), un fournisseur de détection (à l’aide de [**WSDCreateDiscoveryProvider**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoveryprovider)) ou un serveur de publication de découverte (à l’aide de [**WSDCreateDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nf-wsddisco-wsdcreatediscoverypublisher)).

Ce guide part du principe que le client et l’hôte peuvent interagir correctement avec WSDAPI dans un environnement contrôlé. En conséquence, ce guide n’a pas pour but de vous aider à résoudre les problèmes liés aux piles DPWS susceptibles de générer des messages WS incorrects. pour plus d’informations sur l’interopérabilité des tests avec wsdapi, consultez l' [outil wsdapi Basic interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) dans le Kit de pilotes Windows (WDK).

avant de commencer à dépanner votre application, vous devez vous familiariser avec la [découverte et les métadonnées Exchange les modèles de Message](discovery-and-metadata-exchange-message-patterns.md).

Ce guide contient les sections suivantes.

-   [Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
-   [Procédures de diagnostic WSDAPI](wsdapi-diagnostic-procedures.md)
