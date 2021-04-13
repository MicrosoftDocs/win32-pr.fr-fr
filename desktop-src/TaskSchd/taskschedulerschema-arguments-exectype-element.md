---
title: Argument (execType), élément
description: Spécifie les arguments associés à l’opération de ligne de commande.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Arguments, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508853"
---
# <a name="arguments-exectype-element"></a>Argument (execType), élément

Spécifie les arguments associés à l’opération de ligne de commande.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

L’élément **arguments** est défini par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .

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

 

 





