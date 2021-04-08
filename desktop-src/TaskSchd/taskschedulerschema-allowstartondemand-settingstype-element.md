---
title: Élément AllowStartOnDemand (settingsType)
description: Spécifie que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Élément AllowStartOnDemand Planificateur de tâches
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941825"
---
# <a name="allowstartondemand-settingstype-element"></a>Élément AllowStartOnDemand (settingsType)

Spécifie que la tâche peut être démarrée à l’aide de la commande exécuter ou du menu contextuel.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

L’élément **AllowStartOnDemand** est défini par le type complexe [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Paramètres**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contient les paramètres que le Planificateur de tâches utilise pour effectuer la tâche.<br/> |



## <a name="remarks"></a>Notes

Lorsque cet élément est défini sur true, la tâche peut être démarrée indépendamment du moment où les déclencheurs démarrent la tâche.

Pour le développement C++, consultez la [**propriété AllowDemandStart de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Pour le développement de scripts, consultez [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui autorise le démarrage à la demande, consultez [exemple de déclenchement de temps (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





