---
description: Indique au compilateur MOF de séparer un fichier MOF en versions indépendantes du langage et spécifiques à la langue.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: Amendement pragma
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
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753700"
---
# <a name="pragma-amendment"></a>Amendement pragma

La commande de préprocesseur **pragma avenant** indique au compilateur MOF de séparer un fichier MOF en versions indépendantes du langage et spécifiques à la langue. Le fichier MOF propre au langage déplace les qualificateurs modifiés vers un espace de noms pour des paramètres régionaux spécifiques. Vous compilez ensuite les fichiers MOF propres au langage et à la langue pour stocker les informations de classe dans le référentiel WMI.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment créer un fichier MOF qui contient des qualificateurs modifiés. Vous pouvez ensuite compiler le code MOF avec la commande suivante :

**mofcomp** **-MOF : Lnmof. mof** **-MFL : Lsmof. MFL** **Mastermof. mof**

La commande indique au compilateur MOF de générer deux fichiers MOF à partir du fichier Mastermof. mof d’origine. Le compilateur MOF produit une version indépendante du langage du fichier MOF, appelée Lnmof. mof, avec tous les éléments spécifiques à la langue supprimés. Le compilateur crée également un second fichier MOF propre au langage appelé Lsmof. MFL qui contient uniquement les éléments que vous devez localiser.

> [!Note]  
> Lorsque vous fractionnez un fichier MOF avec le qualificateur d' **Amendement** ou la commande **pragma avenant** , vous devez spécifier les options **-MOF** et **-MFL** . Sinon, le compilateur ne génère pas de fichiers de sortie. Vous devez ensuite compiler les deux fichiers de sortie pour rendre les informations de classe disponibles pour WMI.

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
{
     [DisplayName("User Name") : Amended,
     Description("The Name property contains the name of the user") : 
     Amended, key]
    string Name;

    uint64 Value; // non-localized value field

     [DisplayName("Time Stamp") : Amended,
     Description("This property shows when the object was created") : 
     Amended] 
    uint64 Timestamp;
};
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

 

 




