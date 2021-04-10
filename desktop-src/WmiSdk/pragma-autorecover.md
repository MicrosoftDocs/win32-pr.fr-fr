---
description: Ajoute un fichier MOF à la liste des fichiers compilés au cours de la récupération du référentiel.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma AutoRecover
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
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952684"
---
# <a name="pragma-autorecover"></a>pragma AutoRecover

La commande de préprocesseur **pragma AutoRecover** ajoute un fichier MOF à la liste des fichiers compilés au cours de la récupération du référentiel. La liste des fichiers MOF de **récupération automatique** est stockée dans cette clé de Registre :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM**- \\ **récupération automatique (MOF** )

WMI vérifie l’intégrité de l’espace de stockage WMI lorsque le système d’exploitation démarre WMI. Si le référentiel est endommagé, WMI reconstruit automatiquement le référentiel et RECOMPILE tous les fichiers MOF listés dans cette clé dans le registre.

La syntaxe de la commande pragma autoautorecover est décrite ci-dessous :


```mof
#pragma autorecover
```



Toutefois, vous devez respecter les restrictions suivantes lors de l’utilisation de cette commande :

-   WMI ne peut pas récupérer les fichiers MOF situés sur un ordinateur distant.

    Par conséquent, les fichiers MOF listés dans cette clé de Registre doivent résider sur l’ordinateur local.

-   Vous ne pouvez pas spécifier les commutateurs de ligne de commande que le compilateur MOF utilise lorsque WMI récupère un fichier MOF.

    Par conséquent, vous devez inclure dans votre fichier MOF des commandes [pragma](-pragma.md) qui rendent les commutateurs de ligne de commande inutiles. L’exemple suivant décrit un commutateur de ligne de commande courant que WMI n’utilise pas lors de la récupération d’un fichier MOF à partir de cette clé de Registre : **mofcomp-N :root \\ test mymof. mof**

    Toutefois, vous pouvez spécifier l’espace de noms à l’aide d’une commande [pragma](-pragma.md) dans le fichier MOF.

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
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

 

 




