---
description: Décrit les conventions de document relatives à la lecture des rubriques de l’API de script WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Conventions de document pour l’API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127526200"
---
# <a name="document-conventions-for-the-scripting-api"></a>Conventions de document pour l’API de script

L' [API de script pour](scripting-api-for-wmi.md) la référence WMI utilise les conventions de document suivantes :

-   Les types de paramètres sont définis à l’aide d’un préfixe : b (booléen), Str (String), I (Integer), obj (objet Automation), var (variant).
-   Les paramètres facultatifs sont placés entre crochets avec leurs valeurs par défaut affichées par assignation.
-   Dans le cas des paramètres d’objet, les caractères qui suivent le préfixe « obj » indiquent le type d’objet attendu.



| Paramètre de l’objet      | Type d'objet                                          |
|-----------------------|------------------------------------------------------|
| *WbemDatetime*        | [**SWbemDateTime**](swbemdatetime.md)               |
| *WbemEventSource*     | [**SWbemEventSource**](swbemeventsource.md)         |
| *WbemLocator*         | [**SWbemLocator**](swbemlocator.md)                 |
| *WbemMethod*          | [**SWbemMethod**](swbemmethod.md)                   |
| *WbemMethodSet*       | [**SWbemMethodSet**](swbemmethodset.md)             |
| *WbemNamedValueSet*   | [**SWbemNamedValueSet**](swbemnamedvalueset.md)     |
| *WbemObject*          | [**M**](swbemobject.md)                   |
| *WbemObjectEx*        | [**SWbemObjectEx**](swbemobjectex.md)               |
| *WbemObjectPath*      | [**SWbemObjectPath**](swbemobjectpath.md)           |
| *WbemObjectSet*       | [**SWbemObjectSet**](swbemobjectset.md)             |
| *WbemPrivilege*       | [**SWbemPrivilege**](swbemprivilege.md)             |
| *WbemPrivilegeSet*    | [**SWbemPrivilegeSet**](swbemprivilegeset.md)       |
| *WbemProperty*        | [**SWbemProperty**](swbemproperty.md)               |
| *WbemPropertySet*     | [**SWbemPropertySet**](swbempropertyset.md)         |
| *WbemQualifier*       | [**SWbemQualifier**](swbemqualifier.md)             |
| *WbemQualifierSet*    | [**SWbemQualifierSet**](swbemqualifierset.md)       |
| *WbemRefreshableItem* | [**SWbemRefreshableItem**](swbemrefreshableitem.md) |
| *WbemRefresher*       | [**SWbemRefresher**](swbemrefresher.md)             |
| *WbemServices*        | [**M**](swbemservices.md)               |
| *WbemServicesEx*      | [**SWbemServicesEx**](swbemservicesex.md)           |



 

Par exemple, le code suivant montre comment nommer des variables pour différents types d’objets :


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



