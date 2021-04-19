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
# <a name="creating-and-declaring-an-instance-using-c"></a>Création et déclaration d’une instance à l’aide de C++

Vous pouvez créer une instance en C++ par le biais de l’interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

Les exemples de code de cette rubrique requièrent l' \# instruction include suivante pour compiler correctement.


```C++
#include <wbemidl.h>
```



La procédure suivante décrit comment créer une instance d’une classe existante.

**Pour créer une instance d’une classe existante**

1.  Récupérez la définition de la classe existante en appelant les méthodes [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    L’exemple de code suivant montre comment utiliser les méthodes [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) et [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) pour obtenir un pointeur vers l’interface [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) qui fournit l’accès à la définition de classe.

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

    

2.  Créez la nouvelle instance en appelant la méthode [**IWbemClassObject :: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

    L’exemple de code suivant montre comment créer une nouvelle instance, puis libérer la classe.

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Définissez les valeurs des propriétés qui n’héritent pas des valeurs définies pour la classe en appelant la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    Chaque instance d’une classe hérite de toutes les propriétés définies pour la classe. Toutefois, vous pouvez spécifier des valeurs de propriété différentes si vous le souhaitez.

    Si la classe existante a une propriété de clé, vous devez affecter à la propriété la valeur **null** ou une valeur unique garantie. Si vous affectez à la clé la **valeur null** et que la clé est une chaîne, [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) ou [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) génère en interne et assigne un GUID à la clé. De cette façon, la spécification de **null** pour une propriété de clé vous permet de créer une instance unique qui ne remplacera aucune instance précédente.

    L’exemple de code suivant montre comment définir la valeur de la propriété d' [**index**](swbemrefreshableitem-index.md) de la classe d’instance example.

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

    

4.  Définissez les valeurs de tous les qualificateurs appropriés à l’aide d’un appel à [**IWbemClassObject :: GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    La méthode [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) retourne un pointeur vers une interface [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , qui utilise pour accéder aux qualificateurs d’une classe ou d’une instance. Vous pouvez spécifier des valeurs différentes pour un qualificateur défini pour la classe si la version du qualificateur de classe est **EnableOverride**. Vous ne pouvez pas modifier ou supprimer un qualificateur de classe avec la version définie sur **DisableOverride**. Pour plus d’informations, consultez [versions de qualificateur](qualifier-flavors.md).

    En guise d’option, vous pouvez également définir des qualificateurs supplémentaires pour votre classe d’instance. Vous pouvez définir des qualificateurs supplémentaires pour la propriété d’instance ou d’instance qui n’ont pas besoin d’apparaître dans la déclaration de classe.

5.  Enregistrez l’instance en appelant la méthode [**IWbemServices ::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) ou [**IWbemServices ::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    WMI enregistre l’instance dans l’espace de noms WMI actuel. Par conséquent, le chemin d’accès complet de l’instance dépend de l’espace de noms, qui est généralement la racine \\ par défaut. Pour cet exemple de code, le nom de chemin d’accès complet est \\ \\ . \\ racine \\ par défaut : exemple. index = "IX100".

    L’exemple de code suivant montre comment enregistrer une instance.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

L’enregistrement de l’instance dans WMI verrouille plusieurs propriétés de l’instance.

Plus précisément, vous ne pouvez pas effectuer les opérations suivantes par le biais de l’API WMI après l’existence d’une instance dans l’infrastructure WMI :

-   Modifiez la classe parente de la classe à laquelle l’instance appartient.
-   Ajoutez ou supprimez des propriétés.
-   Modifiez les types de propriété.
-   Ajoutez ou supprimez des qualificateurs de [**clé**](standard-qualifiers.md) ou **indexés** .
-   Ajoutez ou supprimez des qualificateurs [**Singleton**](standard-wmi-qualifiers.md), **Dynamic** ou [**abstract**](standard-qualifiers.md) .

L’exemple de code suivant combine les exemples de code présentés dans la procédure précédente pour montrer comment créer une instance à l’aide de l’API WMI.


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



 

 



