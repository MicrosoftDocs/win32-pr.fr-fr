---
description: Contrôle la manière dont WMI crée ou met à jour des classes en fonction des indicateurs spécifiés.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6fd2b8ec75bd0521ce31af1ee7ce9dba2d9498890f9b5ddc768463f733322cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996319"
---
# <a name="pragma-classflags"></a>pragma classflags

La commande de préprocesseur **pragma classflags** contrôle la manière dont WMI crée ou met à jour des classes en fonction des indicateurs spécifiés.

La syntaxe de cette commande est décrite ci-dessous :


```mof
#pragma classflags ("[flag1], [flag2]")
```



L' *\[ indicateur \]* doit être un ou plusieurs des arguments suivants. Vous pouvez combiner tous les indicateurs qui ne sont pas contradictoires.



| Indicateur        | Description                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CreateOnly  | Indique au compilateur de ne pas apporter de modifications aux classes existantes et met fin à une compilation si une classe spécifiée dans le fichier MOF existe déjà dans WMI.                                                                                                                                                                                                        |
| ForceUpdate | Force les mises à jour des classes lorsque des classes enfants sont en conflit. Par exemple, si vous définissez un qualificateur de classe dans une classe enfant et que la classe de base tente d’ajouter le même qualificateur, l’utilisation de cet indicateur force le compilateur à résoudre ce conflit en supprimant le qualificateur en conflit dans la classe enfant. Si la classe enfant a des instances, la mise à jour échoue. |
| safeupdate  | Permet au compilateur de mettre à jour des classes même si des classes enfants existent, si la modification ne provoque pas de conflits avec les classes enfants. Par exemple, cet indicateur vous permet d’ajouter une nouvelle propriété à une classe de base sans avoir à ajouter la propriété à une classe enfant préexistante. Si les classes enfants ont des instances, la mise à jour échoue.                           |
| updateonly  | Indique au compilateur de ne pas créer de nouvelles classes et force le compilateur à arrêter la compilation si une classe spécifiée dans le fichier MOF n’existe pas.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser cette commande avec les indicateurs updateonly et ForceUpdate.


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Commandes de préprocesseur](preprocessor-commands.md)
</dt> </dl>

 

 




