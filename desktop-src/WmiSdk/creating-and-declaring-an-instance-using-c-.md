---
description: Vous pouvez créer une instance en C++ par le biais de l’interface IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Création et déclaration d’une instance à l’aide de C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543526"
---
# <a name="creating-and-declaring-an-instance-using-c"></a><span data-ttu-id="7e0c7-103">Création et déclaration d’une instance à l’aide de C++</span><span class="sxs-lookup"><span data-stu-id="7e0c7-103">Creating and Declaring an Instance Using C++</span></span>

<span data-ttu-id="7e0c7-104">Vous pouvez créer une instance en C++ par le biais de l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="7e0c7-104">You can create an instance in C++ through the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="7e0c7-105">Les exemples de code de cette rubrique requièrent l' \# instruction include suivante pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-105">The code examples in this topic require the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="7e0c7-106">La procédure suivante décrit comment créer une instance d’une classe existante.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-106">The following procedure describes how to create an instance of an existing class.</span></span>

<span data-ttu-id="7e0c7-107">**Pour créer une instance d’une classe existante**</span><span class="sxs-lookup"><span data-stu-id="7e0c7-107">**To create an instance of an existing class**</span></span>

1.  <span data-ttu-id="7e0c7-108">Récupérez la définition de la classe existante en appelant les méthodes [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="7e0c7-108">Retrieve the definition of the existing class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span>

    <span data-ttu-id="7e0c7-109">L’exemple de code suivant montre comment utiliser les méthodes [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) et [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) pour obtenir un pointeur vers l’interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui fournit l’accès à la définition de classe.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-109">The following code example shows how to use the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to get a pointer to the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface that provides access to the class definition.</span></span>

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  <span data-ttu-id="7e0c7-110">Créez la nouvelle instance en appelant la méthode [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="7e0c7-110">Create the new instance by calling the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

    <span data-ttu-id="7e0c7-111">L’exemple de code suivant montre comment créer une nouvelle instance, puis libérer la classe.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-111">The following code example shows how to create a new instance and then release the class.</span></span>

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  <span data-ttu-id="7e0c7-112">Définissez les valeurs des propriétés qui n’héritent pas des valeurs définies pour la classe en appelant la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="7e0c7-112">Set values for any properties that do not inherit the values defined for the class by calling the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="7e0c7-113">Chaque instance d’une classe hérite de toutes les propriétés définies pour la classe.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-113">Each instance of a class inherits all of the properties that are defined for the class.</span></span> <span data-ttu-id="7e0c7-114">Toutefois, vous pouvez spécifier des valeurs de propriété différentes si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-114">However, you can specify different property values if you choose.</span></span>

    <span data-ttu-id="7e0c7-115">Si la classe existante a une propriété de clé, vous devez affecter à la propriété la valeur **null** ou une valeur unique garantie.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-115">If the existing class has a key property, you should set the property either to **NULL** or a guaranteed unique value.</span></span> <span data-ttu-id="7e0c7-116">Si vous affectez à la clé la **valeur null** et que la clé est une chaîne, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) ou [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) génère en interne et assigne un GUID à la clé.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-116">If you set the key to **NULL** and the key is a string, then [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) or [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) internally generates and assigns a GUID to the key.</span></span> <span data-ttu-id="7e0c7-117">De cette façon, la spécification de **null** pour une propriété de clé vous permet de créer une instance unique qui ne remplacera aucune instance précédente.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-117">This way, specifying **NULL** for a key property lets you create a unique instance that will not overwrite any previous instance.</span></span>

    <span data-ttu-id="7e0c7-118">L’exemple de code suivant montre comment définir la valeur de la propriété d' [**index**](swbemrefreshableitem-index.md) de la classe d’instance example.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-118">The following code example shows how to set the [**Index**](swbemrefreshableitem-index.md) property value of the example instance class.</span></span>

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  <span data-ttu-id="7e0c7-119">Définissez les valeurs de tous les qualificateurs appropriés à l’aide d’un appel à [**IWbemClassObject :: GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span><span class="sxs-lookup"><span data-stu-id="7e0c7-119">Set the values for any relevant qualifiers through a call to [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span></span>

    <span data-ttu-id="7e0c7-120">La méthode [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) retourne un pointeur vers une interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , qui utilise pour accéder aux qualificateurs d’une classe ou d’une instance.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-120">The [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) method returns a pointer to an [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface, which use to access the qualifiers for a class or instance.</span></span> <span data-ttu-id="7e0c7-121">Vous pouvez spécifier des valeurs différentes pour un qualificateur défini pour la classe si la version du qualificateur de classe est **EnableOverride**.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-121">You can specify different values for a qualifier defined for the class if the class qualifier flavor is **EnableOverride**.</span></span> <span data-ttu-id="7e0c7-122">Vous ne pouvez pas modifier ou supprimer un qualificateur de classe avec la version définie sur **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-122">You cannot modify or delete a class qualifier with the flavor set to **DisableOverride**.</span></span> <span data-ttu-id="7e0c7-123">Pour plus d’informations, consultez [versions de qualificateur](qualifier-flavors.md).</span><span class="sxs-lookup"><span data-stu-id="7e0c7-123">For more information, see [Qualifier Flavors](qualifier-flavors.md).</span></span>

    <span data-ttu-id="7e0c7-124">En guise d’option, vous pouvez également définir des qualificateurs supplémentaires pour votre classe d’instance.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-124">As an option, you can also define additional qualifiers for your instance class.</span></span> <span data-ttu-id="7e0c7-125">Vous pouvez définir des qualificateurs supplémentaires pour la propriété d’instance ou d’instance qui n’ont pas besoin d’apparaître dans la déclaration de classe.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-125">You can define additional qualifiers for the instance or instance property which do not need to appear in the class declaration.</span></span>

5.  <span data-ttu-id="7e0c7-126">Enregistrez l’instance en appelant la méthode [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="7e0c7-126">Save the instance by calling the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method.</span></span>

    <span data-ttu-id="7e0c7-127">WMI enregistre l’instance dans l’espace de noms WMI actuel.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-127">WMI saves the instance in the current WMI namespace.</span></span> <span data-ttu-id="7e0c7-128">Par conséquent, le chemin d’accès complet de l’instance dépend de l’espace de noms, qui est généralement la racine \\ par défaut.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-128">As such, the full path of the instance is dependent on the namespace, which is typically root\\default.</span></span> <span data-ttu-id="7e0c7-129">Pour cet exemple de code, le nom de chemin d’accès complet est \\ \\ . \\ racine \\ par défaut : exemple. index = "IX100".</span><span class="sxs-lookup"><span data-stu-id="7e0c7-129">For this code example, the full path name would be \\\\.\\root\\default:Example.Index="IX100".</span></span>

    <span data-ttu-id="7e0c7-130">L’exemple de code suivant montre comment enregistrer une instance.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-130">The following code example shows how to save an instance.</span></span>

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

<span data-ttu-id="7e0c7-131">L’enregistrement de l’instance dans WMI verrouille plusieurs propriétés de l’instance.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-131">Saving the instance to WMI locks down several of the properties of the instance.</span></span>

<span data-ttu-id="7e0c7-132">Plus précisément, vous ne pouvez pas effectuer les opérations suivantes par le biais de l’API WMI après l’existence d’une instance dans l’infrastructure WMI :</span><span class="sxs-lookup"><span data-stu-id="7e0c7-132">Specifically, you cannot perform any of the following operations through the WMI API after an instance exists within the WMI infrastructure:</span></span>

-   <span data-ttu-id="7e0c7-133">Modifiez la classe parente de la classe à laquelle l’instance appartient.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-133">Change the parent class of the class to which the instance belongs.</span></span>
-   <span data-ttu-id="7e0c7-134">Ajoutez ou supprimez des propriétés.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-134">Add or remove properties.</span></span>
-   <span data-ttu-id="7e0c7-135">Modifiez les types de propriété.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-135">Change property types.</span></span>
-   <span data-ttu-id="7e0c7-136">Ajoutez ou supprimez des qualificateurs de [**clé**](standard-qualifiers.md) ou **indexés** .</span><span class="sxs-lookup"><span data-stu-id="7e0c7-136">Add or remove [**Key**](standard-qualifiers.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="7e0c7-137">Ajoutez ou supprimez des qualificateurs [**Singleton**](standard-wmi-qualifiers.md), **Dynamic** ou [**abstract**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="7e0c7-137">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

<span data-ttu-id="7e0c7-138">L’exemple de code suivant combine les exemples de code présentés dans la procédure précédente pour montrer comment créer une instance à l’aide de l’API WMI.</span><span class="sxs-lookup"><span data-stu-id="7e0c7-138">The following code example combines the code examples discussed in the previous procedure to show how to create an instance using the WMI API.</span></span>


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



