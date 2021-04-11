---
description: L’API de script pour la référence WMI décrit chaque objet de script à l’aide d’une syntaxe spécifique. Pour une explication de cette syntaxe, consultez conventions de document pour l’API de script.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Scripts d’objets d’API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e30d3269b137686472f54cdb8cf53720b4aad978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202168"
---
# <a name="scripting-api-objects"></a>Scripts d’objets d’API

L’API de script pour la référence WMI décrit chaque objet de script à l’aide d’une syntaxe spécifique. Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Le tableau suivant répertorie les objets de script WMI et la façon dont ils sont utilisés.



| Object                                               | Description                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Construit et analyse les valeurs [DateTime](date-and-time-format.md) CIM.                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | Récupère les événements conjointement à [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | Fournit des informations d’erreur étendues lorsqu’une erreur se produit.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Obtient un objet [**SWbemServices**](swbemservices.md) qui peut accéder à WMI sur un ordinateur hôte particulier.                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | Contient une définition de méthode WMI unique.                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | Obtient une collection d’objets [**SWbemMethod**](swbemmethod.md) .                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | Contient une valeur nommée unique.                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | Obtient l’accès à une collection d’objets [**SWbemNamedValue**](swbemnamedvalue.md) .                                                                                                                                                                     |
| [**M**](swbemobject.md)                   | Contient et manipule une seule classe d’objet ou instance WMI.                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | Étend les fonctionnalités de [**SWbemObject**](swbemobject.md). Cet objet ajoute la méthode [**Refresh**](swbemrefresher-refresh.md) pour les objets [**SWbemRefresher**](swbemrefresher.md) .                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | Génère et valide un chemin d’accès à un objet.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Obtient l’accès à une collection d’objets [**SWbemObject**](swbemobject.md) .                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | Définit ou efface un privilège.                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | Obtient l’accès à une collection d’objets [**SWbemPrivilege**](swbemprivilege.md) .                                                                                                                                                                       |
| [**SWbemProperty**](swbemproperty.md)               | Contient une propriété WMI unique.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Obtient l’accès à une collection d’objets [**SWbemProperty**](swbemproperty.md) .                                                                                                                                                                         |
| [**SWbemQualifier**](swbemqualifier.md)             | Contient un qualificateur de propriété unique.                                                                                                                                                                                                                  |
| [**SWbemQualifierSet**](swbemqualifierset.md)       | Obtient l’accès à une collection d’objets [**SWbemQualifier**](swbemqualifier.md) .                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | Collecte et met à jour les valeurs des propriétés de l’objet en une seule opération.                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Représente un élément actualisable unique dans un objet [**SWbemRefresher**](swbemrefresher.md) , tel qu’une propriété.                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | Gère les paramètres de sécurité tels que les [**privilèges**](swbemsecurity-privileges.md)com (Component Object Model), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)et [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md).   |
| [**M**](swbemservices.md)               | Crée, met à jour et récupère des instances ou des classes.                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | Étend les fonctionnalités de [**SWbemServices**](swbemservices.md). Cet objet ajoute les méthodes [**put**](swbemservicesex-put.md) et [**PutAsync**](swbemservicesex-putasync.md) pour permettre l’enregistrement d’une classe ou d’une instance dans plusieurs espaces de noms. |
| [**SWbemSink**](swbemsink.md)                       | Reçoit les résultats des opérations asynchrones et des notifications d’événements, qui sont utilisées par les applications clientes.                                                                                                                                        |



 

 

 



