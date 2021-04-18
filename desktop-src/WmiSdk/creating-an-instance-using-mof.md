---
description: Vous pouvez déclarer une instance de base d’une classe dans le service de gestion Windows à l’aide d’format MOF (MOF). Vous pouvez également remplacer les valeurs par défaut d’une instance. Pour plus d’informations, consultez Définition d’une valeur de propriété d’instance.
ms.assetid: 12eda062-9614-455d-ae99-7706c685137b
ms.tgt_platform: multiple
title: Création d’une instance à l’aide de MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5078c5fcddaab4e8437a33e8cb3210d515360fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522686"
---
# <a name="creating-an-instance-using-mof"></a><span data-ttu-id="23b41-105">Création d’une instance à l’aide de MOF</span><span class="sxs-lookup"><span data-stu-id="23b41-105">Creating an Instance Using MOF</span></span>

<span data-ttu-id="23b41-106">Vous pouvez déclarer une instance de base d’une classe dans le service de gestion Windows à l’aide d’format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="23b41-106">You can declare a basic instance of a class in the Windows Management service using Managed Object Format (MOF).</span></span> <span data-ttu-id="23b41-107">Vous pouvez également remplacer les valeurs par défaut d’une instance.</span><span class="sxs-lookup"><span data-stu-id="23b41-107">You can also override the default values for an instance.</span></span> <span data-ttu-id="23b41-108">Pour plus d’informations, consultez [définition d’une valeur de propriété d’instance](#setting-an-instance-property-value).</span><span class="sxs-lookup"><span data-stu-id="23b41-108">For more information, see [Setting an Instance Property Value](#setting-an-instance-property-value).</span></span>

<span data-ttu-id="23b41-109">La procédure suivante décrit comment déclarer une instance de base d’une classe à l’aide de code MOF.</span><span class="sxs-lookup"><span data-stu-id="23b41-109">The following procedure describes how to declare a basic instance of a class using MOF code.</span></span>

<span data-ttu-id="23b41-110">**Pour déclarer une instance de base d’une classe à l’aide du code MOF**</span><span class="sxs-lookup"><span data-stu-id="23b41-110">**To declare a basic instance of a class using MOF code**</span></span>

1.  <span data-ttu-id="23b41-111">Utilisez l' **instance de** Mots clés suivie du nom de la classe, des accolades et d’un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="23b41-111">Use the **Instance of** keywords followed by the class name, curly braces, and a semicolon.</span></span>

    <span data-ttu-id="23b41-112">L’exemple de code suivant montre comment déclarer une instance d’une classe.</span><span class="sxs-lookup"><span data-stu-id="23b41-112">The following code example shows how to declare an instance of a class.</span></span>

    ```mof
    instance of ClassName
    {
    };
    ```

    

2.  <span data-ttu-id="23b41-113">Lorsque vous avez terminé, insérez votre code MOF dans le référentiel WMI à l’aide du compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="23b41-113">When finished, insert your MOF code into the WMI repository using the MOF compiler.</span></span>

    <span data-ttu-id="23b41-114">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="23b41-114">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="23b41-115">Une instance d’une classe comprend toutes les propriétés de la classe.</span><span class="sxs-lookup"><span data-stu-id="23b41-115">An instance of a class includes all of the properties of the class.</span></span> <span data-ttu-id="23b41-116">Si la classe est une classe dérivée, les instances incluent les propriétés qui appartiennent à toutes les classes figurant plus haut dans la hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="23b41-116">If the class is a derived class, instances include the properties belonging to all of the classes higher in the hierarchy.</span></span> <span data-ttu-id="23b41-117">Chaque classe à partir de laquelle une instance est créée a une ou plusieurs propriétés de clé.</span><span class="sxs-lookup"><span data-stu-id="23b41-117">Each class that an instance is created from has one or more key properties.</span></span> <span data-ttu-id="23b41-118">Vous ne pouvez pas créer une instance avec plus de 256 clés.</span><span class="sxs-lookup"><span data-stu-id="23b41-118">You cannot create an instance with more than 256 keys.</span></span>

## <a name="setting-an-instance-property-value"></a><span data-ttu-id="23b41-119">Définition d’une valeur de propriété d’instance</span><span class="sxs-lookup"><span data-stu-id="23b41-119">Setting an Instance Property Value</span></span>

<span data-ttu-id="23b41-120">Étant donné que les propriétés de type WMI sont fortement typées, vous ne pouvez pas modifier les types de propriété.</span><span class="sxs-lookup"><span data-stu-id="23b41-120">Because WMI strongly types properties, you cannot modify property types.</span></span> <span data-ttu-id="23b41-121">Toutefois, vous pouvez définir des valeurs de propriété dans les instances.</span><span class="sxs-lookup"><span data-stu-id="23b41-121">You can, however, set property values in instances.</span></span> <span data-ttu-id="23b41-122">Quand une classe assigne une valeur par défaut à une propriété, WMI affecte la valeur par défaut à chaque instance.</span><span class="sxs-lookup"><span data-stu-id="23b41-122">When a class assigns a default value to a property, WMI assigns the default value to each instance.</span></span> <span data-ttu-id="23b41-123">Vous pouvez remplacer cette valeur dans votre déclaration d’instance.</span><span class="sxs-lookup"><span data-stu-id="23b41-123">You can override this value in your instance declaration.</span></span>

<span data-ttu-id="23b41-124">La procédure suivante décrit comment définir une valeur de propriété ou remplacer une valeur par défaut à l’aide du code MOF.</span><span class="sxs-lookup"><span data-stu-id="23b41-124">The following procedure describes how to set a property value or overwrite a default value using MOF code.</span></span>

<span data-ttu-id="23b41-125">**Pour définir une valeur de propriété ou remplacer une valeur par défaut à l’aide du code MOF**</span><span class="sxs-lookup"><span data-stu-id="23b41-125">**To set a property value or overwrite a default value using MOF code**</span></span>

1.  <span data-ttu-id="23b41-126">Placez une instruction d’assignation entre les accolades de la déclaration d’instance.</span><span class="sxs-lookup"><span data-stu-id="23b41-126">Place an assignment statement between the curly braces of the instance declaration.</span></span>

    <span data-ttu-id="23b41-127">L’exemple de code suivant montre comment définir une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="23b41-127">The following code example shows how to set a property value.</span></span>

    ``` syntax
    instance of ClassName
    {
        Prop = "value";
    };
    ```

    <span data-ttu-id="23b41-128">WMI ne nécessite pas de définir de propriété lors de la création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="23b41-128">WMI does not require that you set any property during instance creation.</span></span> <span data-ttu-id="23b41-129">L’exception est toute propriété marquée avec le qualificateur de [**clé**](key-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="23b41-129">The exception is any property marked with the [**Key**](key-qualifier.md) qualifier.</span></span> <span data-ttu-id="23b41-130">Étant donné que WMI utilise des propriétés de clé pour identifier de façon unique les instances, vous devez définir toutes les propriétés de clé à mesure que vous les rencontrez.</span><span class="sxs-lookup"><span data-stu-id="23b41-130">Because WMI uses key properties to uniquely identify instances, you must set all key properties as you encounter them.</span></span> <span data-ttu-id="23b41-131">En revanche, vous ne devez pas définir une propriété système dans une déclaration d’instance.</span><span class="sxs-lookup"><span data-stu-id="23b41-131">In contrast, you must not set a system property in an instance declaration.</span></span> <span data-ttu-id="23b41-132">Au lieu de cela, WMI affecte les valeurs appropriées à une propriété système si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="23b41-132">Instead, WMI assigns the appropriate values to a system property when necessary.</span></span>

2.  <span data-ttu-id="23b41-133">Lorsque vous avez terminé, insérez votre code MOF dans le référentiel WMI à l’aide d’un appel au compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="23b41-133">When finished, insert your MOF code into the WMI repository with a call to the MOF compiler.</span></span>

    <span data-ttu-id="23b41-134">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="23b41-134">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="23b41-135">Les exemples de code suivants montrent comment une instance spécifie des données pour les propriétés définies par une classe.</span><span class="sxs-lookup"><span data-stu-id="23b41-135">The following code examples show how an instance specifies data for properties defined by a class.</span></span>

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

<span data-ttu-id="23b41-136">Dans l’exemple précédent, la classe définit trois propriétés : une chaîne de caractères, un entier signé 32 bits et un entier 32 bits non signé.</span><span class="sxs-lookup"><span data-stu-id="23b41-136">In the preceding example, the class defines three properties: a character string, a 32-bit signed integer, and a 32-bit unsigned integer.</span></span> <span data-ttu-id="23b41-137">L’instance de fournit des valeurs de données pour chacune de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="23b41-137">The instance provides data values for each of these properties.</span></span>

 

 



