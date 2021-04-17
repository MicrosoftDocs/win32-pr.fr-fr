---
title: Élément Duration (idleSettingsType)
description: Spécifie la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Élément Duration Planificateur de tâches
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508433"
---
# <a name="duration-idlesettingstype-element"></a>Élément Duration (idleSettingsType)

Spécifie la durée pendant laquelle l’ordinateur doit être dans un état inactif avant que la tâche ne soit exécutée. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). La valeur minimale est d’une minute. Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Duration"
    default="PT10M"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L’élément est défini par le type complexe [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                       | Dérivé de                                                                 | Description                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est dans un état d’inactivité.<br/> |



## <a name="remarks"></a>Notes

Pour la programmation de script, ce paramètre inactif est spécifié à l’aide de la propriété [**IdleSettings. IdleDuration**](idlesettings-idleduration.md) .

Pour la programmation en C++, ce paramètre inactif est spécifié à l’aide de la propriété [**IIdleSettings :: IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) .

## <a name="examples"></a>Exemples

Le code XML suivant définit un paramètre inactif qui autorise 5 minutes à démarrer la tâche.


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





