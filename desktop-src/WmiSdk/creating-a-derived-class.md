---
description: La création d’une classe dérivée dans WMI est très similaire à la création d’une classe de base. Comme avec une classe de base, vous devez d’abord définir la classe dérivée, puis inscrire la classe dérivée avec WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Création d’une classe dérivée WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517634"
---
# <a name="creating-a-wmi-derived-class"></a><span data-ttu-id="e0721-104">Création d’une classe dérivée WMI</span><span class="sxs-lookup"><span data-stu-id="e0721-104">Creating a WMI Derived Class</span></span>

<span data-ttu-id="e0721-105">La création d’une classe dérivée dans WMI est très similaire à la création d’une classe de base.</span><span class="sxs-lookup"><span data-stu-id="e0721-105">Creating a derived class in WMI is very similar to creating a base class.</span></span> <span data-ttu-id="e0721-106">Comme avec une classe de base, vous devez d’abord définir la classe dérivée, puis inscrire la classe dérivée avec WMI.</span><span class="sxs-lookup"><span data-stu-id="e0721-106">As with a base class, you must first define the derived class and then register the derived class with WMI.</span></span> <span data-ttu-id="e0721-107">La principale différence réside dans le fait que vous devez d’abord rechercher la classe parente à partir de laquelle vous souhaitez dériver.</span><span class="sxs-lookup"><span data-stu-id="e0721-107">The main difference is that you must first locate the parent class from which you wish to derive.</span></span> <span data-ttu-id="e0721-108">Pour plus d’informations, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md) et [écriture d’un fournisseur d’instances](writing-an-instance-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e0721-108">For more information, see [Writing a Class Provider](writing-a-class-provider.md) and [Writing an Instance Provider](writing-an-instance-provider.md).</span></span>

<span data-ttu-id="e0721-109">La méthode recommandée pour créer des classes pour un fournisseur se trouve dans des fichiers format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e0721-109">The recommended way to create classes for a provider is in Managed Object Format (MOF) files.</span></span> <span data-ttu-id="e0721-110">Plusieurs classes dérivées qui sont liées entre elles doivent être regroupées dans un fichier MOF, ainsi que toutes les classes de base à partir desquelles elles dérivent des propriétés ou des méthodes.</span><span class="sxs-lookup"><span data-stu-id="e0721-110">Several derived classes that are related to each other should be grouped into a MOF file, along with any base classes from which they derive properties or methods.</span></span> <span data-ttu-id="e0721-111">Si vous placez chaque classe dans un fichier MOF distinct, chaque fichier doit être compilé pour que le fournisseur puisse fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="e0721-111">If you place each class in a separate MOF file then each file must be compiled before the provider can work properly.</span></span>

<span data-ttu-id="e0721-112">Après avoir créé votre classe, vous devez supprimer toutes les instances de votre classe avant de pouvoir effectuer l’une des activités suivantes sur votre classe dérivée :</span><span class="sxs-lookup"><span data-stu-id="e0721-112">After you create your class, you must delete all instances of your class before you can perform any of the following activities on your derived class:</span></span>

-   <span data-ttu-id="e0721-113">Modifiez la classe parente de votre classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-113">Change the parent class of your derived class.</span></span>
-   <span data-ttu-id="e0721-114">Ajoutez ou supprimez des propriétés.</span><span class="sxs-lookup"><span data-stu-id="e0721-114">Add or remove properties.</span></span>
-   <span data-ttu-id="e0721-115">Modifiez les types de propriété.</span><span class="sxs-lookup"><span data-stu-id="e0721-115">Change property types.</span></span>
-   <span data-ttu-id="e0721-116">Ajoutez ou supprimez des qualificateurs de [**clé**](key-qualifier.md) ou **indexés** .</span><span class="sxs-lookup"><span data-stu-id="e0721-116">Add or remove [**Key**](key-qualifier.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="e0721-117">Ajoutez ou supprimez des qualificateurs [**Singleton**](standard-wmi-qualifiers.md), **Dynamic** ou [**abstract**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="e0721-117">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

> [!Note]  
> <span data-ttu-id="e0721-118">Pour ajouter, supprimer ou modifier une propriété ou un qualificateur, appelez [**IWbemServices ::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) ou [**SWbemObject. put \_**](swbemobject-put-.md) et définissez le paramètre flag sur « Force mode ».</span><span class="sxs-lookup"><span data-stu-id="e0721-118">To add, remove, or modify a property or qualifier, call [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) or [**SWbemObject.Put\_**](swbemobject-put-.md) and set the flag parameter to "force mode".</span></span> <span data-ttu-id="e0721-119">Le qualificateur [**abstract**](standard-qualifiers.md) peut être utilisé uniquement si la classe parente est abstraite.</span><span class="sxs-lookup"><span data-stu-id="e0721-119">The [**Abstract**](standard-qualifiers.md) qualifier can be used only if the parent class is abstract.</span></span>

 

<span data-ttu-id="e0721-120">Quand vous déclarez votre classe dérivée, observez les règles et restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="e0721-120">When you declare your derived class, observe the following rules and restrictions:</span></span>

-   <span data-ttu-id="e0721-121">La classe parente de la classe dérivée doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="e0721-121">The parent class of the derived class must already exist.</span></span>

    <span data-ttu-id="e0721-122">La déclaration de la classe parente peut apparaître dans le même fichier MOF que la classe dérivée ou dans un autre fichier.</span><span class="sxs-lookup"><span data-stu-id="e0721-122">The declaration of the parent class can appear in the same MOF file as the derived class or in a different file.</span></span> <span data-ttu-id="e0721-123">Si la classe parente est inconnue, le compilateur génère une erreur au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e0721-123">If the parent class is unknown, the compiler generates a run-time error.</span></span>

-   <span data-ttu-id="e0721-124">Une classe dérivée ne peut avoir qu’une seule classe parente.</span><span class="sxs-lookup"><span data-stu-id="e0721-124">A derived class can have only a single parent class.</span></span>

    <span data-ttu-id="e0721-125">WMI ne prend pas en charge l’héritage multiple.</span><span class="sxs-lookup"><span data-stu-id="e0721-125">WMI does not support multiple inheritance.</span></span> <span data-ttu-id="e0721-126">Toutefois, une classe parente peut avoir de nombreuses classes dérivées.</span><span class="sxs-lookup"><span data-stu-id="e0721-126">However, a parent class can have many derived classes.</span></span>

-   <span data-ttu-id="e0721-127">Vous pouvez définir des index pour les classes dérivées, mais WMI n’utilise pas ces index.</span><span class="sxs-lookup"><span data-stu-id="e0721-127">You can define indices for derived classes, but WMI does not use these indices.</span></span>

    <span data-ttu-id="e0721-128">Par conséquent, la spécification d’un index sur une classe dérivée n’améliore pas les performances des requêtes pour les instances de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-128">Therefore, specifying an index on a derived class does not improve the performance of queries for instances of the derived class.</span></span> <span data-ttu-id="e0721-129">Vous pouvez améliorer les performances d’une requête sur une classe dérivée en spécifiant des propriétés indexées pour la classe parente de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-129">You can improve the performance of a query on a derived class by specifying indexed properties for the parent class of the derived class.</span></span>

-   <span data-ttu-id="e0721-130">Les définitions de classe dérivée peuvent être plus complexes et peuvent inclure des fonctionnalités telles que des alias, des qualificateurs et des versions de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="e0721-130">Derived class definitions can be more complex, and can include such features as aliases, qualifiers, and qualifier flavors.</span></span>

    <span data-ttu-id="e0721-131">Pour plus d’informations, consultez [création d’un alias](creating-an-alias.md) et [Ajout d’un qualificateur](adding-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="e0721-131">For more information, see [Creating an Alias](creating-an-alias.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

-   <span data-ttu-id="e0721-132">Si vous souhaitez modifier un qualificateur, modifier la valeur par défaut d’une propriété de la classe de base, ou encore fortement taper une référence ou une propriété d’objet incorporée d’une classe de base, vous devez déclarer à nouveau la totalité de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="e0721-132">If you wish to change a qualifier, change the default value of a base class property, or more strongly type a reference or embedded object property of a base class, you must declare the entire base class again.</span></span>
-   <span data-ttu-id="e0721-133">Le nombre maximal de propriétés que vous pouvez définir dans une classe WMI est 1024.</span><span class="sxs-lookup"><span data-stu-id="e0721-133">The maximum number of properties you can define in a WMI class is 1024.</span></span>

> [!Note]  
> <span data-ttu-id="e0721-134">Les classes ne peuvent pas être modifiées pendant l’exécution des fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="e0721-134">Classes cannot be changed during execution of providers.</span></span> <span data-ttu-id="e0721-135">Vous devez arrêter l’activité, modifier la classe, puis redémarrer le service de gestion Windows.</span><span class="sxs-lookup"><span data-stu-id="e0721-135">You must stop the activity, change the class, and then restart the Windows Management service.</span></span> <span data-ttu-id="e0721-136">La détection d’une modification de classe n’est pas possible actuellement.</span><span class="sxs-lookup"><span data-stu-id="e0721-136">Detecting a class change is currently not possible.</span></span>

 

<span data-ttu-id="e0721-137">Comme pour la classe de base, l’utilisation la plus courante de cette technique est celle des applications clientes.</span><span class="sxs-lookup"><span data-stu-id="e0721-137">As with the base class, the most common use of this technique will be by client applications.</span></span> <span data-ttu-id="e0721-138">Toutefois, un fournisseur peut également créer une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-138">However, a provider can also create a derived class.</span></span> <span data-ttu-id="e0721-139">Pour plus d’informations, consultez [création d’une classe de base](creating-a-base-class.md) et [écriture d’un fournisseur de classes](writing-a-class-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e0721-139">For more information, see [Creating a Base Class](creating-a-base-class.md) and [Writing a Class Provider](writing-a-class-provider.md).</span></span>

<span data-ttu-id="e0721-140">L’exemple de code de cette rubrique requiert que l' \# instruction include suivante soit correctement compilée.</span><span class="sxs-lookup"><span data-stu-id="e0721-140">The code example in this topic requires the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="e0721-141">La procédure suivante décrit comment créer une classe dérivée à l’aide de C++.</span><span class="sxs-lookup"><span data-stu-id="e0721-141">The following procedure describes how to create a derived class using C++.</span></span>

<span data-ttu-id="e0721-142">**Pour créer une classe dérivée à l’aide de C++**</span><span class="sxs-lookup"><span data-stu-id="e0721-142">**To create a derived class using C++**</span></span>

1.  <span data-ttu-id="e0721-143">Localisez la classe de base avec un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="e0721-143">Locate the base class with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

    <span data-ttu-id="e0721-144">L’exemple de code suivant montre comment localiser l’exemple de classe de base.</span><span class="sxs-lookup"><span data-stu-id="e0721-144">The following code example shows how to locate the Example base class.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewDerivedClass = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="e0721-145">Créez un objet dérivé de la classe de base avec un appel à [**IWbemClassObject :: SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span><span class="sxs-lookup"><span data-stu-id="e0721-145">Create a derived object from the base class with a call to [**IWbemClassObject::SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).</span></span>

    <span data-ttu-id="e0721-146">L’exemple de code suivant montre comment créer un objet de classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-146">The following code example shows how to create a derived class object.</span></span>

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  <span data-ttu-id="e0721-147">Établissez un nom pour la classe en définissant la propriété système de **\_ \_ classe** avec un appel à la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="e0721-147">Establish a name for the class by setting the **\_\_CLASS** system property with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="e0721-148">L’exemple de code suivant montre comment assigner un nom à la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-148">The following code example shows how to assign a name to the derived class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"Example2");
    BSTR Class = SysAllocString(L"__CLASS");
    pNewDerivedClass->Put(Class, 0, &v, 0);
    SysFreeString(Class);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="e0721-149">Créez des propriétés supplémentaires avec [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="e0721-149">Create additional properties with [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="e0721-150">L’exemple de code suivant montre comment créer des propriétés supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e0721-150">The following code example shows how to create additional properties.</span></span>

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  <span data-ttu-id="e0721-151">Enregistrez la nouvelle classe en appelant [**IWbemServices ::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span><span class="sxs-lookup"><span data-stu-id="e0721-151">Save the new class by calling [**IWbemServices::PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).</span></span>

    <span data-ttu-id="e0721-152">L’exemple de code suivant montre comment enregistrer la nouvelle classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-152">The following code example shows how to save the new derived class.</span></span>

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

<span data-ttu-id="e0721-153">L’exemple de code suivant combine les exemples de code présentés dans la procédure précédente pour décrire comment créer une classe dérivée à l’aide de l’API WMI.</span><span class="sxs-lookup"><span data-stu-id="e0721-153">The following code example combines the code examples discussed in the previous procedure to describe how to create a derived class using the WMI API.</span></span>


```C++
void CreateDerivedClass(IWbemServices *pSvc)
{
  IWbemClassObject *pNewDerivedClass = 0;
  IWbemClassObject *pExampleClass = 0;
  IWbemContext *pCtx = 0;
  IWbemCallResult *pResult = 0;

  BSTR PathToClass = SysAllocString(L"Example");
  HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
    &pExampleClass, &pResult);
  SysFreeString(PathToClass);

  if (hRes != 0)
    return;

  pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
  pExampleClass->Release();  // The parent class is no longer needed

  VARIANT v;
  VariantInit(&v);

  // Create the class name.
  // =====================

  V_VT(&v) = VT_BSTR;
  V_BSTR(&v) = SysAllocString(L"Example2");
  BSTR Class = SysAllocString(L"__CLASS");
  pNewDerivedClass->Put(Class, 0, &v, 0);
  SysFreeString(Class);
  VariantClear(&v);

  // Create another property.
  // =======================
  BSTR OtherProp = SysAllocString(L"OtherInfo2");
  // No default value
  pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
  SysFreeString(OtherProp);
  
  // Register the class with WMI. 
  // ============================
  hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
  pNewDerivedClass->Release();
}
```



<span data-ttu-id="e0721-154">La procédure suivante décrit comment définir une classe dérivée à l’aide de code MOF.</span><span class="sxs-lookup"><span data-stu-id="e0721-154">The following procedure describes how to define a derived class using MOF code.</span></span>

<span data-ttu-id="e0721-155">**Pour définir une classe dérivée à l’aide de code MOF**</span><span class="sxs-lookup"><span data-stu-id="e0721-155">**To define a derived class using MOF code**</span></span>

1.  <span data-ttu-id="e0721-156">Définissez votre classe dérivée avec le mot clé **Class** , suivi du nom de votre classe dérivée et du nom de la classe parente séparés par un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="e0721-156">Define your derived class with the **Class** keyword, followed by the name of your derived class, and the name of the parent class separated by a colon.</span></span>

    <span data-ttu-id="e0721-157">L’exemple de code suivant décrit une implémentation d’une classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="e0721-157">The following code example describes an implementation of a derived class.</span></span>

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32   dwProp1;
        uint32       dwProp2;
    };

    class MyDerivedClass : MyClass
    {
        string   strDerivedProp;
        sint32   dwDerivedProp;
    };
    ```

2.  <span data-ttu-id="e0721-158">Lorsque vous avez terminé, compilez votre code MOF avec le compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="e0721-158">When complete, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="e0721-159">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="e0721-159">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0721-160">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e0721-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0721-161">Création d’une classe</span><span class="sxs-lookup"><span data-stu-id="e0721-161">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



