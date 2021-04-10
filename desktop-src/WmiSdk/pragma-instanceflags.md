---
description: Contrôle la façon dont les instances sont créées ou mises à jour en fonction des indicateurs spécifiés.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210562"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

La commande de préprocesseur **pragma instanceflags** contrôle la manière dont les instances sont créées ou mises à jour en fonction des indicateurs spécifiés.

Les éléments suivants décrivent la syntaxe :


```mof
#pragma instanceflags ([Flag])
```



L' *\[ indicateur \]* doit être l’un des arguments suivants.



| Indicateur       | Description                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| CreateOnly | Empêche le compilateur de modifier les instances existantes dans le fichier MOF.                                |
| updateonly | Empêche le compilateur de créer de nouvelles instances si une instance spécifiée dans le fichier MOF n’existe pas. |



 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser cette commande.


```mof
#pragma instanceflags("createonly")
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

 

 




