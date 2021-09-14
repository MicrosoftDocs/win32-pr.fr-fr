---
title: Fonctions d’alerte
description: Les fonctions d’alerte de gestion de réseau notifient les programmes de service réseau et les applications d’événements réseau.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fde863b27bebc8bf815c939f7edf96cd998442
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119325"
---
# <a name="alert-functions"></a>Fonctions d’alerte

\[les fonctions d’alerte ne sont pas prises en charge à partir de Windows Vista, car les services alertes et messenger ne sont pas pris en charge.\]

Les fonctions d’alerte de gestion de réseau notifient les programmes de service réseau et les applications d’événements réseau. Un *événement* est une instance particulière d’un processus, d’une occurrence ou d’un état de matériel tel que défini par une application. Les fonctions d’alerte permettent aux applications d’indiquer quand des événements prédéfinis se produisent.

**Windows Server 2003 :** les services alertes et messenger sont désactivés par défaut sur Windows Server 2003. Vous devez réactiver les services avant d’appeler les fonctions d’alerte de gestion de réseau ou les [fonctions de message](message-functions.md)de gestion de réseau.

Les fonctions d’alerte sont répertoriées ci-après.



| Fonction                                   | Description                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Avertit tous les clients inscrits qu’un événement particulier s’est produit.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Simplifie la notification des clients inscrits qu’un événement particulier s’est produit, car, contrairement à **NetAlertRaise**, **NetAlertRaiseEx** ne nécessite pas de structure d' [**\_ alerte STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) . |



 

Le service d’alerte doit être en cours d’exécution sur l’ordinateur client lorsque vous appelez la fonction **NetAlertRaise** ou la fonction **NetAlertRaiseEx** . Si le service n’est pas en cours d’exécution, les fonctions échouent avec le **fichier d’erreur \_ \_ \_ introuvable**. Le service d’alerte sur le client appelle la fonction [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) pour envoyer des informations aux destinataires.

Les applications, les services réseau et les composants réseau internes utilisent les fonctions d’alerte de gestion de réseau pour déclencher une alerte, en avertissant plusieurs applications ou utilisateurs lorsqu’un type particulier d’événement se produit. Les fonctions de catégorie d’alerte, les types de données, les structures et les constantes sont définis dans le LMCONS. H, LMERR. H et LMALERT. Fichiers d’en-tête H. Pour accéder à ces définitions, définissez les constantes, y compris les \_ Erreurs de l' \_ en-tête et les alertes NetAlert, et incluez le fichier d’en-tête LM. H.

LMALERT. Le fichier H prédéfinit les classes d’alerte suivantes (types d’événements réseau) pour l’envoi d’alertes :

-   Événements réseau nécessitant une assistance administrative
-   Ajout d’une entrée à un fichier journal des erreurs
-   Réception d’un message de diffusion par un utilisateur ou une application
-   Achèvement d’un travail d’impression
-   Utilisation de certaines applications ou ressources par les utilisateurs

Vous pouvez définir d’autres classes d’alertes pour les applications réseau en fonction des besoins. Par exemple, si une application sur un serveur écrit régulièrement de grandes quantités de données sur un lecteur de disque, l’application risque de saturer le disque. Dans ce cas, vous souhaiterez peut-être ajouter l’événement « pas d’espace disque libre » pour déclencher une alerte qui indique à l’application de suspendre ou de terminer le processus qui remplit le disque. Le nom d’événement d’une alerte peut être n’importe quelle chaîne de texte.

Lorsque vous déclenchez une alerte avec un appel à la fonction [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) , les données du message doivent se composer d’une structure d’en-tête d' [**\_ alerte STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) , suivie de données de longueur fixe supplémentaires qui sont spécifiques aux alertes dans un administrateur, d’autres informations, [**ERRLOG \_ autres \_**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info)informations, [**imprimer d' \_ autres \_**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)informations ou structure d' [**\_ autres \_ informations**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) de l’utilisateur. [**\_ \_**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info) Les données de longueur variable supplémentaires peuvent suivre la structure spécifique aux alertes. (Les appels à la fonction [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) ne nécessitent pas de structure d' **\_ alerte STD** .) L’application appelante doit allouer la mémoire pour toutes les structures et toutes les données de longueur variable, et libérer la mémoire après le retour de l’appel.

Les macros suivantes peuvent être utilisées avec des tampons de données d’alerte.



| Macro                                          | Description                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**ALERTEr d' \_ autres \_ informations**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Retourne un pointeur vers les données de longueur fixe qui suivent la structure d' **\_ alerte STD** dans un message d’alerte. |
| [**\_données var d’alerte \_**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Retourne un pointeur vers les données de longueur variable qui suivent les données spécifiques aux alertes dans un message d’alerte.   |



 

au lieu d’utiliser les fonctions d’alerte de gestion de réseau, vous pourrez peut-être utiliser le kit de développement logiciel (SDK) Windows Management Instrumentation (WMI) pour la notification d’événements. Pour plus d’informations sur les plateformes qui prennent en charge le modèle d’événement WMI, consultez [infrastructure WMI](/windows/desktop/WmiSdk/wmi-infrastructure) et [événements de surveillance](/windows/desktop/WmiSdk/monitoring-events) dans la documentation WMI.

 

 