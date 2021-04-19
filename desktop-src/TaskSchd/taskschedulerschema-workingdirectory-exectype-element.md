---
title: Élément WorkingDirectory (execType)
description: Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Élément WorkingDirectory Planificateur de tâches
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514867"
---
# <a name="workingdirectory-exectype-element"></a>Élément WorkingDirectory (execType)

Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

L’élément **WorkingDirectory** est défini par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                      | Dérivé de                                                 | Description                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exécutable**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Spécifie une action qui exécute une opération de ligne de commande.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, le répertoire de travail est spécifié par la propriété [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) .

Pour le développement C++, le répertoire de travail est spécifié par la propriété [**IExecAction :: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .

## <a name="examples"></a>Exemples

Le code XML suivant définit une action d’exécution.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
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

 

 





