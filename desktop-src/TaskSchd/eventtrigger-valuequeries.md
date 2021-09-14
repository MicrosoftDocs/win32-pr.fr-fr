---
title: Propriété EventTrigger. ValueQueries
description: Pour les scripts, obtient ou définit une collection de requêtes XPath nommées. Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans la propriété Subscription.
ms.assetid: 9ff92b66-f63c-4736-b086-df7dd8cd2b10
keywords:
- Planificateur de tâches de la propriété ValueQueries
- Planificateur de tâches de propriété ValueQueries, objet EventTrigger
- Objet EventTrigger Planificateur de tâches, propriété ValueQueries
topic_type:
- apiref
api_name:
- EventTrigger.ValueQueries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd2061f9d910e67855cc0dcb6d64248067fcb9e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008661"
---
# <a name="eventtriggervaluequeries-property"></a>Propriété EventTrigger. ValueQueries

Pour les scripts, obtient ou définit une collection de requêtes XPath nommées. Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans la propriété [**subscription**](eventtrigger-subscription.md) .

## <a name="syntax"></a>Syntaxe


```VB
EventTrigger.ValueQueries As String
```



## <a name="property-value"></a>Valeur de la propriété

Collection de paires nom-valeur. Chaque paire nom-valeur de la collection définit un nom unique pour une valeur de propriété de l’événement qui déclenche le déclencheur d’événement. La valeur de la propriété de l’événement est définie en tant que requête d’événement XPath. Pour plus d’informations sur les requêtes d’événements XPath, consultez [sélection des événements](/previous-versions//aa385231(v=vs.85)).

## <a name="remarks"></a>Notes

Le nom de la requête peut être utilisé en tant que variable dans les propriétés d’action suivantes :

-   [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md)
-   [**ShowMessageAction. title**](showmessageaction-title.md)
-   [**ExecAction. arguments**](execaction-arguments.md)
-   [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md)
-   [**EmailAction. Server**](emailaction-server.md)
-   [**EmailAction. Subject**](emailaction-subject.md)
-   [**EmailAction.To**](emailaction-to.md)
-   [**EmailAction.Cc**](emailaction-cc.md)
-   [**EmailAction. CCI**](emailaction-bcc.md)
-   [**EmailAction. ReplyTo**](emailaction-replyto.md)
-   [**EmailAction. from**](emailaction-from.md)
-   [**EmailAction. Body**](emailaction-body.md)
-   [**ComHandlerAction. Data**](comhandleraction-data.md)

Les chaînes d’exemple de code suivantes affichent deux paires nom/valeur qui peuvent être utilisées dans une collection nom-valeur. Les valeurs retournées par les requêtes XPath peuvent remplacer des variables dans la propriété d’une action. Les valeurs sont référencées par nom, avec `$(user)` et `$(machine)` , dans la propriété action. Par exemple, si les `$(user)` `$(machine)` variables et sont utilisées dans la chaîne [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md) , la valeur des requêtes XPath remplace les variables de la chaîne.

``` syntax
name: user
value: Event/UserData/SubjectUserName

name: machine
value: Event/UserData/MachineName
```

Pour plus d’informations sur l’écriture d’une chaîne de requête pour certains événements, consultez [sélection d’événements](/previous-versions//aa385231(v=vs.85)) et [abonnement à des événements](../wes/subscribing-to-events.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[**EventTrigger**](eventtrigger.md)
</dt> </dl>

 

