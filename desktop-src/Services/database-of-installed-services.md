---
description: Le SCM gère une base de données des services installés dans le registre.
ms.assetid: 70f24e15-2607-4c32-9192-a9413b74558b
title: Base de données des services installés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24a92712d6713e2ca31dbc4b768e3b7c2983ffc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233124"
---
# <a name="database-of-installed-services"></a>Base de données des services installés

Le SCM gère une base de données des services installés dans le registre. La base de données est utilisée par le SCM et les programmes qui ajoutent, modifient ou configurent des services. Voici la clé de registre de cette base de données : **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services**.

Cette clé contient une sous-clé pour chaque service installé et le service de pilote. Le nom de la sous-clé est le nom du service, tel que spécifié par la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) lorsque le service a été installé par un programme de configuration de service.

Une copie initiale de la base de données est créée lors de l’installation du système. La base de données contient des entrées pour les pilotes de périphérique requis lors du démarrage du système. La base de données comprend les informations suivantes sur chaque service installé et le service de pilote :

-   Type de service. Cela indique si le service s’exécute dans son propre processus ou s’il partage un processus avec d’autres services. Pour les services de pilote, cela indique si le service est un pilote de noyau ou un pilote de système de fichiers.
-   Type de démarrage. Cela indique si le service ou le service de pilote est démarré automatiquement au démarrage du système (service de démarrage automatique) ou si le SCM le démarre lorsqu’il est demandé par un programme de contrôle de service (service à démarrage à la demande). Le type de démarrage peut également indiquer que le service ou le service de pilote est désactivé. dans ce cas, il ne peut pas être démarré.
-   Niveau de contrôle de l’erreur. Cela spécifie la gravité de l’erreur si le service ou le service de pilote ne parvient pas à démarrer au démarrage du système et détermine l’action que le programme de démarrage prendra.
-   Chemin d’accès qualifié complet du fichier exécutable. L’extension de nom de fichier est .EXE pour les services et .SYS pour les services de pilote.
-   Informations de dépendance facultatives utilisées pour déterminer l’ordre approprié pour démarrer les services ou les services de pilote. Pour les services, ces informations peuvent inclure une liste de services que le SCM doit démarrer avant de pouvoir démarrer le service spécifié, le nom d’un groupe d’ordre de chargement dont le service fait partie, et un identificateur de balise qui indique l’ordre de démarrage du service dans son groupe de commande de charge. Pour les services de pilote, ces informations incluent une liste de pilotes qui doivent être démarrés avant le pilote spécifié.
-   Pour les services, un nom de compte et un mot de passe facultatifs. Le programme de service s’exécute dans le contexte de ce compte. Si aucun compte n’est spécifié, le service s’exécute dans le contexte du [compte LocalSystem](localsystem-account.md).
-   Pour les services de pilote, il s’agit d’un nom d’objet de pilote facultatif (par exemple, \\ \\ le système de fichiers RDR ou le \\ pilote \\ XNS), utilisé par le système d’e/s pour charger le pilote de périphérique. Si aucun nom n’est spécifié, le système d’e/s crée un nom par défaut basé sur le nom du service de pilote.

> [!Note]  
> Cette base de données est également appelée base de données ServicesActive ou la base de données SCM. Vous devez utiliser les fonctions fournies par le SCM au lieu de modifier directement la base de données.

 

 

 



