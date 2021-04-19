---
description: Rend les interfaces de l’API de script pour WMI disponibles pour les programmeurs C/C++, à la place des versions de l’API COM.
ms.assetid: 18f6cc70-9df1-4d43-a2e0-af03e2f9e2c5
ms.tgt_platform: multiple
title: Interfaces d’automatisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652e9a1fb35a66bddb9f0aebe543770e89e6e2ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543527"
---
# <a name="automation-interfaces"></a>Interfaces d’automatisation

L’API Automation rend les interfaces de l’API de script pour WMI disponibles pour les programmeurs C/C++, à la place des versions de l’API COM.

Le tableau suivant répertorie les objets WMI et la façon dont ils sont utilisés dans l’API d’automatisation. Les références croisées sont liées à la documentation de l’interface pour l’API de script pour les équivalents WMI.



| Objet Automation                                 | Description                                                                                                                 |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**ISWbemEventSource**](swbemeventsource.md)     | Récupère les événements conjointement à [**ISWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).   |
| [**ISWbemLastError**](swbemlasterror.md)         | Fournit des informations d’erreur étendues lorsqu’une erreur se produit.                                                                   |
| [**ISWbemLocator**](swbemlocator.md)             | Obtient une référence à un objet [**ISWbemServices**](swbemservices.md) qui peut accéder à WMI sur un ordinateur hôte particulier. |
| [**ISWbemMethod**](swbemmethod.md)               | Contient une définition de méthode unique.                                                                                        |
| [**ISWbemMethodSet**](swbemmethodset.md)         | Obtient l’accès à une collection d’objets [**ISWbemMethod**](swbemmethod.md) .                                                 |
| [**ISWbemNamedValue**](swbemnamedvalue.md)       | Contient une valeur nommée unique.                                                                                              |
| [**ISWbemNamedValueSet**](swbemnamedvalueset.md) | Obtient l’accès à une collection d’objets [**ISWbemNamedValue**](swbemnamedvalue.md) .                                         |
| [**ISWbemObject**](swbemobject.md)               | Contient et manipule une seule instance ou classe d’objet Common Information Model (CIM).                                  |
| [**ISWbemObjectPath**](swbemobjectpath.md)       | Génère et valide un chemin d’accès à un objet.                                                                                     |
| [**ISWbemObjectSet**](swbemobjectset.md)         | Obtient l’accès à une collection d’objets [**ISWbemObject**](swbemobject.md) .                                                 |
| [**ISWbemPrivilege**](swbemprivilege.md)         | Définit ou efface un privilège.                                                                                                 |
| [**ISWbemPrivilegeSet**](swbemprivilegeset.md)   | Obtient l’accès à une collection d’objets [**ISWbemPrivilege**](swbemprivilege.md) .                                           |
| [**ISWbemProperty**](swbemproperty.md)           | Utilisé pour contenir une propriété CIM unique.                                                                                      |
| [**ISWbemPropertySet**](swbempropertyset.md)     | Accédez à une collection d’objets [**ISWbemProperty**](swbemproperty.md) .                                              |
| [**ISWbemQualifier**](swbemqualifier.md)         | Contient un qualificateur de classe unique.                                                                                          |
| [**ISWbemQualifierSet**](swbemqualifierset.md)   | Obtient l’accès à une collection d’objets [**ISWbemQualifier**](swbemqualifier.md) .                                           |
| [**ISWbemSecurity**](swbemsecurity.md)           | Gère les paramètres de sécurité tels que le privilège COM (Component Object Model), AuthenticationLevel et ImpersonationLevel.      |
| [**ISWbemServices**](swbemservices.md)           | Crée, met à jour et récupère des instances ou des classes.                                                                       |
| [**ISWbemSink**](swbemsink.md)                   | Reçoit les résultats des opérations asynchrones d’application cliente et des notifications d’événements.                                 |



 

 

 



