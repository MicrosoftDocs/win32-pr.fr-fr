---
title: Élément Delay (registrationTriggerType)
description: Spécifie la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée.
ms.assetid: 8955d86c-8306-45e7-93cf-eacf50e10075
keywords:
- Retarder l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fe1a580a0e69c8e4816022971b2d0bc143544cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013408"
---
# <a name="delay-registrationtriggertype-element"></a>Élément Delay (registrationTriggerType)

Spécifie la durée entre le moment où la tâche est inscrite et le moment où la tâche est démarrée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L’élément **delay** est défini par le type complexe [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                     | Dérivé de                                                                               | Description                                                                    |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsque la tâche est inscrite.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, le délai de déclenchement d’inscription est spécifié à l’aide de la propriété [**RegistrationTrigger. Delay**](registrationtrigger-delay.md) .

Pour le développement C++, le délai de déclenchement de l’inscription est spécifié à l’aide de la propriété [**IRegistrationTrigger ::D Nouv**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un délai de déclenchement d’inscription qui autorise un délai de 5 minutes entre le moment où la tâche est inscrite et le démarrage de la tâche.


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay>PT5M<Delay>
 </BootTrigger>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





