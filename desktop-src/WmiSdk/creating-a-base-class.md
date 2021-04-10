---
description: La méthode recommandée pour créer une nouvelle classe de base WMI pour un fournisseur WMI est dans un fichier format MOF (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Création d’une classe de base WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebdcbe6995a7782d854a4d0950db841f23a30b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952865"
---
# <a name="creating-a-wmi-base-class"></a><span data-ttu-id="58f90-103">Création d’une classe de base WMI</span><span class="sxs-lookup"><span data-stu-id="58f90-103">Creating a WMI Base Class</span></span>

<span data-ttu-id="58f90-104">La méthode recommandée pour créer une nouvelle classe de base WMI pour un fournisseur WMI est dans un fichier format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="58f90-104">The recommended way to create a new WMI base class for a WMI provider is in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="58f90-105">Vous pouvez également créer une classe de base à l’aide [de l’API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-105">You can also create a base class using the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="58f90-106">Bien que vous puissiez créer une classe de base ou une classe dérivée dans un script, sans qu’un fournisseur fournisse des données à la classe et à ses sous-classes, la classe n’est pas utile.</span><span class="sxs-lookup"><span data-stu-id="58f90-106">While you can create a base or derived class in script, without a provider supplying data to the class and its subclasses, the class is not useful.</span></span>

<span data-ttu-id="58f90-107">Les sections suivantes sont présentées dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="58f90-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="58f90-108">Création d’une classe de base à l’aide de MOF</span><span class="sxs-lookup"><span data-stu-id="58f90-108">Creating a Base Class Using MOF</span></span>](#creating-a-base-class-using-mof)
-   [<span data-ttu-id="58f90-109">Création d’une classe de base avec C++</span><span class="sxs-lookup"><span data-stu-id="58f90-109">Creating a Base Class with C++</span></span>](#creating-a-base-class-with-c)
-   [<span data-ttu-id="58f90-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58f90-110">Related topics</span></span>](#related-topics)

## <a name="creating-a-base-class-using-mof"></a><span data-ttu-id="58f90-111">Création d’une classe de base à l’aide de MOF</span><span class="sxs-lookup"><span data-stu-id="58f90-111">Creating a Base Class Using MOF</span></span>

<span data-ttu-id="58f90-112">Les classes WMI s’appuient généralement sur l’héritage.</span><span class="sxs-lookup"><span data-stu-id="58f90-112">WMI classes usually rely on inheritance.</span></span> <span data-ttu-id="58f90-113">Avant de créer une classe de base, vérifiez les classes Common Information Model (CIM) disponibles dans Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span><span class="sxs-lookup"><span data-stu-id="58f90-113">Before creating a base class, check the Common Information Model (CIM) classes available from the Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).</span></span>

<span data-ttu-id="58f90-114">Si de nombreuses classes dérivées utilisent les mêmes propriétés, placez ces propriétés et ces méthodes dans votre classe de base.</span><span class="sxs-lookup"><span data-stu-id="58f90-114">If many derived classes will use the same properties, put these properties and methods in your base class.</span></span> <span data-ttu-id="58f90-115">Le nombre maximal de propriétés que vous pouvez définir dans une classe WMI est 1024.</span><span class="sxs-lookup"><span data-stu-id="58f90-115">The maximum number of properties you can define in a WMI class is 1024.</span></span>

<span data-ttu-id="58f90-116">Lorsque vous créez une classe de base, observez la liste suivante d’instructions pour les noms de classe :</span><span class="sxs-lookup"><span data-stu-id="58f90-116">When creating a base class, observe the following list of guidelines for class names:</span></span>

-   <span data-ttu-id="58f90-117">Utilisez les majuscules et les minuscules.</span><span class="sxs-lookup"><span data-stu-id="58f90-117">Use both uppercase and lowercase letters.</span></span>
-   <span data-ttu-id="58f90-118">Commencez un nom de classe par une lettre.</span><span class="sxs-lookup"><span data-stu-id="58f90-118">Begin a class name with a letter.</span></span>
-   <span data-ttu-id="58f90-119">N’utilisez pas de trait de soulignement de début ou de fin.</span><span class="sxs-lookup"><span data-stu-id="58f90-119">Do not use either a leading or trailing underscore.</span></span>
-   <span data-ttu-id="58f90-120">Définissez tous les caractères restants comme des lettres, des chiffres ou des traits de soulignement.</span><span class="sxs-lookup"><span data-stu-id="58f90-120">Define all remaining characters as letters, digits, or underscores.</span></span>
-   <span data-ttu-id="58f90-121">Utilisez une convention d’affectation de noms cohérente.</span><span class="sxs-lookup"><span data-stu-id="58f90-121">Use a consistent naming convention.</span></span>

    <span data-ttu-id="58f90-122">Bien qu’il ne soit pas nécessaire, une bonne Convention d’affectation de noms pour une classe est de deux composants joints par un trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="58f90-122">While not necessary, a good naming convention for a class is two components joined by an underscore.</span></span> <span data-ttu-id="58f90-123">Lorsque cela est possible, un nom de fournisseur doit constituer la première moitié du nom et un nom de classe descriptif doit être la deuxième partie.</span><span class="sxs-lookup"><span data-stu-id="58f90-123">When possible, a vendor name should make up the first half of the name, and a descriptive class name should be the second part.</span></span>

> [!Note]  
> <span data-ttu-id="58f90-124">Les classes ne peuvent pas être modifiées pendant l’exécution des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="58f90-124">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="58f90-125">Vous devez arrêter l’activité, modifier la classe, puis redémarrer le service de gestion Windows.</span><span class="sxs-lookup"><span data-stu-id="58f90-125">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="58f90-126">La détection d’une modification de classe n’est pas possible actuellement.</span><span class="sxs-lookup"><span data-stu-id="58f90-126">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="58f90-127">Dans MOF, créez une classe de base en la nommant avec le mot clé **Class** , mais sans indiquer une classe parente.</span><span class="sxs-lookup"><span data-stu-id="58f90-127">In MOF, create a base class by naming it with the **class** keyword, but not indicating a parent class.</span></span>

<span data-ttu-id="58f90-128">**Pour créer une classe de base à l’aide du code MOF**</span><span class="sxs-lookup"><span data-stu-id="58f90-128">**To create a base class using MOF code**</span></span>

1.  <span data-ttu-id="58f90-129">Utilisez le mot clé **Class** avec le nom de la nouvelle classe, suivi d’une paire d’accolades et d’un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="58f90-129">Use the **class** keyword with the name of the new class, followed by a pair of curly braces and a semicolon.</span></span> <span data-ttu-id="58f90-130">Ajoutez des propriétés et des méthodes pour la classe entre les accolades.</span><span class="sxs-lookup"><span data-stu-id="58f90-130">Add properties and methods for the class between the curly braces.</span></span> <span data-ttu-id="58f90-131">L’exemple de code suivant est fourni.</span><span class="sxs-lookup"><span data-stu-id="58f90-131">The following code example is provided.</span></span>

    <span data-ttu-id="58f90-132">L’exemple de code suivant montre comment définir une classe de base.</span><span class="sxs-lookup"><span data-stu-id="58f90-132">The following code example shows how a base class should be defined.</span></span>

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    <span data-ttu-id="58f90-133">L’exemple de code suivant montre une définition incorrecte d’une classe de base.</span><span class="sxs-lookup"><span data-stu-id="58f90-133">The following code example shows an incorrect definition of a base class.</span></span>

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  <span data-ttu-id="58f90-134">Ajoutez des [*qualificateurs*](gloss-q.md) de classe avant le mot clé class pour modifier la façon dont la classe est utilisée.</span><span class="sxs-lookup"><span data-stu-id="58f90-134">Add any class [*qualifiers*](gloss-q.md) before the class keyword to modify the way the class is used.</span></span> <span data-ttu-id="58f90-135">Placez les qualificateurs entre crochets.</span><span class="sxs-lookup"><span data-stu-id="58f90-135">Place the qualifiers between square brackets.</span></span> <span data-ttu-id="58f90-136">Pour plus d’informations sur les qualificateurs permettant de modifier des classes, consultez [qualificateurs WMI](wmi-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-136">For more information about qualifiers for modifying classes, see [WMI Qualifiers](wmi-qualifiers.md).</span></span> <span data-ttu-id="58f90-137">Utilisez le qualificateur **abstract** pour indiquer que vous ne pouvez pas créer une instance de cette classe directement.</span><span class="sxs-lookup"><span data-stu-id="58f90-137">Use the **Abstract** qualifier to indicate that you cannot create an instance of this class directly.</span></span> <span data-ttu-id="58f90-138">Les classes abstraites sont souvent utilisées pour définir des propriétés ou des méthodes qui seront utilisées par plusieurs classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="58f90-138">Abstract classes are often used to define properties or methods that will be used by several derived classes.</span></span> <span data-ttu-id="58f90-139">Pour plus d’informations, consultez [création d’une classe dérivée](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-139">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

    <span data-ttu-id="58f90-140">L’exemple de code suivant définit la classe comme abstraite et définit le fournisseur qui fournira les données.</span><span class="sxs-lookup"><span data-stu-id="58f90-140">The following code example defines the class as abstract and defines the provider that will supply the data.</span></span> <span data-ttu-id="58f90-141">La [*version*](gloss-f.md) du qualificateur **ToSubClass** indique que les informations contenues dans le qualificateur du **fournisseur** sont héritées par les classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="58f90-141">The **ToSubClass** qualifier [*flavor*](gloss-f.md) indicates that the information in the **Provider** qualifier is inherited by derived classes.</span></span>

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  <span data-ttu-id="58f90-142">Ajoutez les propriétés et les méthodes de la classe à l’intérieur des crochets avant le nom de la propriété ou de la méthode.</span><span class="sxs-lookup"><span data-stu-id="58f90-142">Add the properties and methods for the class inside square brackets before the property or method name.</span></span> <span data-ttu-id="58f90-143">Pour plus d’informations, consultez [Ajout d’une propriété](adding-a-property.md) et [création d’une méthode](creating-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-143">For more information, see [Adding a Property](adding-a-property.md) and [Creating a Method](creating-a-method.md).</span></span> <span data-ttu-id="58f90-144">Vous pouvez modifier ces propriétés et méthodes à l’aide de qualificateurs MOF.</span><span class="sxs-lookup"><span data-stu-id="58f90-144">You can modify these properties and methods using MOF qualifiers.</span></span> <span data-ttu-id="58f90-145">Pour plus d’informations, consultez [Ajout d’un qualificateur](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-145">For more information, see [Adding a Qualifier](adding-a-qualifier.md).</span></span>

    <span data-ttu-id="58f90-146">L’exemple de code suivant montre comment modifier les propriétés et les méthodes avec des qualificateurs MOF.</span><span class="sxs-lookup"><span data-stu-id="58f90-146">The following code example shows how to modify properties and methods with MOF qualifiers.</span></span>

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  <span data-ttu-id="58f90-147">Enregistrez le fichier MOF avec l’extension. mof.</span><span class="sxs-lookup"><span data-stu-id="58f90-147">Save the MOF file with an extension of .mof.</span></span>
5.  <span data-ttu-id="58f90-148">Inscrivez la classe avec WMI en exécutant [**Mofcomp.exe**](mofcomp.md) sur le fichier.</span><span class="sxs-lookup"><span data-stu-id="58f90-148">Register the class with WMI by running [**Mofcomp.exe**](mofcomp.md) on the file.</span></span>

    <span data-ttu-id="58f90-149">**mofcomp.exe** *newmof. mof*</span><span class="sxs-lookup"><span data-stu-id="58f90-149">**mofcomp.exe** *newmof.mof*</span></span>

    <span data-ttu-id="58f90-150">Si vous n’utilisez pas le commutateur **-N** ou l' \# [**espace de noms du pragma**](pragma-namespace.md) de commande du préprocesseur pour spécifier un espace de noms, les classes MOF compilées sont stockées dans l' \\ espace de noms racine par défaut dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="58f90-150">If you do not use the **-N** switch or the preprocessor command \#[**pragma namespace**](pragma-namespace.md) to specify a namespace, the compiled MOF classes will be stored in the root\\default namespace in the repository.</span></span> <span data-ttu-id="58f90-151">Pour plus d’informations, consultez [**mofcomp**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-151">For more information, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="58f90-152">L’exemple de code suivant combine les exemples de code MOF décrits dans la procédure précédente et montre comment créer une classe de base dans l' \\ espace de noms CIMV2 racine à l’aide de MOF.</span><span class="sxs-lookup"><span data-stu-id="58f90-152">The following code example combines the MOF code examples discussed in the previous procedure and shows how to create a base class in the root\\cimv2 namespace using MOF.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root\\cimv2")

[Abstract, Provider("MyProvider") : ToSubClass]
class MyClass_BaseDisk
{
  [read : ToSubClass, key : ToSubClass ] string DeviceID;
  [read : ToSubClass] uint32 State;
  [read : ToSubClass, write : ToSubClass] uint64 LimitUsers;
};
```

<span data-ttu-id="58f90-153">Pour plus d’informations, consultez [création d’une classe dérivée](creating-a-derived-class.md) pour obtenir un exemple de classe dynamique dérivée de cette classe de base.</span><span class="sxs-lookup"><span data-stu-id="58f90-153">For more information, see [Creating a Derived Class](creating-a-derived-class.md) for an example of a dynamic class derived from this base class.</span></span>

## <a name="creating-a-base-class-with-c"></a><span data-ttu-id="58f90-154">Création d’une classe de base avec C++</span><span class="sxs-lookup"><span data-stu-id="58f90-154">Creating a Base Class with C++</span></span>

<span data-ttu-id="58f90-155">La création d’une classe de base à l’aide de l’API WMI est principalement une série de commandes put qui définissent la classe et inscrivent la classe auprès de WMI.</span><span class="sxs-lookup"><span data-stu-id="58f90-155">Creating a base class using the WMI API is mainly a series of Put commands that define the class and register the class with WMI.</span></span> <span data-ttu-id="58f90-156">L’objectif principal de cette API est de permettre aux applications clientes de créer des classes de base.</span><span class="sxs-lookup"><span data-stu-id="58f90-156">The main purpose of this API is to enable client applications to create base classes.</span></span> <span data-ttu-id="58f90-157">Toutefois, vous pouvez également faire en sorte qu’un fournisseur utilise cette API pour créer une classe de base.</span><span class="sxs-lookup"><span data-stu-id="58f90-157">However, you can also have a provider use this API to create a base class.</span></span> <span data-ttu-id="58f90-158">Par exemple, si vous pensez que le code MOF de votre fournisseur ne sera pas installé correctement, vous pouvez demander à votre fournisseur de créer automatiquement les classes appropriées dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="58f90-158">For example, if you believe that the MOF code for your provider will not be installed properly, you can instruct your provider to automatically create the correct classes in the WMI repository.</span></span> <span data-ttu-id="58f90-159">Pour plus d’informations sur les fournisseurs, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-159">For more information about providers, see [Writing a Class Provider](writing-a-class-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="58f90-160">Les classes ne peuvent pas être modifiées pendant l’exécution des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="58f90-160">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="58f90-161">Vous devez arrêter l’activité, modifier la classe, puis redémarrer le service de gestion Windows.</span><span class="sxs-lookup"><span data-stu-id="58f90-161">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="58f90-162">La détection d’une modification de classe n’est pas possible actuellement.</span><span class="sxs-lookup"><span data-stu-id="58f90-162">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="58f90-163">Le code requiert la compilation correcte de la référence suivante.</span><span class="sxs-lookup"><span data-stu-id="58f90-163">The code requires the following reference to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="58f90-164">Vous pouvez créer une classe de base par programmation à l’aide [de l’API com pour WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="58f90-164">You can create a new base class programmatically using the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="58f90-165">**Pour créer une nouvelle classe de base avec l’API WMI**</span><span class="sxs-lookup"><span data-stu-id="58f90-165">**To create a new base class with the WMI API**</span></span>

1.  <span data-ttu-id="58f90-166">Récupérez une définition de la nouvelle classe en appelant la méthode [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) avec le paramètre *strObjectPath* défini sur une valeur **null** .</span><span class="sxs-lookup"><span data-stu-id="58f90-166">Retrieve a definition for the new class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method with the *strObjectPath* parameter set to a **null** value.</span></span>

    <span data-ttu-id="58f90-167">L’exemple de code suivant montre comment récupérer une définition pour une nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="58f90-167">The following code example shows how to retrieve a definition for a new class.</span></span>

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  <span data-ttu-id="58f90-168">Établissez un nom pour la classe en définissant la propriété système de **\_ \_ classe** avec un appel à la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="58f90-168">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="58f90-169">L’exemple de code suivant montre comment nommer la classe en définissant la propriété système de la **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="58f90-169">The following code example shows how to name the class by setting the **\_\_CLASS** system property.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);
    V_VT(&v) = VT_BSTR;

    V_BSTR(&v) = SysAllocString(L"Example");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

3.  <span data-ttu-id="58f90-170">Créez la ou les propriétés de clé en appelant [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="58f90-170">Create the key property or properties by calling [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="58f90-171">L’exemple de code suivant décrit comment créer la propriété d' [**index**](swbemrefreshableitem-index.md) , qui est étiquetée comme une propriété de clé à l’étape 4.</span><span class="sxs-lookup"><span data-stu-id="58f90-171">The following code example describes how to create the [**Index**](swbemrefreshableitem-index.md) property, which is labeled as a key property in Step 4.</span></span>

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  <span data-ttu-id="58f90-172">Attachez le qualificateur standard [**Key**](standard-qualifiers.md) à la propriété de clé en appelant d’abord la méthode [**IWbemClassObject :: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) , puis la méthode [**IWbemQualifierSet ::P ut**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .</span><span class="sxs-lookup"><span data-stu-id="58f90-172">Attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property by first calling the [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) method and then the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="58f90-173">L’exemple de code suivant montre comment attacher le qualificateur standard [**Key**](standard-qualifiers.md) à la propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="58f90-173">The following code example shows how to attach the [**Key**](standard-qualifiers.md) standard qualifier to the key property.</span></span>

    ```C++
      IWbemQualifierSet *pQual = 0;
      pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
      SysFreeString(KeyProp);

      V_VT(&v) = VT_BOOL;
      V_BOOL(&v) = VARIANT_TRUE;
      BSTR Key = SysAllocString(L"Key");

      pQual->Put(Key, &v, 0);   // Flavors not required for Key 
      SysFreeString(Key);

      // No longer need the qualifier set for "Index"
      pQual->Release();   
      VariantClear(&v);
    ```

    

5.  <span data-ttu-id="58f90-174">Créez d’autres propriétés de la classe avec [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="58f90-174">Create other properties of the class with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="58f90-175">L’exemple de code suivant décrit comment créer des propriétés supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="58f90-175">The following code example describes how to create additional properties.</span></span>

    ```C++
      V_VT(&v) = VT_BSTR;
      V_BSTR(&v) = SysAllocString(L"<default>");
      BSTR OtherProp = SysAllocString(L"OtherInfo");
      pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
      SysFreeString(OtherProp);
      VariantClear(&v);

      OtherProp = SysAllocString(L"IntVal");
      pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
      SysFreeString(OtherProp);
    ```

    

6.  <span data-ttu-id="58f90-176">Inscrivez la nouvelle classe en appelant [**IWbemServices ::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="58f90-176">Register the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="58f90-177">Étant donné que vous ne pouvez pas définir de clés et d’index après avoir inscrit une nouvelle classe, assurez-vous que vous avez défini toutes vos propriétés avant d’appeler [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="58f90-177">Because you cannot define keys and indices after you register a new class, ensure that you have defined all of your properties before calling [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="58f90-178">L’exemple de code suivant décrit comment inscrire une nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="58f90-178">The following code example describes how to register a new class.</span></span>

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

<span data-ttu-id="58f90-179">L’exemple de code suivant combine les exemples de code présentés dans la procédure précédente et montre comment créer une classe de base à l’aide de l’API WMI.</span><span class="sxs-lookup"><span data-stu-id="58f90-179">The following code example combines the code examples discussed in the previous procedure and shows how to create a base class using the WMI API.</span></span>


```C++
void CreateClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  // Get a class definition. 
  // ============================
  HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create the key property. 
  // ============================
  BSTR KeyProp = SysAllocString(L"Index");
  pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);

  // Attach Key qualifier to mark the "Index" property as the key.
  // ============================
  IWbemQualifierSet *pQual = 0;
  pNewClass->GetPropertyQualifierSet(KeyProp, &pQual);
  SysFreeString(KeyProp);

  V_VT(&v) = VT_BOOL;
  V_BOOL(&v) = VARIANT_TRUE;
  BSTR Key = SysAllocString(L"Key");

  pQual->Put(Key, &v, 0);   // Flavors not required for Key 
  SysFreeString(Key);

  // No longer need the qualifier set for "Index"
  pQual->Release();     
  VariantClear(&v);

  // Create other properties.
  // ============================
  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"<default>");
  BSTR OtherProp = SysAllocString(L"OtherInfo");
  pNewClass->Put(OtherProp, 0, &v, CIM_STRING);
  SysFreeString(OtherProp);
  VariantClear(&v);

  OtherProp = SysAllocString(L"IntVal");
  pNewClass->Put(OtherProp, 0, NULL, CIM_SINT32); // NULL is default
  SysFreeString(OtherProp);
  
  // Register the class with WMI
  // ============================
  hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
  pNewClass->Release();
}
```



## <a name="related-topics"></a><span data-ttu-id="58f90-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58f90-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58f90-181">Création d’une classe</span><span class="sxs-lookup"><span data-stu-id="58f90-181">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



