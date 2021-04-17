---
description: Le service de composants en file d’attente COM+ améliore le modèle de programmation COM en fournissant un environnement dans lequel un composant peut être appelé de façon synchrone (en temps réel) ou asynchrone (en file d’attente).
ms.assetid: fd455679-b2b3-487f-8494-9ea296ce2c89
title: Architecture des composants en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a2f6e1012bd3c11a27a44214ee28e84d5bd404
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104561736"
---
# <a name="queued-components-architecture"></a>Architecture des composants en file d’attente

Le service de composants en file d’attente COM+ améliore le modèle de programmation COM en fournissant un environnement dans lequel un composant peut être appelé de façon synchrone (en temps réel) ou asynchrone (en file d’attente). Un composant n’a pas besoin de savoir s’il est utilisé dans un contexte en temps réel ou en file d’attente.

Les applications de messagerie sont similaires aux transactions par courrier électronique entre les programmes. Le demandeur envoie un message au serveur ; Lorsque le serveur s’y trouve, le message est traité. À l’instar de la messagerie électronique, un système de messagerie doit gérer les détails du réseau et s’assurer que le message est déplacé du client vers le serveur. Dans l’infrastructure des composants en file d’attente, Message Queuing en est responsable.

Le service COM+ Queued Components se compose des éléments suivants :

-   Enregistreur (pour le client ou le côté envoi)
-   Écouteur (pour le serveur ou le côté réception)
-   Player (pour le serveur ou le côté réception)

![Diagramme qui montre le chemin d’accès du client au serveur : client, enregistreur, file d’attente, écouteur, lecteur, serveur.](images/d732774b-1ca6-45ad-bce0-a95b0bfc3edb.png)

## <a name="the-recorder"></a>Enregistreur

Dans un scénario de composants en file d’attente standard, le client appelle un composant mis en file d’attente. L’appel est fait à l’enregistreur des composants en file d’attente, qui le place dans le cadre d’un message sur le serveur et le place dans une file d’attente. L’enregistreur marshale le contexte de sécurité du client dans le message et enregistre tous les appels de méthode du client. Dans son rôle en tant que proxy pour le composant serveur, l’enregistreur sélectionne les interfaces à partir des interfaces de mise en file d’attente dans le catalogue COM+.

Une représentation de l’enregistrement est envoyée à Message Queuing sous la forme d’un message à envoyer à un serveur. Lorsque le paramètre d’attribut de transaction du composant en file d’attente est obligatoire ou pris en charge, Message Queuing accepte la remise du message uniquement si la transaction côté client est validée et que la file d’attente Message Queuing est transactionnelle, ce qui correspond à la valeur par défaut normalement établie. Lorsque le paramètre d’attribut de transaction requiert New, Message Queuing peut accepter le message même si la transaction côté client est abandonnée. Pour plus d’informations sur les transactions, consultez [Message Queuing transactionnelles](transactional-message-queuing.md).

## <a name="the-listener"></a>L’écouteur

L’écouteur de composants en file d’attente récupère le message de la file d’attente et le transmet au lecteur des composants en file d’attente.

## <a name="the-player"></a>Le lecteur

Le lecteur démarshale le contexte de sécurité du client côté serveur, puis appelle le composant serveur et effectue les mêmes appels de méthode. Les appels de méthode ne sont pas lus par le joueur jusqu’à ce que le composant client se termine et que la transaction qui a enregistré la méthode appelle valids.

## <a name="the-message-mover"></a>Le message Mover

Le gestionnaire de messages des composants en file d’attente est un utilitaire qui déplace tous les messages d’échec Message Queuing d’une file d’attente vers une autre, afin qu’ils puissent être retentés. L’utilitaire de déplacement de messages est un objet Automation qui peut être appelé à l’aide d’un script VBScript. Pour plus d’informations, consultez [gestion des erreurs](handling-errors-in-queued-components.md).

 

 



