---
description: Pour déterminer le type d’événement de l’appareil lors du traitement d’un \_ message WM DEVICECHANGE, examinez le paramètre wParam.
ms.assetid: 17078548-879d-4a11-a268-27d1f30180ab
title: Types d’événements d’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35ece6b810ba4d1310638bbfbdcdcaa7f67f79d8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114386"
---
# <a name="device-event-types"></a>Types d’événements d’appareil

Pour déterminer le type d’événement de l’appareil lors du traitement d’un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) , examinez le paramètre *wParam* . La valeur de *wParam* détermine la signification des données spécifiques à l’événement dans le paramètre *lParam* . En général, les données spécifiques à l’événement identifient l’appareil et fournissent des détails supplémentaires sur l’événement. Le format de ces données dépend du type d’appareil, mais les premiers octets ont toujours le même format que la structure [**\_ \_ HDR de diffusion dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) . Pour déterminer le format des données, vérifiez le membre **dbch \_ DeviceType** .

Le système diffuse un événement de périphérique de type [DBT \_ DEVICEARRIVAL](dbt-devicearrival.md) (autrement dit, un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) avec *wParam* défini sur DBT \_ DEVICEARRIVAL) chaque fois qu’un appareil a été inséré et qu’il est disponible pour utilisation. En règle générale, les applications vérifient le type d’appareil et commencent à utiliser l’appareil immédiatement si cela est approprié.

Le système diffuse un événement de périphérique [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) pour demander l’autorisation de supprimer un appareil. Pour déterminer si elle a besoin de l’appareil, une application peut afficher une boîte de dialogue pour inviter l’utilisateur à fournir des instructions. Si une application détermine qu’elle a besoin de l’appareil, elle peut refuser cette demande et annuler la suppression en retournant la requête de diffusion \_ \_ Deny. Si l’application n’a pas besoin de l’appareil, elle doit retourner la **valeur true**. Le système envoie immédiatement un message [DBT \_ DEVICEQUERYREMOVEFAILED](dbt-devicequeryremovefailed.md) si une application ou un pilote a annulé une demande précédente de suppression d’un appareil.

Le système diffuse un événement d’appareil [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) comme dernier avertissement avant la suppression d’un appareil. À ce stade, l’application ne peut pas annuler la suppression. par conséquent, si elle utilise l’appareil, elle doit préparer sa suppression pour éviter la perte de données. Cela est particulièrement important lors de la suppression d’une connexion réseau. L’application doit déterminer si l’un de ses fichiers ou canaux ouverts se trouve sur cette connexion. Pour ce faire, il compare l’identificateur de ressource réseau dans les données spécifiques à l’événement du message avec les identificateurs de ressource obtenus précédemment pour les fichiers et les canaux. Le système diffuse un événement d’appareil [DBT \_ DEVICEREMOVECOMPLETE](dbt-deviceremovecomplete.md) lorsqu’un appareil a été supprimé et n’est plus disponible.

Le système diffuse un événement de périphérique [DBT \_ QUERYCHANGECONFIG](dbt-querychangeconfig.md) pour demander l’autorisation de modifier la configuration actuelle (ancrer ou détacher). Toute application peut renvoyer la \_ requête \_ de diffusion Deny pour refuser la demande et annuler la modification. Si une application refuse la demande, le système envoie un message [DBT \_ CONFIGCHANGECANCELED](dbt-configchangecanceled.md) . Si la configuration actuelle a changé, en raison d’une station d’accueil ou d’une déconnexion, le système envoie un message [DBT \_ CONFIGCHANGED](dbt-configchanged.md) .

Le système diffuse un événement de périphérique [DBT \_ DEVICETYPESPECIFIC](dbt-devicetypespecific.md) chaque fois qu’un événement spécifique à l’appareil se produit.

Les pilotes peuvent créer leurs propres types d’événements personnalisés. Les événements personnalisés sont envoyés uniquement à l’application qui a été inscrite pour la notification d’événement d’appareil sur un appareil particulier et qui peuvent uniquement être initiés par des pilotes en mode noyau. Pour plus d’informations, consultez [DBT \_ CUSTOMEVENT](dbt-customevent.md).

 

 



