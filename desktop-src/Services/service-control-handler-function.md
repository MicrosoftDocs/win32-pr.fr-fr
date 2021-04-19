---
description: Chaque service a un gestionnaire de contrôle, la fonction de gestionnaire, qui est appelé par le répartiteur de contrôle lorsque le processus de service reçoit une demande de contrôle d’un programme de contrôle de service.
ms.assetid: 437334ed-05fa-4ab6-aab3-dc2739113e19
title: Fonction du gestionnaire de contrôle des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1303bff45421ee7206d02be9ee30066324648823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514168"
---
# <a name="service-control-handler-function"></a>Fonction du gestionnaire de contrôle des services

Chaque service a un gestionnaire de contrôle, la fonction de [**Gestionnaire**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) , qui est appelé par le répartiteur de contrôle lorsque le processus de service reçoit une demande de contrôle d’un programme de contrôle de service. Par conséquent, cette fonction s’exécute dans le contexte du répartiteur de contrôle. Pour obtenir un exemple, consultez [écriture d’une fonction de gestionnaire de contrôle](writing-a-control-handler-function.md).

Un service appelle la fonction [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) ou [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) pour enregistrer sa fonction de gestionnaire de contrôle des services.

Quand le gestionnaire de contrôle des services est appelé, le service doit appeler la fonction [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) pour signaler son état au SCM uniquement si la gestion du code de contrôle entraîne la modification de l’état du service. Si la gestion du code de contrôle n’entraîne pas la modification de l’état du service, il n’est pas nécessaire d’appeler **SetServiceStatus**.

Un programme de contrôle de service peut envoyer des demandes de contrôle à l’aide de la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Tous les services doivent accepter et traiter le code de contrôle d' **\_ \_ interrogation du contrôle des services** . Vous pouvez activer ou désactiver l’acceptation des autres codes de contrôle en appelant [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus). Pour recevoir le code de contrôle **\_ \_ DEVICEEVENT du contrôle de service** , vous devez appeler la fonction [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) . Les services peuvent également gérer des codes de contrôle supplémentaires définis par l’utilisateur.

Si un service accepte le code de contrôle d' **\_ \_ arrêt du contrôle de service** , il doit s’arrêter lors de la réception, en accédant à l’état d’arrêt du **service \_ \_ en attente** ou d' **\_ arrêt du service** . Une fois que le SCM a envoyé ce code de contrôle, il n’envoie pas d’autres codes de contrôle.

**Windows XP :** Si le service **ne retourne aucune \_ erreur** et continue à s’exécuter, il continue à recevoir les codes de contrôle. Ce comportement a été modifié à partir de Windows Server 2003 et Windows XP avec Service Pack 2 (SP2).

Le gestionnaire de contrôle doit retourner dans un délai de 30 secondes, sinon le SCM renvoie une erreur. Si un service doit effectuer un traitement long lorsque le service exécute le gestionnaire de contrôle, il doit créer un thread secondaire pour effectuer le traitement long, puis retourner à partir du gestionnaire de contrôle. Cela empêche le service de relier le répartiteur de contrôle. Par exemple, lors de la gestion de la demande d’arrêt pour un service qui prend beaucoup de temps, créez un autre thread pour gérer le processus d’arrêt. Le gestionnaire de contrôle doit simplement appeler [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) avec le service qui arrête le message **\_ \_ en attente** et retourne.

Lorsque l’utilisateur ferme le système, tous les gestionnaires de contrôle qui ont appelé [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) avec le service acceptent le code de contrôle de **\_ \_ préarrêt** reçoivent le code de contrôle de **\_ \_ préarrêt du contrôle de service** . Le gestionnaire de contrôle des services attend que le service s’arrête ou que la valeur du délai d’attente de préarrêt spécifié expire (cette valeur peut être définie avec la fonction [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) ). Ce code de contrôle doit être utilisé uniquement dans des circonstances particulières, car un service qui gère cette notification bloque l’arrêt du système jusqu’à ce que le service s’arrête ou que l’intervalle de délai d’attente avant l’arrêt expire.

Une fois les notifications de préarrêt terminées, tous les gestionnaires de contrôle qui ont appelé [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) avec le **service \_ acceptent \_** le code de contrôle d’arrêt reçoivent le code de contrôle d' **\_ \_ arrêt du contrôle de service** . Ils sont notifiés dans l’ordre dans lequel ils apparaissent dans la base de données des services installés. Par défaut, un service dispose d’environ 20 secondes pour effectuer des tâches de nettoyage avant que le système ne s’arrête. À l’expiration de ce délai, l’arrêt du système se poursuit, que l’arrêt du service soit terminé ou non. Notez que si le système est laissé à l’état d’arrêt (pas redémarré ou mis hors tension), le service continue à s’exécuter.

Si le service nécessite plus de temps pour le nettoyage, il envoie des messages d’état d' **arrêt \_ en attente** , ainsi qu’un indicateur d’attente, afin que le contrôleur de service sache combien de temps attendre avant de signaler au système que l’arrêt du service est terminé. Toutefois, pour empêcher un service d’arrêter l’arrêt, la durée d’attente du contrôleur de service est limitée. Si le service est arrêté par le biais du composant logiciel enfichable Services, la limite est de 125 secondes, soit 125 000 millisecondes. Si le système d’exploitation est en cours de redémarrage, la limite de temps est spécifiée dans la valeur **WaitToKillServiceTimeout** (en millisecondes) de la clé de Registre suivante :

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control**

> [!IMPORTANT]
> Un service ne doit pas tenter d’augmenter la limite de temps en modifiant cette valeur. Si vous n’avez pas besoin de définir **WaitToKillServiceTimeout** à la main, la valeur doit être exprimée en millisecondes.

Les clients doivent arrêter rapidement le système d’exploitation. Par exemple, si un ordinateur exécutant une alimentation UPS ne peut pas se terminer avant que l’onduleur ne soit hors tension, les données peuvent être perdues. Par conséquent, les services doivent effectuer leurs tâches de nettoyage aussi rapidement que possible. Il est conseillé de réduire les données non enregistrées en enregistrant régulièrement les données, en conservant le suivi des données enregistrées sur le disque et en enregistrant uniquement les données non enregistrées à l’arrêt. Étant donné que l’ordinateur est en cours d’arrêt, ne perdez pas de temps à libérer de la mémoire ou d’autres ressources système. Si vous avez besoin de notifier un serveur que vous quittez, réduisez le temps passé à attendre une réponse, car des problèmes réseau pourraient retarder l’arrêt de votre service.

Notez que pendant l’arrêt du service, par défaut, le SCM ne prend pas en compte les dépendances. Le SCM énumère la liste des services en cours d’exécution et envoie la commande d' **\_ \_ arrêt du contrôle de service** . Par conséquent, un service peut échouer parce qu’un autre service dont il dépend a déjà été arrêté.

Pour définir manuellement l’ordre d’arrêt des services, créez une valeur de Registre multichaîne qui contient les noms de service dans l’ordre dans lequel ils doivent être arrêtés et affectez-les à la valeur **PreshutdownOrder** de la clé de contrôle, comme suit :

**HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ PreshutdownOrder = "ordre d’arrêt"**

Pour définir l’ordre d’arrêt des services dépendants à partir de votre application, utilisez la fonction [**SetProcessShutdownParameters**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) . Le SCM utilise cette fonction pour attribuer à son gestionnaire la priorité 0x1E0. Le SCM envoie des notifications d' **\_ \_ arrêt du contrôle de service** lorsque son gestionnaire de contrôle est appelé et attend que les services se ferment avant de retourner à partir de son gestionnaire de contrôle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’une fonction de gestionnaire de contrôle](writing-a-control-handler-function.md)
</dt> </dl>

 

 
