---
description: Pour créer une méthode WMI, définissez les paramètres d’entrée et de sortie de la méthode.
ms.assetid: 71cbecde-33c4-4bf1-9793-bef6d823dcac
ms.tgt_platform: multiple
title: Création d’une méthode WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2489a5dd4e97ed6c8d26eeb292c45fa66901cbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210213"
---
# <a name="creating-a-wmi-method"></a>Création d’une méthode WMI

Pour créer une méthode WMI, définissez les paramètres d’entrée et de sortie de la méthode. Les paramètres d’entrée et de sortie sont représentés par des [**\_ \_ paramètres**](--parameters.md)de classe système WMI spéciaux. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [écriture d’un fournisseur de méthode](writing-a-method-provider.md).

Les sections suivantes sont présentées dans cette rubrique :

-   [Création d’une méthode de classe WMI dans MOF](#creating-a-wmi-class-method-in-mof)
-   [Création d’une méthode de classe WMI en C++](#creating-a-wmi-class-method-in-c)
-   [Rubriques connexes](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a>Création d’une méthode de classe WMI dans MOF

Dans WMI, les méthodes de fournisseur sont généralement des actions distinctes en rapport avec l’objet représenté par la classe. Au lieu de modifier la valeur d’une propriété pour exécuter une action, une méthode doit être créée. Par exemple, vous pouvez activer ou désactiver un centre d’informations réseau (NIC) qui est représenté par la carte réseau [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter) à l’aide des méthodes [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) et [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) . Si ces actions peuvent être représentées en tant que propriété en lecture/écriture, la conception recommandée consiste à créer une méthode. Sinon, si vous souhaitez rendre un État ou une valeur visible pour la classe, l’approche recommandée consiste à créer une propriété en lecture/écriture plutôt qu’une méthode. Dans **Win32 \_ NetworkAdapter**, la propriété **NetEnabled** rend l’état de l’adaptateur visible, mais les modifications entre les États sont exécutées par les méthodes d' **activation** ou de **désactivation** .

Les déclarations de classe peuvent inclure la déclaration d’une ou plusieurs méthodes. Vous pouvez soit choisir d’hériter des méthodes d’une classe parente, soit implémenter la vôtre. Si vous choisissez d’implémenter vos propres méthodes, vous devez déclarer la méthode et marquer la méthode avec des balises de qualificateur spécifiques.

La procédure suivante décrit comment déclarer une méthode dans une classe qui n’hérite pas d’une classe de base.

**Pour déclarer une méthode**

1.  Définissez le nom de votre méthode entre les accolades d’une déclaration de classe, suivi de tous les qualificateurs.

    L’exemple de code suivant décrit la syntaxe d’une méthode.

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  Lorsque vous avez terminé, insérez votre code format MOF (MOF) dans le référentiel WMI à l’aide d’un appel au compilateur MOF.

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

La liste suivante définit les éléments de la déclaration de méthode.

<dl> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Moteur**](/windows/desktop/api/Provider/nl-provider-provider)
</dt> <dd>

Lie un fournisseur spécifique à votre description de classe. La valeur du qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) est le nom du fournisseur, qui indique à WMI où se trouve le code qui prend en charge votre méthode. Un fournisseur doit également marquer avec le qualificateur **dynamique** toute classe qui a des instances dynamiques. En revanche, n’utilisez pas le qualificateur **Dynamic** pour marquer une classe qui contient une instance statique avec des méthodes **implémentées** .

</dd> <dt>

<span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Été**
</dt> <dd>

Déclare que vous allez implémenter une méthode, plutôt que d’hériter de l’implémentation de la méthode de la classe parente. Par défaut, WMI propage l’implémentation de la classe parente à une classe dérivée, à moins que la classe dérivée fournisse une implémentation. Si vous omettez le qualificateur **Implemented** , cela signifie que la méthode n’a aucune implémentation dans cette classe. Si vous redéclarez une méthode sans qualificateur **implémenté** , WMI suppose toujours que vous n’allez pas implémenter cette méthode et appelle l’implémentation de la méthode de la classe parente quand elle est appelée. Ainsi, la redéclaration d’une méthode dans une classe dérivée sans attacher le qualificateur **implémenté** n’est utile que lorsque vous ajoutez ou supprimez un qualificateur vers ou à partir de la méthode.

</dd> <dt>

<span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType
</dt> <dd>

Décrit la valeur retournée par la méthode. La valeur de retour d’une méthode doit être un objet booléen, numérique, **char**, **String**, [DateTime](datetime.md)ou Schema. Vous pouvez également déclarer le type de retour comme [void](void.md), ce qui indique que la méthode ne retourne rien. Toutefois, vous ne pouvez pas déclarer un tableau en tant que type de valeur de retour.

</dd> <dt>

<span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName
</dt> <dd>

Définit le nom de la méthode. Chaque méthode doit avoir un nom unique. WMI n’autorise pas l’existence de deux méthodes ayant le même nom et des signatures différentes dans une classe ou dans une hiérarchie de classes. Par conséquent, vous ne pouvez pas non plus surcharger une méthode.

</dd> <dt>

<span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection
</dt> <dd>

Contient des qualificateurs qui décrivent si un paramètre est un paramètre d’entrée, un paramètre de sortie, ou les deux. N’utilisez pas le même nom de paramètre plus d’une fois en tant que paramètre d’entrée ou plusieurs fois en tant que paramètre de sortie. Si le même nom de paramètre apparaît avec les qualificateurs [**in**](standard-qualifiers.md) et **out** , la fonctionnalité est conceptuellement identique à l’utilisation des qualificateurs **in**, **out** sur un paramètre unique. Toutefois, lorsque vous utilisez des déclarations distinctes, les paramètres d’entrée et de sortie doivent être exactement les mêmes à tous les autres égards, y compris le nombre et le type des qualificateurs d' [**ID**](standard-wmi-qualifiers.md) , et le qualificateur doit être identique et déclaré explicitement pour les deux. Il est fortement recommandé d’utiliser les qualificateurs **in**, **out** dans une déclaration de paramètre unique.

</dd> <dt>

<span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**
</dt> <dd>

Contient le qualificateur d' [**ID**](standard-wmi-qualifiers.md) qui identifie de façon unique la position de chaque paramètre dans la séquence de paramètres de la méthode. Par défaut, le compilateur MOF marque automatiquement les paramètres avec un qualificateur d' **ID** . Le compilateur marque le premier paramètre avec la valeur 0 (zéro), le deuxième paramètre a la valeur 1 (un), et ainsi de suite. Si nécessaire, vous pouvez déclarer explicitement la séquence d’ID dans votre code MOF.

</dd> <dt>

<span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType
</dt> <dd>

Décrit le type de données que la méthode peut accepter. Vous pouvez définir un type de paramètre comme n’importe quelle valeur de données MOF, y compris un tableau, un objet de schéma ou une référence. Lors de l’utilisation d’un tableau en tant que paramètre, utilisez le tableau comme non lié ou avec une taille explicite.

</dd> <dt>

<span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName
</dt> <dd>

Contient le nom du paramètre. Vous pouvez également choisir de définir la valeur par défaut du paramètre à ce stade. Les paramètres qui n’ont pas de valeurs initiales restent non assignés.

</dd> </dl>

L’exemple de code suivant décrit la liste des paramètres et les qualificateurs.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] sint32 InParam);
    [Implemented] 
    void MyMethod2 ([in, id(0)] sint32 InParam, 
       [out, id(1)] sint32 OutParam);
    [Implemented] 
    sint32 MyMethod3 ([in, out, id(0)] sint32 InOutParam);
};
```

L’exemple de code suivant décrit comment utiliser un tableau dans un paramètre MOF.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskParam[]);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskParam[32]);
};
```

L’exemple de code suivant décrit l’utilisation d’un objet de schéma en tant que paramètre et valeur de retour.

``` syntax
[Dynamic, Provider ("ProviderX")]
class MyClass
{
    [Implemented] sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk 
        DiskParam);
    [Implemented] 
    Win32_LogicalDisk MyMethod2 ([in, id(0)] string DiskVolLabel);
};
```

L’exemple de code suivant décrit comment inclure deux références : une à une instance de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) et l’autre à une instance d’un type d’objet inconnu.

``` syntax
[Dynamic, Provider("ProviderX")]
class MyClass
{
    [Implemented] 
    sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk ref DiskRef);
    [Implemented] 
    sint32 MyMethod2 ([in, id(0)] object ref AnyObject);
};
```

## <a name="creating-a-wmi-class-method-in-c"></a>Création d’une méthode de classe WMI en C++

La procédure suivante décrit comment créer une méthode de classe WMI par programme.

**Pour créer une méthode de classe WMI par programmation**

1.  Créez la classe à laquelle la méthode appartiendra.

    Vous devez d’abord avoir une classe dans laquelle placer la méthode avant de créer la méthode.

2.  Récupérez deux classes enfants de la classe de système de [**\_ \_ paramètres**](--parameters.md) à l’aide de [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Utilisez la première classe enfant pour décrire les paramètres in-et la seconde pour décrire les paramètres out. Si nécessaire, vous pouvez effectuer une récupération unique suivie d’un appel à la méthode [**IWbemClassObject :: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .

3.  Écrivez les paramètres in-dans la première classe, et les paramètres out dans la deuxième classe, à l’aide d’un ou plusieurs appels à [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Lors de la description des paramètres d’une méthode, observez les règles et restrictions suivantes :

    -   Traitez les \[ paramètres in, out \] en tant qu’entrées distinctes, l’un dans l’objet qui contient les paramètres in et l’autre dans l’objet qui contient les paramètres out.
    -   \[En dehors des qualificateurs out, les qualificateurs \] restants doivent être exactement les mêmes.
    -   Spécifiez les qualificateurs d' [**ID**](standard-wmi-qualifiers.md) , en commençant à 0 (zéro), un pour chaque paramètre.

        L’ordre des paramètres d’entrée ou de sortie est établi par la valeur du qualificateur d' [**ID**](standard-wmi-qualifiers.md) sur chaque paramètre. Tous les arguments d’entrée doivent précéder les arguments de sortie. La modification de l’ordre des paramètres d’entrée et de sortie de la méthode lors de la mise à jour d’un fournisseur de méthode existant peut entraîner l’échec des applications qui appellent la méthode. Ajoutez de nouveaux paramètres d’entrée à la fin des paramètres existants au lieu de les insérer dans la séquence déjà établie.

        Veillez à ne pas définir d’écart dans la séquence de qualificateur d' [**ID**](standard-wmi-qualifiers.md) .

    -   Placez la valeur de retour dans la classe out-Parameters en tant que propriété nommée **returnValue**.

        Cela identifie la propriété en tant que valeur de retour de la méthode. Le type CIM de cette propriété est le type de retour de la méthode. Si la méthode a un type de retour void, alors n’avez aucune propriété **returnValue** . En outre, la propriété **returnValue** ne peut pas avoir un qualificateur d' [**ID**](standard-wmi-qualifiers.md) comme les arguments de la méthode. L’affectation d’un qualificateur d' **ID** à la propriété **returnValue** génère une erreur WMI.

    -   Exprimez toutes les valeurs de paramètre par défaut pour la propriété dans la classe.

4.  Placez les deux objets de [**\_ \_ paramètres**](--parameters.md) dans la classe parente à l’aide d’un appel à [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

    Un seul appel à [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) peut placer les deux objets de [**\_ \_ paramètres**](--parameters.md) dans la classe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une classe](creating-a-class.md)
</dt> </dl>

 

 
