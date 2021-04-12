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
# <a name="creating-a-wmi-method"></a><span data-ttu-id="1c6f2-103">Création d’une méthode WMI</span><span class="sxs-lookup"><span data-stu-id="1c6f2-103">Creating a WMI Method</span></span>

<span data-ttu-id="1c6f2-104">Pour créer une méthode WMI, définissez les paramètres d’entrée et de sortie de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-104">To create a WMI method, define the input and output parameters for the method.</span></span> <span data-ttu-id="1c6f2-105">Les paramètres d’entrée et de sortie sont représentés par des [**\_ \_ paramètres**](--parameters.md)de classe système WMI spéciaux.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-105">The input and output parameters are represented by a special WMI system class [**\_\_PARAMETERS**](--parameters.md).</span></span> <span data-ttu-id="1c6f2-106">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md) et [écriture d’un fournisseur de méthode](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-106">For more information, see [Calling a Method](calling-a-method.md) and [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="1c6f2-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="1c6f2-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="1c6f2-108">Création d’une méthode de classe WMI dans MOF</span><span class="sxs-lookup"><span data-stu-id="1c6f2-108">Creating a WMI Class Method in MOF</span></span>](#creating-a-wmi-class-method-in-mof)
-   [<span data-ttu-id="1c6f2-109">Création d’une méthode de classe WMI en C++</span><span class="sxs-lookup"><span data-stu-id="1c6f2-109">Creating a WMI Class Method in C++</span></span>](#creating-a-wmi-class-method-in-c)
-   [<span data-ttu-id="1c6f2-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c6f2-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-wmi-class-method-in-mof"></a><span data-ttu-id="1c6f2-111">Création d’une méthode de classe WMI dans MOF</span><span class="sxs-lookup"><span data-stu-id="1c6f2-111">Creating a WMI Class Method in MOF</span></span>

<span data-ttu-id="1c6f2-112">Dans WMI, les méthodes de fournisseur sont généralement des actions distinctes en rapport avec l’objet représenté par la classe.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-112">In WMI, provider methods are generally distinct actions related to the object that the class represents.</span></span> <span data-ttu-id="1c6f2-113">Au lieu de modifier la valeur d’une propriété pour exécuter une action, une méthode doit être créée.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-113">Rather than change the value of a property to execute an action, a method should be created.</span></span> <span data-ttu-id="1c6f2-114">Par exemple, vous pouvez activer ou désactiver un centre d’informations réseau (NIC) qui est représenté par la carte réseau [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-networkadapter) à l’aide des méthodes [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) et [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) .</span><span class="sxs-lookup"><span data-stu-id="1c6f2-114">For example, you can enable or disable a network information center (NIC) that is represented by [**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) by using the [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) and [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) methods.</span></span> <span data-ttu-id="1c6f2-115">Si ces actions peuvent être représentées en tant que propriété en lecture/écriture, la conception recommandée consiste à créer une méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-115">While these actions can be represented as a read/write property, the recommended design is to create a method.</span></span> <span data-ttu-id="1c6f2-116">Sinon, si vous souhaitez rendre un État ou une valeur visible pour la classe, l’approche recommandée consiste à créer une propriété en lecture/écriture plutôt qu’une méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-116">Alternatively, if you want to make a state or value visible for the class, then the recommended approach is to create a read/write property rather than a method.</span></span> <span data-ttu-id="1c6f2-117">Dans **Win32 \_ NetworkAdapter**, la propriété **NetEnabled** rend l’état de l’adaptateur visible, mais les modifications entre les États sont exécutées par les méthodes d' **activation** ou de **désactivation** .</span><span class="sxs-lookup"><span data-stu-id="1c6f2-117">In **Win32\_NetworkAdapter**, the **NetEnabled** property makes the state of the adapter visible but changes between states are executed by the **Enable** or **Disable** methods.</span></span>

<span data-ttu-id="1c6f2-118">Les déclarations de classe peuvent inclure la déclaration d’une ou plusieurs méthodes.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-118">Class declarations can include the declaration of one or more methods.</span></span> <span data-ttu-id="1c6f2-119">Vous pouvez soit choisir d’hériter des méthodes d’une classe parente, soit implémenter la vôtre.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-119">You can either choose to inherit the methods of a parent class, or implement your own.</span></span> <span data-ttu-id="1c6f2-120">Si vous choisissez d’implémenter vos propres méthodes, vous devez déclarer la méthode et marquer la méthode avec des balises de qualificateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-120">If you choose to implement your own methods, you must declare the method and mark the method with specific qualifier tags.</span></span>

<span data-ttu-id="1c6f2-121">La procédure suivante décrit comment déclarer une méthode dans une classe qui n’hérite pas d’une classe de base.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-121">The following procedure describes how to declare a method in a class that does not inherit from a base class.</span></span>

<span data-ttu-id="1c6f2-122">**Pour déclarer une méthode**</span><span class="sxs-lookup"><span data-stu-id="1c6f2-122">**To declare a method**</span></span>

1.  <span data-ttu-id="1c6f2-123">Définissez le nom de votre méthode entre les accolades d’une déclaration de classe, suivi de tous les qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-123">Define the name of your method between the curly braces of a class declaration, followed by any qualifiers.</span></span>

    <span data-ttu-id="1c6f2-124">L’exemple de code suivant décrit la syntaxe d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-124">The following code example describes the syntax for a method.</span></span>

    ``` syntax
    [Dynamic, Provider ("ProviderName")]
    class ClassName
    {
        [Implemented] <ReturnType> <MethodName>
            ([ParameterDirection, IDQualifier] 
            <ParameterType> <ParameterName>);
    };
    ```

2.  <span data-ttu-id="1c6f2-125">Lorsque vous avez terminé, insérez votre code format MOF (MOF) dans le référentiel WMI à l’aide d’un appel au compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-125">When finished, insert your Managed Object Format (MOF) code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="1c6f2-126">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-126">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="1c6f2-127">La liste suivante définit les éléments de la déclaration de méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-127">The following list defines the elements of the method declaration.</span></span>

<dl> <dt>

<span data-ttu-id="1c6f2-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Moteur**](/windows/desktop/api/Provider/nl-provider-provider)</span><span class="sxs-lookup"><span data-stu-id="1c6f2-128"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>[**Provider**](/windows/desktop/api/Provider/nl-provider-provider)</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-129">Lie un fournisseur spécifique à votre description de classe.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-129">Links a specific provider to your class description.</span></span> <span data-ttu-id="1c6f2-130">La valeur du qualificateur du [**fournisseur**](/windows/desktop/api/Provider/nl-provider-provider) est le nom du fournisseur, qui indique à WMI où se trouve le code qui prend en charge votre méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-130">The value of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier is the name of the provider, which tells WMI where the code that supports your method resides.</span></span> <span data-ttu-id="1c6f2-131">Un fournisseur doit également marquer avec le qualificateur **dynamique** toute classe qui a des instances dynamiques.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-131">A provider should also mark with the **Dynamic** qualifier any class that has dynamic instances.</span></span> <span data-ttu-id="1c6f2-132">En revanche, n’utilisez pas le qualificateur **Dynamic** pour marquer une classe qui contient une instance statique avec des méthodes **implémentées** .</span><span class="sxs-lookup"><span data-stu-id="1c6f2-132">In contrast, do not use the **Dynamic** qualifier to mark a class that contains a static instance with **Implemented** methods.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f2-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Été**</span><span class="sxs-lookup"><span data-stu-id="1c6f2-133"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-134">Déclare que vous allez implémenter une méthode, plutôt que d’hériter de l’implémentation de la méthode de la classe parente.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-134">Declares that you will implement a method, rather than inherit the method implementation from the parent class.</span></span> <span data-ttu-id="1c6f2-135">Par défaut, WMI propage l’implémentation de la classe parente à une classe dérivée, à moins que la classe dérivée fournisse une implémentation.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-135">By default, WMI propagates the implementation of the parent class to a derived class unless the derived class provides an implementation.</span></span> <span data-ttu-id="1c6f2-136">Si vous omettez le qualificateur **Implemented** , cela signifie que la méthode n’a aucune implémentation dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-136">Omitting the **Implemented** qualifier indicates that the method has no implementation in that class.</span></span> <span data-ttu-id="1c6f2-137">Si vous redéclarez une méthode sans qualificateur **implémenté** , WMI suppose toujours que vous n’allez pas implémenter cette méthode et appelle l’implémentation de la méthode de la classe parente quand elle est appelée.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-137">If you redeclare a method without the **Implemented** qualifier, WMI still assumes that you are not going to implement that method, and invokes the parent class method implementation when called.</span></span> <span data-ttu-id="1c6f2-138">Ainsi, la redéclaration d’une méthode dans une classe dérivée sans attacher le qualificateur **implémenté** n’est utile que lorsque vous ajoutez ou supprimez un qualificateur vers ou à partir de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-138">As such, redeclaring a method in a derived class without attaching the **Implemented** qualifier is useful only when you add or remove a qualifier to or from the method.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f2-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span><span class="sxs-lookup"><span data-stu-id="1c6f2-139"><span id="ReturnType"></span><span id="returntype"></span><span id="RETURNTYPE"></span>ReturnType</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-140">Décrit la valeur retournée par la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-140">Describes what value the method returns.</span></span> <span data-ttu-id="1c6f2-141">La valeur de retour d’une méthode doit être un objet booléen, numérique, **char**, **String**, [DateTime](datetime.md)ou Schema.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-141">The return value for a method must be a Boolean, numeric, **CHAR**, **STRING**, [DATETIME](datetime.md), or schema object.</span></span> <span data-ttu-id="1c6f2-142">Vous pouvez également déclarer le type de retour comme [void](void.md), ce qui indique que la méthode ne retourne rien.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-142">You can also declare the return type as [VOID](void.md), indicating that the method returns nothing.</span></span> <span data-ttu-id="1c6f2-143">Toutefois, vous ne pouvez pas déclarer un tableau en tant que type de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-143">However, you cannot declare an array as a return value type.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f2-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span><span class="sxs-lookup"><span data-stu-id="1c6f2-144"><span id="MethodName"></span><span id="methodname"></span><span id="METHODNAME"></span>MethodName</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-145">Définit le nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-145">Defines the name of the method.</span></span> <span data-ttu-id="1c6f2-146">Chaque méthode doit avoir un nom unique.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-146">Every method must have a unique name.</span></span> <span data-ttu-id="1c6f2-147">WMI n’autorise pas l’existence de deux méthodes ayant le même nom et des signatures différentes dans une classe ou dans une hiérarchie de classes.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-147">WMI does not allow two methods with the same name and different signatures to exist in one class or within a class hierarchy.</span></span> <span data-ttu-id="1c6f2-148">Par conséquent, vous ne pouvez pas non plus surcharger une méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-148">As such, you also cannot overload a method.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f2-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="1c6f2-149"><span id="ParameterDirection"></span><span id="parameterdirection"></span><span id="PARAMETERDIRECTION"></span>ParameterDirection</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-150">Contient des qualificateurs qui décrivent si un paramètre est un paramètre d’entrée, un paramètre de sortie, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-150">Contains qualifiers that describe if a parameter is an input parameter, output parameter, or both.</span></span> <span data-ttu-id="1c6f2-151">N’utilisez pas le même nom de paramètre plus d’une fois en tant que paramètre d’entrée ou plusieurs fois en tant que paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-151">Do not use the same parameter name more than one time as an input parameter or more than one time as an output parameter.</span></span> <span data-ttu-id="1c6f2-152">Si le même nom de paramètre apparaît avec les qualificateurs [**in**](standard-qualifiers.md) et **out** , la fonctionnalité est conceptuellement identique à l’utilisation des qualificateurs **in**, **out** sur un paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-152">If the same parameter name appears with both the [**In**](standard-qualifiers.md) and an **Out** qualifiers, the functionality is conceptually the same as using the **In**, **Out** qualifiers on a single parameter.</span></span> <span data-ttu-id="1c6f2-153">Toutefois, lorsque vous utilisez des déclarations distinctes, les paramètres d’entrée et de sortie doivent être exactement les mêmes à tous les autres égards, y compris le nombre et le type des qualificateurs d' [**ID**](standard-wmi-qualifiers.md) , et le qualificateur doit être identique et déclaré explicitement pour les deux.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-153">However, when using separate declarations, the input and output parameters must be exactly the same in all other respects, including the number and type of [**ID**](standard-wmi-qualifiers.md) qualifiers, and the qualifier must be the same and explicitly declared for both.</span></span> <span data-ttu-id="1c6f2-154">Il est fortement recommandé d’utiliser les qualificateurs **in**, **out** dans une déclaration de paramètre unique.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-154">It is strongly recommended to use the **In**, **Out** qualifiers within a single parameter declaration.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f2-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span><span class="sxs-lookup"><span data-stu-id="1c6f2-155"><span id="IDQualifier"></span><span id="idqualifier"></span><span id="IDQUALIFIER"></span>**IDQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-156">Contient le qualificateur d' [**ID**](standard-wmi-qualifiers.md) qui identifie de façon unique la position de chaque paramètre dans la séquence de paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-156">Contains the [**ID**](standard-wmi-qualifiers.md) qualifier that uniquely identifies the position of each parameter within the sequence of parameters in the method.</span></span> <span data-ttu-id="1c6f2-157">Par défaut, le compilateur MOF marque automatiquement les paramètres avec un qualificateur d' **ID** .</span><span class="sxs-lookup"><span data-stu-id="1c6f2-157">By default, the MOF compiler automatically marks parameters with an **ID** qualifier.</span></span> <span data-ttu-id="1c6f2-158">Le compilateur marque le premier paramètre avec la valeur 0 (zéro), le deuxième paramètre a la valeur 1 (un), et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-158">The compiler marks the first parameter with a value of 0 (zero), the second parameter a value of 1 (one), and so on.</span></span> <span data-ttu-id="1c6f2-159">Si nécessaire, vous pouvez déclarer explicitement la séquence d’ID dans votre code MOF.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-159">If necessary, you can explicitly state the ID sequence in your MOF code.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f2-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span><span class="sxs-lookup"><span data-stu-id="1c6f2-160"><span id="ParameterType"></span><span id="parametertype"></span><span id="PARAMETERTYPE"></span>ParameterType</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-161">Décrit le type de données que la méthode peut accepter.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-161">Describes what data type the method can accept.</span></span> <span data-ttu-id="1c6f2-162">Vous pouvez définir un type de paramètre comme n’importe quelle valeur de données MOF, y compris un tableau, un objet de schéma ou une référence.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-162">You can define a parameter type as any MOF data value, including an array, schema object, or reference.</span></span> <span data-ttu-id="1c6f2-163">Lors de l’utilisation d’un tableau en tant que paramètre, utilisez le tableau comme non lié ou avec une taille explicite.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-163">When using an array as a parameter, use the array as unbound or with an explicit size.</span></span>

</dd> <dt>

<span data-ttu-id="1c6f2-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span><span class="sxs-lookup"><span data-stu-id="1c6f2-164"><span id="ParameterName"></span><span id="parametername"></span><span id="PARAMETERNAME"></span>ParameterName</span></span>
</dt> <dd>

<span data-ttu-id="1c6f2-165">Contient le nom du paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-165">Contains the name of the parameter.</span></span> <span data-ttu-id="1c6f2-166">Vous pouvez également choisir de définir la valeur par défaut du paramètre à ce stade.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-166">You can also choose to define the default value of the parameter at this point.</span></span> <span data-ttu-id="1c6f2-167">Les paramètres qui n’ont pas de valeurs initiales restent non assignés.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-167">Parameters lacking initial values remain unassigned.</span></span>

</dd> </dl>

<span data-ttu-id="1c6f2-168">L’exemple de code suivant décrit la liste des paramètres et les qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-168">The following code example describes parameter listing and qualifiers.</span></span>

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

<span data-ttu-id="1c6f2-169">L’exemple de code suivant décrit comment utiliser un tableau dans un paramètre MOF.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-169">The following code example describes how to use an array in a MOF parameter.</span></span>

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

<span data-ttu-id="1c6f2-170">L’exemple de code suivant décrit l’utilisation d’un objet de schéma en tant que paramètre et valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-170">The following code example describes using a schema object as both a parameter and return value.</span></span>

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

<span data-ttu-id="1c6f2-171">L’exemple de code suivant décrit comment inclure deux références : une à une instance de la [**classe \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) et l’autre à une instance d’un type d’objet inconnu.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-171">The following code example describes how to include two references: one to an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and the other to an instance of an unknown object type.</span></span>

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

## <a name="creating-a-wmi-class-method-in-c"></a><span data-ttu-id="1c6f2-172">Création d’une méthode de classe WMI en C++</span><span class="sxs-lookup"><span data-stu-id="1c6f2-172">Creating a WMI Class Method in C++</span></span>

<span data-ttu-id="1c6f2-173">La procédure suivante décrit comment créer une méthode de classe WMI par programme.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-173">The following procedure describes how to create a WMI class method programmatically.</span></span>

<span data-ttu-id="1c6f2-174">**Pour créer une méthode de classe WMI par programmation**</span><span class="sxs-lookup"><span data-stu-id="1c6f2-174">**To create a WMI class method programmatically**</span></span>

1.  <span data-ttu-id="1c6f2-175">Créez la classe à laquelle la méthode appartiendra.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-175">Create the class to which the method will belong.</span></span>

    <span data-ttu-id="1c6f2-176">Vous devez d’abord avoir une classe dans laquelle placer la méthode avant de créer la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-176">You must first have a class to place the method in before you create the method.</span></span>

2.  <span data-ttu-id="1c6f2-177">Récupérez deux classes enfants de la classe de système de [**\_ \_ paramètres**](--parameters.md) à l’aide de [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-177">Retrieve two child classes of the [**\_\_PARAMETERS**](--parameters.md) system class using either [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="1c6f2-178">Utilisez la première classe enfant pour décrire les paramètres in-et la seconde pour décrire les paramètres out.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-178">Use the first child class to describe the in-parameters, and the second to describe the out-parameters.</span></span> <span data-ttu-id="1c6f2-179">Si nécessaire, vous pouvez effectuer une récupération unique suivie d’un appel à la méthode [**IWbemClassObject :: Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) .</span><span class="sxs-lookup"><span data-stu-id="1c6f2-179">If necessary, you can perform a single retrieval followed by a call to the [**IWbemClassObject::Clone**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-clone) method.</span></span>

3.  <span data-ttu-id="1c6f2-180">Écrivez les paramètres in-dans la première classe, et les paramètres out dans la deuxième classe, à l’aide d’un ou plusieurs appels à [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-180">Write the in-parameters to the first class, and the out-parameters to the second class, using one or more calls to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="1c6f2-181">Lors de la description des paramètres d’une méthode, observez les règles et restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="1c6f2-181">When describing parameters to a method, observe the following rules and restrictions:</span></span>

    -   <span data-ttu-id="1c6f2-182">Traitez les \[ paramètres in, out \] en tant qu’entrées distinctes, l’un dans l’objet qui contient les paramètres in et l’autre dans l’objet qui contient les paramètres out.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-182">Treat the \[in, out\] parameters as separate entries, one in the object that contains the in-parameters and one in the object that contains the out-parameters.</span></span>
    -   <span data-ttu-id="1c6f2-183">\[En dehors des qualificateurs out, les qualificateurs \] restants doivent être exactement les mêmes.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-183">Other than the \[in, out\] qualifiers, the remaining qualifiers must be exactly the same.</span></span>
    -   <span data-ttu-id="1c6f2-184">Spécifiez les qualificateurs d' [**ID**](standard-wmi-qualifiers.md) , en commençant à 0 (zéro), un pour chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-184">Specify the [**ID**](standard-wmi-qualifiers.md) qualifiers, starting at 0 (zero), one for each parameter.</span></span>

        <span data-ttu-id="1c6f2-185">L’ordre des paramètres d’entrée ou de sortie est établi par la valeur du qualificateur d' [**ID**](standard-wmi-qualifiers.md) sur chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-185">The order of the input or output parameters is established by the value of the [**ID**](standard-wmi-qualifiers.md) qualifier on each parameter.</span></span> <span data-ttu-id="1c6f2-186">Tous les arguments d’entrée doivent précéder les arguments de sortie.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-186">All input arguments must precede any output arguments.</span></span> <span data-ttu-id="1c6f2-187">La modification de l’ordre des paramètres d’entrée et de sortie de la méthode lors de la mise à jour d’un fournisseur de méthode existant peut entraîner l’échec des applications qui appellent la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-187">Changing the order of method input and output parameters when updating an existing method provider can cause applications that call the method to fail.</span></span> <span data-ttu-id="1c6f2-188">Ajoutez de nouveaux paramètres d’entrée à la fin des paramètres existants au lieu de les insérer dans la séquence déjà établie.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-188">Add new input parameters at the end of the existing parameters rather than inserting them in the sequence that is already established.</span></span>

        <span data-ttu-id="1c6f2-189">Veillez à ne pas définir d’écart dans la séquence de qualificateur d' [**ID**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="1c6f2-189">Make sure to leave no gaps in the [**ID**](standard-wmi-qualifiers.md) qualifier sequence.</span></span>

    -   <span data-ttu-id="1c6f2-190">Placez la valeur de retour dans la classe out-Parameters en tant que propriété nommée **returnValue**.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-190">Place the return value in the out-parameters class as a property named **ReturnValue**.</span></span>

        <span data-ttu-id="1c6f2-191">Cela identifie la propriété en tant que valeur de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-191">This identifies the property as the return value of the method.</span></span> <span data-ttu-id="1c6f2-192">Le type CIM de cette propriété est le type de retour de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-192">The CIM type of this property is the return type of the method.</span></span> <span data-ttu-id="1c6f2-193">Si la méthode a un type de retour void, alors n’avez aucune propriété **returnValue** .</span><span class="sxs-lookup"><span data-stu-id="1c6f2-193">If the method has a return type of void, then do not have a **ReturnValue** property at all.</span></span> <span data-ttu-id="1c6f2-194">En outre, la propriété **returnValue** ne peut pas avoir un qualificateur d' [**ID**](standard-wmi-qualifiers.md) comme les arguments de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-194">Also, the **ReturnValue** property cannot have an [**ID**](standard-wmi-qualifiers.md) qualifier like the arguments of the method.</span></span> <span data-ttu-id="1c6f2-195">L’affectation d’un qualificateur d' **ID** à la propriété **returnValue** génère une erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-195">Assigning an **ID** qualifier to the **ReturnValue** property produces a WMI error.</span></span>

    -   <span data-ttu-id="1c6f2-196">Exprimez toutes les valeurs de paramètre par défaut pour la propriété dans la classe.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-196">Express any default parameter values for the property in the class.</span></span>

4.  <span data-ttu-id="1c6f2-197">Placez les deux objets de [**\_ \_ paramètres**](--parameters.md) dans la classe parente à l’aide d’un appel à [**IWbemClassObject ::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="1c6f2-197">Place both [**\_\_PARAMETERS**](--parameters.md) objects into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

    <span data-ttu-id="1c6f2-198">Un seul appel à [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) peut placer les deux objets de [**\_ \_ paramètres**](--parameters.md) dans la classe.</span><span class="sxs-lookup"><span data-stu-id="1c6f2-198">A single call to [**PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod) can place both [**\_\_PARAMETERS**](--parameters.md) objects into the class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c6f2-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1c6f2-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c6f2-200">Création d’une classe</span><span class="sxs-lookup"><span data-stu-id="1c6f2-200">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 
