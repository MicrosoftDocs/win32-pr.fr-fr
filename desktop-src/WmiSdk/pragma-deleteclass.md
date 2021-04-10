---
description: Supprime une classe existante et ses instances du référentiel.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868590"
---
# <a name="pragma-deleteclass"></a>pragma deleteclass

La commande de préprocesseur **pragma deleteclass** supprime une classe existante et ses instances du référentiel.

Les éléments suivants décrivent la syntaxe :


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* est le nom de la classe que le compilateur MOF supprime de l’espace de noms actuel.

L' *\[ indicateur \]* doit être l’un des arguments suivants.



| Indicateur   | Description                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| Échec   | Provoque la fermeture du compilateur MOF avec un message d’erreur si la classe n’existe pas déjà dans le référentiel. |
| nofail | Fait en sorte que le compilateur MOF continue même si la classe n’existe pas déjà.                                |



 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser cette commande.


```mof
#pragma deleteclass("MyClass1",FAIL)
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

 

 




