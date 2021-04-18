---
description: Lorsqu’une application dispose d’un privilège de propriétaire pour une session de communication, l’application peut choisir de transmettre la propriété à une autre application.
ms.assetid: d6d188c9-9cbd-45af-93f0-b78850374919
title: Livraisons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343815e35f1fc331c57c4aa2d9d311697cab7022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516062"
---
# <a name="handoffs"></a>Livraisons

Lorsqu’une application dispose d’un [privilège](privilege-ovr.md) de propriétaire pour une session de communication, l’application peut choisir de transmettre la propriété à une autre application. L’opération de remise est normalement utilisée pour permettre la modification du type de média de l’appel. L’application dont la priorité est la plus élevée pour le nouveau type de média doit prendre et gérer l’appel. La modification du type de média se produit généralement pour l’une des raisons suivantes.

**Commande utilisateur :** Par le biais d’une interface utilisateur ou de messages de fenêtre, l’application apprend que l’utilisateur local souhaite modifier le type de média. Par exemple, l’utilisateur a indiqué à la nouvelle application cible (qui n’est pas encore un propriétaire) d’obtenir un appel vocal existant pour transmettre des données. L’application cible doit maintenant prendre le contrôle de l’appel. Dans ce cas, le propriétaire actuel constate que le nombre de propriétaires augmente, puis abandonne son contrôle de l’appel. L’utilisateur peut également indiquer au propriétaire actuel de l’appel de le remettre à une application capable de gérer le nouveau type de média.

**Modification du type de média :** Le fournisseur de services peut détecter une modification de type de média. Par exemple, l’application locale lit un message vocal enregistré à l’appelant. Pendant ce message, l’appelant décide spontanément de transmettre une tonalité d’appel de télécopie, et l’application locale peut répondre en conséquence en modifiant le type de média pour la télécopie et, si nécessaire, en transmettant l’appel à une application de télécopie. Cela peut également être fait pour une application de surveillance permettant d’activer la surveillance de type de média et, lorsque le type de support dans lequel elle est intéressée est détecté sur un appel, elle peut demander la propriété de l’appel. Ce mécanisme rend inutile que chaque application surveille chaque appel pour chaque type de média.

**Commande de partie distante :** Le tiers distant peut indiquer de manière interactive une modification des types de média lors d’un appel existant, par exemple si l’application locale surveille l’entrée DTMF par l’appelant distant. Grâce à cette analyse, l’appelant indique, par exemple, qu’une télécopie va être envoyée. Les autres méthodes permettant à l’appelant de contrôler les applications locales sont les commandes reçues sur d’autres connexions de données et les messages d’informations utilisateur de l’utilisateur RNIS.

Un transfert d’appel aura l’un des résultats suivants :

-   L’appel est donné à une autre application (réussite).
-   L’application de gestion est elle-même la cible (TARGETSELF).
-   Le transfert échoue (TARGETNOTFOUND).

Si l’application qui reçoit l’appel remis a déjà un handle d’appel à l’appel, cet ancien descripteur d’appel est utilisé. Dans le cas contraire, un nouveau descripteur d’appel est créé. Dans les deux cas, l’application finit par disposer des privilèges de propriétaire pour l’appel. Chaque fois que l’application de gestion des messages n’est pas la même que l’application cible, la cible est informée de la remise dans un message d’état de session comme si elle recevait un nouvel appel.

Si l’application propriétaire en cours est invitée à modifier les types de supports, elle le fait en distribuant l’appel à une application utilisée pour le type de média cible. Les deux types de transferts d’appel sont décrits dans [transferts dirigés](#directed-handoffs) et [transferts de type de média](#media-type-handoffs).

Les fournisseurs de services ne prennent pas tous en charge l’utilisation de cette opération.

**TAPI 2. x :** Consultez [**lineHandoff**](/windows/win32/api/tapi/nf-tapi-linehandoff), avec *lpszFileName* défini sur le nom de l’application pour un transfert direct ou un *dwMediaMode* défini sur un type de support pour un transfert indirect.

**TAPI 3. x :** Consultez [**ITBasicCallControl :: HandoffDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffdirect), [**ITBasicCallControl :: HandoffIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-handoffindirect).

## <a name="directed-handoffs"></a>Transferts dirigés

Une *remise dirigée* a lieu lorsque l’application cible est connue par son nom à l’application d’origine. Cette situation se produit, par exemple, parmi un ensemble d’applications écrites par le même fournisseur. L’utilisateur peut généralement configurer le contrôle des transferts dirigés. Avec une telle remise, l’appel est donné à l’application spécifiée s’il a ouvert la ligne sur laquelle l’appel existe. Le type de média spécifié au moment de l’ouverture de la ligne par l’application est ignoré. Un exemple courant est un appel vocal suivi d’une transmission de télécopie dans le même appel. La plupart du temps, le transfert dirigé est utilisé par les applications du même développeur, qui sont également liées par d’autres moyens.

La remise dirigée peut également être utilisée dans les versions futures dans le cadre du processus d’arbitrage de plusieurs applications en attente d’appels entrants du même type de média, avec la sélection de l’application pour gérer l’appel en fonction de la liaison de données ou de la détection de protocole de niveau supérieur plutôt que du type de média. Un exemple de son utilisation est une ligne de modem de données entrant avec des applications telles que la prise en charge à distance, le bulletin d’informations, l’accès réseau à distance et l’accès à la messagerie à distance, tous en attente d’appels simultanés.

## <a name="media-type-handoffs"></a>Transferts de type de média

Un *transfert de type de média* a lieu lorsqu’il existe un nouveau type de média ciblé, généralement lorsque l’application propriétaire détermine que le type de média nécessaire pour l’appel n’est pas présent ou est sur le point de changer.

Le processus d’un transfert dépendant du média peut être un processus de sondage si le bit de type de média inconnu est activé. Il incombe à l’application propriétaire de parcourir les types de médias pour trouver l’application dont la priorité est la plus élevée. L’interface TAPI effectue ce cycle uniquement sur l’appel entrant initial pour rechercher le premier propriétaire. Elle ne le fait pas pour une opération de remise. Dans le cas contraire, un transfert est quasiment le même que pour l’affectation initiale d’un appel à une application. La différence réside dans le fait qu’un seul type de média peut être défini pour un transfert indirect (type de média).

Étant donné qu’un seul bit de type de média peut être spécifié, l’appel est donné à l’application de priorité la plus élevée pour ce type de média. Toutefois, il est possible que plusieurs types de média soient pris en compte pour la remise. Dans ce cas, l’application de gestion doit spécifier la priorité la plus élevée des types de média possibles en tant que paramètre.

Si une application spécifie le bit inconnu lors d’un transfert de type média et que la remise échoue, cela signifie qu’une application inconnue capable d’effectuer la détermination du type de média n’est pas en cours d’exécution. L’application qui est en cours de transfert doit ensuite tenter de remettre l’appel à l’application dont la priorité est la plus élevée, inscrite pour le type de média supérieur suivant.

L’application réceptrice est désormais responsable de l’appel. Il sonde maintenant le type de média réel de l’appel. Si l’application peut gérer le type de média de l’appel, elle doit s’assurer qu’il s’agit de l’application dont la priorité est la plus élevée et inscrite pour ce type de média. Si c’est le cas, il conserve l’appel et le traite normalement. Si ce n’est pas le cas, il transmet l’appel à une autre application inscrite pour ce type de média.

Toutefois, si la sonde pour ce type de média échoue, l’application effectue une nouvelle tentative, en tentant les autres possibilités en mode Media. Il doit d’abord désactiver le bit de type de média actuel, puis essayer une autre remise avec un type différent.

Ce processus de détection et de remise continue, et les autres types de médias sont éliminés un par un. En cours de route, l’une des applications peut voir que le type de média qu’elle gère est sur l’appel et que la remise a réussi.

L’application doit ensuite définir le type de support approprié et effacer tous les autres bits de type média. Cela informe les autres applications intéressées du type de média correct. Ces autres applications reçoivent un message de notification d’événement indiquant que le type de média de l’appel a changé.

 

 
