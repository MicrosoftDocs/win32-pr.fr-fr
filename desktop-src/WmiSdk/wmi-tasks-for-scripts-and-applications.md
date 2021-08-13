---
description: Décrit comment trouver la classe et les procédures WMI appropriées à utiliser dans les scripts et les applications qui effectuent des tâches d’administration réseau et d’ordinateur courantes.
ms.assetid: fe15b67c-8ae6-4360-a2ee-1eda292dd05a
ms.tgt_platform: multiple
title: Tâches WMI pour les scripts et les applications
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d273db41b832b8141fe13bdf0538b51fb221688949792e214c9f81c1e7b96e69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553123"
---
# <a name="wmi-tasks-for-scripts-and-applications"></a>Tâches WMI pour les scripts et les applications

Les sections suivantes décrivent différentes tâches d’administration d’ordinateur et de réseau et fournissent des liens vers la classe WMI ou les classes utilisées pour exécuter ces tâches. Pour plus d’informations, consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md). Pour plus d’informations sur l’utilisation de WMI, voir plus d' [informations](further-information.md). Pour plus d’informations sur l’utilisation de WMI, voir [technet scriptcenter](https://www.microsoft.com/technet/scriptcenter/default.mspx). (Ces ressources peuvent ne pas être disponibles dans chaque langue ou pays/région.)

Pour plus d’informations sur la façon de fournir des données à WMI, consultez [utilisation de WMI](using-wmi.md), qui fait référence aux rubriques relatives à l’écriture d’un [*fournisseur*](gloss-p.md)WMI.

Les opérations présentées dans des exemples de script peuvent être effectuées par les applications en C++ ou Visual Basic. Pour plus d’informations, consultez [la page création d’une application WMI à l’aide d’exemples d'](creating-a-wmi-application-using-c-.md) applications C++ et [WMI c++](wmi-c---application-examples.md).

Le tableau suivant répertorie les catégories de tâches.



| Catégories de tâche                                                               | Description                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comptes et domaines](wmi-tasks--accounts-and-domains.md)                   | Obtenir des informations telles que le domaine de l’ordinateur ou l’utilisateur actuellement connecté. La plupart des tâches liées au domaine ou au compte sont effectuées de manière optimale avec les scripts [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) . Pour obtenir des exemples, consultez le ScriptCenter TechNet à l’adresse [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) . |
| [Matériel informatique](wmi-tasks--computer-hardware.md)                         | Obtenir des informations sur la présence, l’État ou les propriétés de composants matériels. Par exemple, vous pouvez déterminer si un ordinateur est un ordinateur de bureau ou un ordinateur portable.                                                                                                                                                                                             |
| [Logiciel informatique](wmi-tasks--computer-software.md)                         | obtenir des informations telles que le logiciel installé par les versions Windows Installer (MSI) et logicielles.                                                                                                                                                                                                                                              |
| [Connexion au service WMI](wmi-tasks--connecting-to-the-wmi-service.md) | Pour obtenir des données à partir de WMI, sur l’ordinateur local ou à partir d’un ordinateur distant, vous devez vous connecter au service WMI en vous connectant à un [*espace de noms*](gloss-n.md)spécifique. Dans la plupart des cas, utilisez soit la connexion sténographique [moniker](creating-a-wmi-script.md) , soit la connexion [**localisateur**](swbemlocator-connectserver.md) .    |
| [Dates et heures](wmi-tasks--dates-and-times.md)                             | Il existe des classes WMI et un objet de script pour analyser ou convertir le format [DateTime CIM](date-and-time-format.md) .                                                                                                                                                                                                                                     |
| [Gestion des postes de travail](wmi-tasks--desktop-management.md)                       | Obtenir des données à partir de ou contrôler les bureaux à distance. Par exemple, vous pouvez déterminer si l’écran de veille requiert ou non un mot de passe. WMI vous donne également la possibilité d’arrêter un ordinateur distant.                                                                                                                                                               |
| [Disques et systèmes de fichiers](wmi-tasks--disks-and-file-systems.md)               | Obtenir des informations sur l’état du matériel du lecteur de disque, sur les volumes logiques.                                                                                                                                                                                                                                                                                      |
| [Journaux des événements](wmi-tasks--event-logs.md)                                       | Obtenir des données d’événement à partir de fichiers journaux des événements NT et effectuer des opérations telles que la sauvegarde ou l’effacement des fichiers journaux.                                                                                                                                                                                                                                                   |
| [Fichiers et dossiers](wmi-tasks--files-and-folders.md)                         | Modifiez les propriétés des fichiers ou des dossiers par le biais de WMI, y compris la création d’un partage ou le changement de nom d’un fichier.                                                                                                                                                                                                                                                              |
| [Mise en réseau](wmi-tasks--networking.md)                                       | Gérer et obtenir des informations sur les connexions et les adresses IP ou MAC.                                                                                                                                                                                                                                                                                  |
| [Systèmes d’exploitation](wmi-tasks--operating-systems.md)                         | Obtenez des informations sur le système d’exploitation, telles que la version, si elle est activée ou les correctifs installés.                                                                                                                                                                                                                                  |
| [Analyse des performances](wmi-tasks--performance-monitoring.md)               | Utilisez les classes WMI qui obtiennent des données à partir des compteurs de performances pour accéder et actualiser les données sur les performances de l’ordinateur.                                                                                                                                                                                                                                     |
| [Processus](wmi-tasks--processes.md)                                         | Obtenir des informations telles que le compte sous lequel un processus est en cours d’exécution. Vous pouvez effectuer des actions telles que la création de processus.                                                                                                                                                                                                                                 |
| [Imprimantes et impression](wmi-tasks--printers-and-printing.md)                 | Gérez et obtenez des données sur les imprimantes, telles que la recherche ou la définition de l’imprimante par défaut.                                                                                                                                                                                                                                                                    |
| [Registre](wmi-tasks--registry.md)                                           | Créer et modifier des clés et des valeurs de registre.                                                                                                                                                                                                                                                                                                               |
| [Tâches planifiées](wmi-tasks--scheduled-tasks.md)                             | Créez et récupérez des informations sur les tâches planifiées.                                                                                                                                                                                                                                                                                                         |
| [Services](wmi-tasks--services.md)                                           | Obtenir des informations sur les services, notamment les services dépendants ou antécédents.                                                                                                                                                                                                                                                                            |



 

 

 
