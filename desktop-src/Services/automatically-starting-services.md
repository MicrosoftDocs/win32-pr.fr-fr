---
description: Lors du démarrage du système, le SCM démarre tous les services à démarrage automatique et les services dont ils dépendent. Par exemple, si un service à démarrage automatique dépend d’un service de démarrage à la demande, le service de démarrage à la demande est également démarré automatiquement.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Démarrage automatique des services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522665"
---
# <a name="automatically-starting-services"></a>Démarrage automatique des services

Lors du démarrage du système, le SCM démarre tous les services à démarrage automatique et les services dont ils dépendent. Par exemple, si un service à démarrage automatique dépend d’un service de démarrage à la demande, le service de démarrage à la demande est également démarré automatiquement.

L’ordre de chargement est déterminé par les éléments suivants :

1.  L’ordre des groupes dans la liste des groupes d’ordre de chargement. Ces informations sont stockées dans la valeur **ServiceGroupOrder** de la clé de Registre suivante :

    **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control**

    Pour spécifier le groupe de commandes de charge pour un service, utilisez le paramètre *lpLoadOrderGroup* de la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .

2.  Ordre des services au sein d’un groupe spécifié dans le vecteur d’ordre des balises. Ces informations sont stockées dans la valeur **GroupOrderList** de la clé de Registre suivante :

    **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control**

3.  Les dépendances listées pour chaque service.

Une fois le démarrage terminé, le système exécute le programme de vérification de démarrage spécifié par la valeur **BootVerificationProgram** de la clé de Registre suivante : **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control**.

Par défaut, cette valeur n'est pas définie. Le système signale simplement que le démarrage a réussi après que le premier utilisateur s’est connecté. Vous pouvez fournir un programme de vérification de démarrage qui vérifie le système à la recherche de problèmes et signale l’état de démarrage au SCM à l’aide de la fonction [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .

Après un démarrage réussi, le système enregistre un clone de la base de données dans la dernière configuration connue (correcte connue). Le système peut restaurer cette copie de la base de données si les modifications apportées à la base de données active entraînent l’échec du redémarrage du système. Voici la clé de registre de cette base de données :

**HKEY \_ local \_ machine \\ System \\ ControlSet *xxx* \\ services**

où *xxx* est la valeur enregistrée dans la valeur de Registre suivante : **HKEY \_ local \_ machine \\ System \\ Select \\ LastKnownGood**.

Si un service à démarrage automatique avec une erreur de SERVICE de niveau de contrôle d’erreur \_ \_ critique ne démarre pas, le SCM redémarre l’ordinateur à l’aide de la configuration correcte connue. Si la configuration correcte connue est déjà utilisée, le démarrage échoue.

Un service à démarrage automatique peut être configuré en tant que service à démarrage automatique retardé en appelant la fonction [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) avec \_ les \_ informations de démarrage automatique différé de la configuration du service \_ \_ \_ . Cette modification prend effet après le prochain démarrage du système. Pour plus d’informations, [**consultez \_ \_ \_ \_ informations sur le démarrage automatique retardé du service**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).

 

 



