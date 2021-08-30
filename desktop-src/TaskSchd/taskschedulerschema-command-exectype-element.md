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
ms.openlocfilehash: 8fa76e0d3a826e5a4fb5eabbe2346de82efbcbf0f60324bb73976487f43a4698
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100059"
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



## <a name="remarks"></a>Remarques

Pour le développement C++, consultez la [**propriété arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Pour le développement de scripts, consultez [**ExecAction. arguments**](execaction-arguments.md).

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise une action exécutable, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





