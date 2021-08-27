---
description: vous pouvez déclarer une instance de base d’une classe dans le service de gestion Windows à l’aide de format MOF (MOF). Vous pouvez également remplacer les valeurs par défaut d’une instance. Pour plus d’informations, consultez Définition d’une valeur de propriété d’instance.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Création d’une instance à l’aide de MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05290fd02de80a905e74eeddeb1a04f316901209a97e0e298d038ac2f8888552
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097319"
---
# <a name="creating-an-instance-using-mof"></a>Création d’une instance à l’aide de MOF

vous pouvez déclarer une instance de base d’une classe dans le service de gestion Windows à l’aide de format MOF (MOF). Vous pouvez également remplacer les valeurs par défaut d’une instance. Pour plus d’informations, consultez [définition d’une valeur de propriété d’instance](#setting-an-instance-property-value).

La procédure suivante décrit comment déclarer une instance de base d’une classe à l’aide de code MOF.

**Pour déclarer une instance de base d’une classe à l’aide du code MOF**

1.  Utilisez l' **instance de** Mots clés suivie du nom de la classe, des accolades et d’un point-virgule.

    L’exemple de code suivant montre comment déclarer une instance d’une classe.

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  Lorsque vous avez terminé, insérez votre code MOF dans le référentiel WMI à l’aide du compilateur MOF.

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

Une instance d’une classe comprend toutes les propriétés de la classe. Si la classe est une classe dérivée, les instances incluent les propriétés qui appartiennent à toutes les classes figurant plus haut dans la hiérarchie. Chaque classe à partir de laquelle une instance est créée a une ou plusieurs propriétés de clé. Vous ne pouvez pas créer une instance avec plus de 256 clés.

## <a name="setting-an-instance-property-value"></a>Définition d’une valeur de propriété d’instance

Étant donné que les propriétés de type WMI sont fortement typées, vous ne pouvez pas modifier les types de propriété. Toutefois, vous pouvez définir des valeurs de propriété dans les instances. Quand une classe assigne une valeur par défaut à une propriété, WMI affecte la valeur par défaut à chaque instance. Vous pouvez remplacer cette valeur dans votre déclaration d’instance.

La procédure suivante décrit comment définir une valeur de propriété ou remplacer une valeur par défaut à l’aide du code MOF.

**Pour définir une valeur de propriété ou remplacer une valeur par défaut à l’aide du code MOF**

1.  Placez une instruction d’assignation entre les accolades de la déclaration d’instance.

    L’exemple de code suivant montre comment définir une valeur de propriété.

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    WMI ne nécessite pas de définir de propriété lors de la création de l’instance. L’exception est toute propriété marquée avec le qualificateur de [**clé**](key-qualifier.md) . Étant donné que WMI utilise des propriétés de clé pour identifier de façon unique les instances, vous devez définir toutes les propriétés de clé à mesure que vous les rencontrez. En revanche, vous ne devez pas définir une propriété système dans une déclaration d’instance. Au lieu de cela, WMI affecte les valeurs appropriées à une propriété système si nécessaire.

2.  Lorsque vous avez terminé, insérez votre code MOF dans le référentiel WMI à l’aide d’un appel au compilateur MOF.

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

Les exemples de code suivants montrent comment une instance spécifie des données pour les propriétés définies par une classe.

``` syntax
class MyClass 
{
    [key] string   strProp;
    sint32   dwProp1;
    uint32       dwProp2;
};

instance of MyClass 
{
    strProp = "hello";
    dwProp1 = -1;
    dwProp2 = 0xffffffff;
};
```

Dans l’exemple précédent, la classe définit trois propriétés : une chaîne de caractères, un entier signé 32 bits et un entier 32 bits non signé. L’instance de fournit des valeurs de données pour chacune de ces propriétés.

 

 



