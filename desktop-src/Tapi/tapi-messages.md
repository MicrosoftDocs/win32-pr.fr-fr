---
description: Les messages sont utilisés pour notifier l’application d’événements asynchrones. Tous ces messages sont envoyés à l’application via le mécanisme de notification de message que l’application a spécifiée dans lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Messages TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd0a73a5ed845901d3cbe937a366a357c149541e8973a423310345dc241b92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002727"
---
# <a name="tapi-messages"></a>Messages TAPI

Les messages sont utilisés pour notifier l’application d’événements asynchrones. Tous ces messages sont envoyés à l’application via le mécanisme de notification de message que l’application a spécifiée dans [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).

Le message contient toujours un handle vers l’objet approprié (téléphone, ligne ou appel), que l’application peut utiliser pour déterminer le type de message.

Certains messages sont utilisés pour notifier l’application d’une modification de l’état d’un objet. Ces messages fournissent le descripteur d’objet et donnent une indication sur l’élément d’état modifié. L’application peut appeler la fonction « obtenir l’État » appropriée de l’objet pour obtenir l’état complet de l’objet.

Lorsqu’un événement se produit, les messages peuvent être envoyés à zéro, une ou plusieurs applications. Les applications cibles pour un message sont déterminées par différents facteurs, notamment la signification du message, le privilège de l’application à l’objet, si l’application a initié ou non la demande pour laquelle le message est un résultat direct, et le masquage de message défini par l’application. Notez les points suivants sur les messages :

-   Les messages de réponse asynchrones sont envoyés à l’application à l’origine de la demande et ne peuvent pas être masqués.
-   Les messages qui signalent l’achèvement de la génération de chiffres ou de tonalités, ou la collecte de chiffres, sont envoyés uniquement à l’application qui a demandé la génération de chiffres ou de tonalités.
-   Les messages qui indiquent des changements d’état de ligne ou d’adresse sont envoyés à toutes les applications qui ont ouvert la ligne, tant que le message a été activé par le biais de [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).
-   Les messages qui indiquent l’état de l’appel et les modifications des informations d’appel sont envoyés à toutes les applications qui ont un handle vers l’appel.
-   Les messages signalant une détection de chiffres, une détection de tonalité ou une détection de type de média sont envoyés aux applications qui ont demandé la surveillance de cet événement.

Cette section contient des informations de référence sur les messages TAPI suivants :

-   [Messages de téléphonie assistés](assisted-telephony-messages.md)
-   [Messages du centre d’appels](call-center-messages.md)
-   [Messages d’erreur mis en forme](formatted-error-messages.md)
-   [Messages du périphérique de ligne](line-device-messages.md)
-   [Téléphone Messages de l’appareil](phone-device-messages.md)

 

 



