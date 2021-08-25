---
description: Une collection est un concept d’automatisation standard qui fournit une interface uniforme à un ensemble d’objets sur lesquels vous pouvez effectuer une itération.
ms.assetid: c1ebe529-33cb-4158-923d-124d6328fc60
ms.tgt_platform: multiple
title: Accès à une collection WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da563830b742b47a138c106b21efe197108bbdddf7ad7f86b90984a04431aa0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860512"
---
# <a name="accessing-a-wmi-collection"></a>Accès à une collection WMI

Une collection est un concept d’automatisation standard qui fournit une interface uniforme à un ensemble d’objets sur lesquels vous pouvez effectuer une itération. L’API de script pour WMI expose un certain nombre d’interfaces conformes au paradigme de collecte. Dans chaque cas, utilisez la méthode **Item** pour identifier les éléments à l’aide d’une chaîne contenant la valeur.

Les collections [**SWbemPropertySet**](swbempropertyset.md), [**SWbemQualifierSet**](swbemqualifierset.md)et [**SWbemMethodSet**](swbemmethodset.md) sont principalement utilisées pour modifier le schéma. Un objet [**SWbemObjectSet**](swbemobjectset.md) contient des objets WMI, tels qu’une instance de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , qui ont été obtenus par le biais d’appels, tels que [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) ou [**SWbemObject. ASSOCIATORS \_**](swbemobject-associators-.md). L’objet [**SWbemRefresher**](swbemrefresher.md) peut uniquement contenir des instances de classes WMI. L’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) peut contenir des objets WMI ou tout autre type de données dont un fournisseur a besoin pour l’appel de méthode.

> [!Note]  
> Les rubriques suivantes ont été écrites principalement pour VBScript. C# utilise l’interface [IEnumerable](/dotnet/api/system.collections.ienumerable) standard pour assembler et énumérer des objets. En revanche, PowerShell utilise généralement une collection d’objets implicite chaque fois qu’une valeur de retour contient plusieurs résultats.

 

Le tableau suivant répertorie les collections de l’API de script pour WMI, ainsi que les éléments et les paramètres de chaque collection.



| Collection                                       | Élément                                              | Paramètre Item ()                                                         |
|--------------------------------------------------|------------------------------------------------------|--------------------------------------------------------------------------|
| [**SWbemObjectSet**](swbemobjectset.md)         | [**M**](swbemobject.md)                   | Chemin d’accès de l’objet                                                              |
| [**SWbemPropertySet**](swbempropertyset.md)     | [**SWbemProperty**](swbemproperty.md)               | Nom de la propriété                                                            |
| [**SWbemQualifierSet**](swbemqualifierset.md)   | [**SWbemQualifier**](swbemqualifier.md)             | Nom du qualificateur                                                           |
| [**SWbemMethodSet**](swbemmethodset.md)         | [**SWbemMethod**](swbemmethod.md)                   | Nom de la méthode                                                              |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md) | [**SWbemNamedValue**](swbemnamedvalue.md)           | Nom de valeur                                                               |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)   | [**SWbemPrivilege**](swbemprivilege.md)             | Nom du privilège                                                           |
| [**SWbemRefresher**](swbemrefresher.md)         | [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Index de l’élément dans l’objet [**SWbemRefresher**](swbemrefresher.md) |



 

Pour plus d’informations et pour obtenir des exemples d’ajout et de suppression d’éléments dans une collection, consultez [Suppression d’un élément unique d’une collection](removing-a-single-item-from-a-collection.md) et [Suppression de plusieurs éléments d’une collection](removing-multiple-items-from-a-collection.md). Pour plus d’informations sur l’utilisation des classes, consultez [manipulation des informations relatives](manipulating-class-and-instance-information.md)aux classes et aux instances.

 

 
