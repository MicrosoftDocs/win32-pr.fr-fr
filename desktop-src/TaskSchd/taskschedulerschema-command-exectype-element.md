---
title: Élément Command (execType)
description: Spécifie le fichier exécutable ou le document à exécuter.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Élément Command Planificateur de tâches
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385076"
---
# <a name="command-exectype-element"></a>Élément Command (execType)

Spécifie le fichier exécutable ou le document à exécuter.

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

L’élément **Command** est défini par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                      | Dérivé de                                                 | Description                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exécutable**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Spécifie une action qui exécute une opération de ligne de commande.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Pour le développement de scripts, consultez [**ExecAction. arguments**](execaction-arguments.md).

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise une action exécutable, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





