---
title: Réception des notifications de modifications
description: De nombreux clients peuvent simultanément mettre à jour la table de routage, et les clients doivent être avertis lorsque des modifications sont apportées aux informations de routage.
ms.assetid: d42e16e2-32b2-4178-967b-e937730b3cca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6eddc92404acb921b31bab22736561cbbc83e4c1c641da80a8ff95352e52f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788709"
---
# <a name="receiving-notification-of-changes"></a>Réception des notifications de modifications

De nombreux clients peuvent simultanément mettre à jour la table de routage, et les clients doivent être avertis lorsque des modifications sont apportées aux informations de routage. Par exemple, un client qui n’est pas averti des modifications apportées à la table de routage par un autre client peut annoncer des informations d’itinéraire obsolètes. Cela peut empêcher les clients de programmation de s’inscrire auprès du gestionnaire de tables de routage pour être informé des modifications apportées à la table de routage. Le gestionnaire de table de routage envoie des notifications de modifications à tous les clients qui s’inscrivent pour les recevoir.

La notification de modification s’applique uniquement aux destinations. Il n’existe aucun moyen d’interroger le gestionnaire de table de routage à la recherche de modifications apportées à un itinéraire particulier.

Lorsqu’une modification est apportée à l’un des itinéraires vers une destination, le gestionnaire de tables de routage envoie une notification indiquant qu’une modification s’est produite. Cette notification est envoyée uniquement aux clients qui se sont inscrits auprès du gestionnaire de tables de routage pour le type de modification qui s’est produit. Toutes les modifications apportées aux informations de routage dans le gestionnaire de tables de routage se produisent dans une ou plusieurs vues, et les messages de notification de modification peuvent être demandés dans n’importe quel sous-ensemble de vues prises en charge.

Il existe actuellement trois types de notifications de modifications pour lesquelles un client peut s’inscrire :

-   Notification de toute modification apportée aux itinéraires pour la destination. Cette demande est effectuée à l’aide de l' \_ indicateur de modification de \_ type \_ tout.
-   Notification si le meilleur itinéraire vers la destination change, ou l’une des informations suivantes pour les meilleures modifications de routage actuelles :

    -   Préférence
    -   Tronçons suivants
    -   Indicateurs de route

    Cette demande est effectuée à l’aide \_ du \_ meilleur indicateur de type de modification RTM \_ .

-   Notification de toutes les modifications du type RTM de type RTM \_ \_ \_ , à l’exception des modifications apportées aux indicateurs de non-transfert dans le meilleur itinéraire. Par exemple, le gestionnaire de routeur attend les modifications de ce type dans la vue de monodiffusion et met à jour les informations dans le redirecteur de monodiffusion. Cette demande est effectuée à l’aide de l' \_ indicateur de transfert de type de modification RTM \_ \_ .

Les demandes de notification des modifications peuvent également être limitées à un sous-ensemble de destinations en s’inscrivant pour les notifications de modifications uniquement aux destinations « marquées ». Le client peut marquer une destination pour la notification de modification en appelant [**RtmMarkDestForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmmarkdestforchangenotification).

Lorsqu’une modification se produit, le gestionnaire de tables de routage vérifie s’il existe des clients qui doivent être avertis de cette modification. Un client doit être averti d’une modification si toutes les conditions suivantes sont remplies :

-   Le type de modification qui s’est produit est un type pour lequel le client s’est inscrit pour la notification
-   Les modifications apportées à une destination marquée par le client ont été effectuées ou n’importe quelle destination, si le client a demandé des modifications pour toutes les destinations
-   Le client a demandé une notification de modification pour la vue dans laquelle cette modification s’est produite

Si la modification remplit tous les critères ci-dessus, la modification est mise en cache et le client est averti.

La notification ne spécifie pas les modifications réelles, mais uniquement si elles se sont produites. Le client doit récupérer les modifications en appelant [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) à l’aide du handle de notification obtenu à partir d’un appel précédent à [**RtmRegisterForChangeNotification**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterforchangenotification).

 

 




