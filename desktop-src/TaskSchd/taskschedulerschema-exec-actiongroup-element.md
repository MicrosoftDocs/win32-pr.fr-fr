---
title: Élément exec (actionGroup)
description: Spécifie une action qui exécute une opération de ligne de commande.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Élément exec Planificateur de tâches
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523113"
---
# <a name="exec-actiongroup-element"></a>Élément exec (actionGroup)

Spécifie une action qui exécute une opération de ligne de commande.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

L’élément **Exec** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                         | Dérivé de                                                       | Description                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Actions**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contient les actions effectuées par la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                           | Type       | Description                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Arguments**](taskschedulerschema-arguments-exectype-element.md)               | **string** | Spécifie les arguments associés à l’opération de ligne de commande.<br/>                               |
| [**Commande**](taskschedulerschema-command-exectype-element.md)                   | **string** | Spécifie le fichier exécutable ou le document à exécuter.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | string     | Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.<br/> |



## <a name="attributes"></a>Attributs



| Nom | Type       | Description                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **string** | Identificateur de l’action exécutée par la tâche.<br/> |



## <a name="remarks"></a>Notes

Les éléments enfants répertoriés ci-dessus sont définis par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .

Pour le développement de scripts, une action d’exécution est définie par l’objet [**ExecAction**](execaction.md) .

Pour le développement C++, une action d’exécution est définie par l’interface [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .

Si les variables d’environnement sont utilisées dans les éléments [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)ou [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , les valeurs des variables d’environnement sont mises en cache et utilisées lors du lancement du Taskeng.exe (le moteur de tâches). Les modifications apportées aux variables d’environnement qui se produisent après le lancement du moteur de tâche ne sont pas utilisées par le moteur de tâche.

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur d’événement, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





