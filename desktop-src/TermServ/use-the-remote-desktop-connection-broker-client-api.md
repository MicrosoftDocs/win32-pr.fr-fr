---
title: Utilisation de l’API cliente Connexion Bureau à distance Broker
description: L’API cliente Connexion Bureau à distance Broker permet aux fournisseurs de protocoles tiers de tirer parti du répartiteur de connexions pour accélérer la gestion des connexions qui utilisent leur protocole pour se connecter à des ordinateurs virtuels ou à des serveurs Bureau à distance dans une batterie de serveurs.
ms.assetid: 05C2D6CA-C9C5-4783-B196-6A02918046EF
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c931245870cfb72aed54e5aaff24e12d03ddf9e7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316187"
---
# <a name="how-to-use-the-remote-desktop-connection-broker-client-api"></a>Utilisation de l’API cliente Connexion Bureau à distance Broker

L’API cliente Connexion Bureau à distance Broker permet aux fournisseurs de protocoles tiers de tirer parti du répartiteur de connexions pour accélérer la gestion des connexions qui utilisent leur protocole pour se connecter à des ordinateurs virtuels ou à des serveurs Bureau à distance dans une batterie de serveurs.

## <a name="instructions"></a>Instructions

### <a name="step-1-obtain-the-iconnectionbrokerclient-interface"></a>Étape 1 : obtenir l’interface IConnectionBrokerClient

Lorsque votre application ou fournisseur de protocole est initialisé, procédez comme suit.

1.  Appelez la fonction [**CBCreateClientInstance**](cbcreateclientinstance.md) pour obtenir l’interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) .
2.  Conservez l’interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) tant que vous en avez besoin.
3.  Lorsque l’interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) n’est plus nécessaire, appelez la méthode [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) .

### <a name="step-2-request-the-target-information"></a>Étape 2 : demander les informations sur la cible

Lorsque votre fournisseur de protocole reçoit une demande de connexion entrante, procédez comme suit pour appeler la méthode [**IConnectionBrokerClient :: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) . Cette méthode obtient, à partir du répartiteur de connexions, le serveur approprié vers lequel rediriger la connexion.

1.  Créez un événement qui peut être signalé à l’aide de [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa), ou d’une fonction similaire, à utiliser pour le paramètre *hStatusEvent* .
2.  Allouez de la mémoire pour les paramètres *pTargetInfo* et *pResult* . Ces blocs de mémoire doivent rester en place jusqu’à ce que l’intégralité de la séquence soit terminée.
3.  Renseignez une structure d' [**\_ \_ informations de connexion CB**](cb-connection-info.md) qui contient toutes les informations relatives à la connexion entrante.
4.  Appelez la méthode [**GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) , en passant tous les paramètres requis. Il s’agit d’une méthode asynchrone qui retourne une instance de l’interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
5.  Attendez que l’événement *hStatusEvent* soit défini.
6.  Chaque fois que l’événement *hStatusEvent* est défini, appelez la méthode [**IConnectionBrokerRequest :: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) pour déterminer l’état de la demande.
7.  Lorsque [**CheckStatus**](iconnectionbrokerrequest-checkstatus.md) retourne **la \_ demande d’État CB \_ \_ terminée**, les paramètres *pTargetInfo* et *pResult* contiennent leurs informations. Vous pouvez quitter la boucle d’attente, car le paramètre *hStatusEvent* ne sera plus utilisé.
8.  Utilisez les informations de la structure d’informations de la [**\_ cible \_ CB**](cb-target-info.md) représentée par le paramètre *pTargetInfo* pour déterminer où rediriger la connexion entrante.
9.  Libérez l’interface [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) .
10. Fermez le handle d’événement *hStatusEvent* ou réutilisez-le pour les demandes de connexion suivantes.

 

 