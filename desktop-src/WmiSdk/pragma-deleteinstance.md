---
description: Supprime une instance existante d’une classe du référentiel.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma DeleteInstance
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
ms.openlocfilehash: 29739f1d95cf5c8352c2b7822dbc3da7777f41f69fc5086631e0069c3b832623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316842"
---
# <a name="pragma-deleteinstance"></a>pragma DeleteInstance

La commande **pragma DeleteInstance** supprime une instance existante d’une classe du référentiel.

La syntaxe de cette commande est décrite ci-dessous :


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceID* est un identificateur unique de l’instance que le compilateur MOF supprime de l’espace de noms actuel.

L' *\[ indicateur \]* doit être l’un des arguments suivants.



| Indicateur   | Description                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| Échec   | Provoque la fermeture du compilateur MOF avec un message d’erreur si la classe n’existe pas déjà dans le référentiel. |
| nofail | Fait en sorte que le compilateur MOF continue même si la classe n’existe pas déjà.                                |



 

## <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser cette commande.


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
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

 

 




