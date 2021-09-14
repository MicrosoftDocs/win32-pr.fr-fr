---
description: La création d’une classe dérivée dans WMI est très similaire à la création d’une classe de base. Comme avec une classe de base, vous devez d’abord définir la classe dérivée, puis inscrire la classe dérivée avec WMI.
ms.assetid: 8dd483b8-8bc2-4a5c-b981-6c2ffaccdb95
ms.tgt_platform: multiple
title: Création d’une classe dérivée WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b65079d206cb7a0a490622018f6d2e2df98867d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520217"
---
# <a name="creating-a-wmi-derived-class"></a>Création d’une classe dérivée WMI

La création d’une classe dérivée dans WMI est très similaire à la création d’une classe de base. Comme avec une classe de base, vous devez d’abord définir la classe dérivée, puis inscrire la classe dérivée avec WMI. La principale différence réside dans le fait que vous devez d’abord rechercher la classe parente à partir de laquelle vous souhaitez dériver. Pour plus d’informations, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md) et [écriture d’un fournisseur d’instances](writing-an-instance-provider.md).

La méthode recommandée pour créer des classes pour un fournisseur se trouve dans des fichiers format MOF (MOF). Plusieurs classes dérivées qui sont liées entre elles doivent être regroupées dans un fichier MOF, ainsi que toutes les classes de base à partir desquelles elles dérivent des propriétés ou des méthodes. Si vous placez chaque classe dans un fichier MOF distinct, chaque fichier doit être compilé pour que le fournisseur puisse fonctionner correctement.

Après avoir créé votre classe, vous devez supprimer toutes les instances de votre classe avant de pouvoir effectuer l’une des activités suivantes sur votre classe dérivée :

-   Modifiez la classe parente de votre classe dérivée.
-   Ajoutez ou supprimez des propriétés.
-   Modifiez les types de propriété.
-   Ajoutez ou supprimez des qualificateurs de [**clé**](key-qualifier.md) ou **indexés** .
-   Ajoutez ou supprimez des qualificateurs [**Singleton**](standard-wmi-qualifiers.md), **Dynamic** ou [**abstract**](standard-qualifiers.md) .

> [!Note]  
> Pour ajouter, supprimer ou modifier une propriété ou un qualificateur, appelez [**IWbemServices ::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass) ou [**SWbemObject. put \_**](swbemobject-put-.md) et définissez le paramètre flag sur « Force mode ». Le qualificateur [**abstract**](standard-qualifiers.md) peut être utilisé uniquement si la classe parente est abstraite.

 

Quand vous déclarez votre classe dérivée, observez les règles et restrictions suivantes :

-   La classe parente de la classe dérivée doit déjà exister.

    La déclaration de la classe parente peut apparaître dans le même fichier MOF que la classe dérivée ou dans un autre fichier. Si la classe parente est inconnue, le compilateur génère une erreur au moment de l’exécution.

-   Une classe dérivée ne peut avoir qu’une seule classe parente.

    WMI ne prend pas en charge l’héritage multiple. Toutefois, une classe parente peut avoir de nombreuses classes dérivées.

-   Vous pouvez définir des index pour les classes dérivées, mais WMI n’utilise pas ces index.

    Par conséquent, la spécification d’un index sur une classe dérivée n’améliore pas les performances des requêtes pour les instances de la classe dérivée. Vous pouvez améliorer les performances d’une requête sur une classe dérivée en spécifiant des propriétés indexées pour la classe parente de la classe dérivée.

-   Les définitions de classe dérivée peuvent être plus complexes et peuvent inclure des fonctionnalités telles que des alias, des qualificateurs et des versions de qualificateur.

    Pour plus d’informations, consultez [création d’un alias](creating-an-alias.md) et [Ajout d’un qualificateur](adding-a-qualifier.md).

-   Si vous souhaitez modifier un qualificateur, modifier la valeur par défaut d’une propriété de la classe de base, ou encore fortement taper une référence ou une propriété d’objet incorporée d’une classe de base, vous devez déclarer à nouveau la totalité de la classe de base.
-   Le nombre maximal de propriétés que vous pouvez définir dans une classe WMI est 1024.

> [!Note]  
> Les classes ne peuvent pas être modifiées pendant l’exécution des fournisseurs. vous devez arrêter l’activité, modifier la classe, puis redémarrer le service de gestion Windows. La détection d’une modification de classe n’est pas possible actuellement.

 

Comme pour la classe de base, l’utilisation la plus courante de cette technique est celle des applications clientes. Toutefois, un fournisseur peut également créer une classe dérivée. Pour plus d’informations, consultez [création d’une classe de base](creating-a-base-class.md) et [écriture d’un fournisseur de classes](writing-a-class-provider.md).

L’exemple de code de cette rubrique requiert que l' \# instruction include suivante soit correctement compilée.


```C++
#include <wbemidl.h>
```



La procédure suivante décrit comment créer une classe dérivée à l’aide de C++.

**Pour créer une classe dérivée à l’aide de C++**

1.  Localisez la classe de base avec un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

    L’exemple de code suivant montre comment localiser l’exemple de classe de base.

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

    

2.  Créez un objet dérivé de la classe de base avec un appel à [**IWbemClassObject :: SpawnDerivedClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawnderivedclass).

    L’exemple de code suivant montre comment créer un objet de classe dérivée.

    ```C++
    pExampleClass->SpawnDerivedClass(0, &pNewDerivedClass);
    pExampleClass->Release();  // Don't need the parent class any more
    ```

    

3.  Établissez un nom pour la classe en définissant la propriété système de **\_ \_ classe** avec un appel à la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    L’exemple de code suivant montre comment assigner un nom à la classe dérivée.

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

    

4.  Créez des propriétés supplémentaires avec [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    L’exemple de code suivant montre comment créer des propriétés supplémentaires.

    ```C++
    BSTR OtherProp = SysAllocString(L"OtherInfo2");
    pNewDerivedClass->Put(OtherProp, 0, NULL, CIM_STRING); 
    SysFreeString(OtherProp);
    ```

    

5.  Enregistrez la nouvelle classe en appelant [**IWbemServices ::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    L’exemple de code suivant montre comment enregistrer la nouvelle classe dérivée.

    ```C++
    hRes = pSvc->PutClass(pNewDerivedClass, 0, pCtx, &pResult);
    pNewDerivedClass->Release();
    ```

    

L’exemple de code suivant combine les exemples de code présentés dans la procédure précédente pour décrire comment créer une classe dérivée à l’aide de l’API WMI.


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



La procédure suivante décrit comment définir une classe dérivée à l’aide de code MOF.

**Pour définir une classe dérivée à l’aide de code MOF**

1.  Définissez votre classe dérivée avec le mot clé **Class** , suivi du nom de votre classe dérivée et du nom de la classe parente séparés par un signe deux-points.

    L’exemple de code suivant décrit une implémentation d’une classe dérivée.

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

2.  Lorsque vous avez terminé, compilez votre code MOF avec le compilateur MOF.

    Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une classe](creating-a-class.md)
</dt> </dl>

 

 



