---
title: Vue d’ensemble des techniques de Change Tracking
description: Il existe plusieurs façons de faire en sorte que les mécanismes de suivi des modifications aient une portée différente pour le suivi des modifications qu’une application peut suivre les modifications apportées à un attribut unique d’un objet unique, à tous les objets d’un domaine, et ainsi de suite.
ms.assetid: 7359e851-61b7-420d-beb0-f7f33f79b007
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036a16362a7f27da47fc086d8758b28619f34d1475c7bb911050deb20c86f08d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025507"
---
# <a name="overview-of-change-tracking-techniques"></a>Vue d’ensemble des techniques de Change Tracking

Les mécanismes de suivi des modifications peuvent différer de plusieurs façons :

-   Étendue pour le suivi des modifications : une application peut suivre les modifications apportées à un attribut d’un seul objet, à tous les objets d’un domaine, et ainsi de suite. Si le mécanisme correspond aux spécifications de l’application, l’application reçoit au minimum des données non pertinentes, ce qui améliore les performances.
-   Actualité : une application est notifiée de chaque modification au fur et à mesure qu’elle se produit, ou peut être avertie de l’effet net des modifications sur une période de minutes ou d’heures.

    Le traitement des données moins rapidement peut s’avérer plus efficace, car plusieurs modifications peuvent être réduites en une seule. Par exemple, si un attribut change trois fois dans un intervalle d’une heure, une application notifiée des modifications accumulées sur une heure est notifiée d’une seule modification d’attribut, et non pas de trois.

    Lorsque vous réfléchissez à la chronologie, tenez compte de l’effet de la latence de réplication. Une mise à jour qui provient d’un contrôleur de domaine n’est pas répliquée instantanément sur un autre contrôleur de domaine. L’exigence d’une chronologie de suivi des modifications bien meilleure que la latence de réplication attendue n’offre souvent aucun avantage réel pour l’application.

-   Interrogation et notification : avec l’interrogation, une application envoie régulièrement une demande à un contrôleur de domaine pour recevoir les données de suivi des modifications. Avec notification, le contrôleur de domaine envoie les modifications à l’application uniquement lorsque des modifications se produisent.

    La surcharge de l’interrogation est évidente : l’application peut demander des données de suivi des modifications si rien ne s’est produit. La surcharge de la notification est plus subtile. Le serveur doit conserver les données relatives aux demandes de notification et doit consulter ces données pour décider s’il faut envoyer une notification. Cela peut ajouter de la surcharge aux demandes de mise à jour normales.

-   Exprimant la connaissance de l’application : persistante et temporaire : chaque mécanisme de suivi des modifications doit inclure une méthode pour le serveur contenant les données suivies pour comprendre l’état de la connaissance de l’application, afin que l’idée de « modification » soit bien définie. Par exemple, l’état de la connaissance de l’application peut être exprimé sous la forme « mis à jour avec toutes les modifications qui se sont produites sur le DC d avant le t t ». Un mécanisme basé sur cette façon d’exprimer l’état des connaissances d’une application permet à l’application d’obtenir efficacement des modifications qui se sont produites plus tard qu’une durée spécifiée.

    Si l’expression de la base de connaissances de l’application peut être persistante, c’est-à-dire stockée de façon plus importante, comme dans un fichier ou une base de données, le redémarrage de l’application est moins gourmand en ressources que s’il ne l’est pas. Dans l’exemple ci-dessus, l’expression de la connaissance de l’application peut être rendue persistante en enregistrant le DC d et l’heure t. Certains mécanismes de notification de modification n’autorisent pas la conservation de ces données. Le serveur et l’application doivent se synchroniser avec un autre mécanisme au démarrage de l’application. Cela nécessite beaucoup de ressources si plusieurs objets sont impliqués et peut impliquer une programmation complexe.

Utilisez les techniques suivantes pour suivre les modifications apportées à Active Directory Domain Services :

-   Utilisez le contrôle de notification de modification pour lancer une recherche asynchrone permanente pour les modifications qui correspondent à un filtre spécifié. Pour plus d’informations, consultez [notifications de modifications dans Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md).
-   Utilisez une recherche de synchronisation d’annuaires (DirSync) pour récupérer les modifications qui se sont produites depuis la recherche DirSync précédente. Pour plus d’informations, consultez [interrogation des modifications à l’aide du contrôle DirSync](polling-for-changes-using-the-dirsync-control.md).
-   Utilisez l’attribut USNChanged pour rechercher des objets qui ont été modifiés depuis la recherche précédente. Pour plus d’informations, consultez [interrogation des modifications à l’aide de USNChanged](polling-for-changes-using-usnchanged.md).

Le contrôle de notification de modification est conçu pour les applications ou services qui requièrent raisonnablement des notifications de modifications peu fréquentes. Par exemple, un service ou un programme qui stocke les données de configuration sur le serveur Active Directory et qui doivent être avertis rapidement en cas de modification. N’oubliez pas qu’il existe des limitations du contrôle de notification.

-   L’incitation des notifications dépend de la latence de réplication et de l’emplacement où la modification s’est produite. Vous pouvez être averti quand une modification est répliquée dans le réplica que vous analysez, mais que la modification a peut-être été apportée plus tôt sur un autre réplica.
-   Le contrôle est limité à l’analyse d’un seul objet ou des enfants immédiats d’un conteneur. Les applications qui doivent surveiller plusieurs conteneurs ou objets non liés peuvent inscrire jusqu’à cinq demandes de notification.
-   Si un trop grand nombre de clients écoutent des modifications fréquentes, cela aura un impact sur les performances du serveur. En général, les applications doivent limiter leur utilisation de ce contrôle pour des raisons de performances sur le serveur. Si vous n’avez pas besoin d’en savoir plus sur les modifications immédiatement, il peut être préférable d’interroger régulièrement les modifications au lieu d’utiliser la notification de modification.

Les techniques de recherche DirSync et USNChanged sont conçues pour les applications qui maintiennent la cohérence entre les données sur le serveur Active Directory et les données correspondantes dans d’autres stockages. Ces techniques sont utilisées par les applications qui interrogent régulièrement les modifications. La technique DirSync est basée sur un contrôle serveur LDAP que vous pouvez utiliser via des API ADSI ou LDAP. Les inconvénients du contrôle DirSync sont qu’il ne peut être utilisé que par un compte doté de privilèges élevés, tel qu’un administrateur de domaine. La liste suivante répertorie les limitations du contrôle DirSync :

-   Le contrôle DirSync ne peut être utilisé que par un compte doté de privilèges élevés, tel qu’un administrateur de domaine.
-   Le contrôle DirSync peut uniquement surveiller l’intégralité d’un contexte d’appellation. Vous ne pouvez pas limiter l’étendue d’une recherche DirSync pour surveiller uniquement un sous-arbre, un conteneur ou un objet spécifique dans un contexte d’appellation.

La technique USNChanged ne présente pas ces limitations, bien qu’elle soit un peu plus compliquée à utiliser que DirSync.

 

 




