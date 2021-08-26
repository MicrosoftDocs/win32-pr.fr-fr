---
description: La méthode recommandée pour créer une nouvelle classe de base WMI pour un fournisseur WMI est dans un fichier format MOF (MOF).
ms.assetid: d46060aa-77c3-4f51-b4a7-2c3612f2bc5c
ms.tgt_platform: multiple
title: Création d’une classe de base WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780279f00eea403b330400c490da75adfa097406796cd0b14f15f9861411bfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071509"
---
# <a name="creating-a-wmi-base-class"></a>Création d’une classe de base WMI

La méthode recommandée pour créer une nouvelle classe de base WMI pour un fournisseur WMI est dans un fichier format MOF (MOF). Vous pouvez également créer une classe de base à l’aide [de l’API com pour WMI](com-api-for-wmi.md). Bien que vous puissiez créer une classe de base ou une classe dérivée dans un script, sans qu’un fournisseur fournisse des données à la classe et à ses sous-classes, la classe n’est pas utile.

Les sections suivantes sont présentées dans cette rubrique :

-   [Création d’une classe de base à l’aide de MOF](#creating-a-base-class-using-mof)
-   [Création d’une classe de base avec C++](#creating-a-base-class-with-c)
-   [Rubriques connexes](#related-topics)

## <a name="creating-a-base-class-using-mof"></a>Création d’une classe de base à l’aide de MOF

Les classes WMI s’appuient généralement sur l’héritage. Avant de créer une classe de base, vérifiez les classes Common Information Model (CIM) disponibles dans Distributed Management Task Force ([DMTF](https://www.dmtf.org/)).

Si de nombreuses classes dérivées utilisent les mêmes propriétés, placez ces propriétés et ces méthodes dans votre classe de base. Le nombre maximal de propriétés que vous pouvez définir dans une classe WMI est 1024.

Lorsque vous créez une classe de base, observez la liste suivante d’instructions pour les noms de classe :

-   Utilisez les majuscules et les minuscules.
-   Commencez un nom de classe par une lettre.
-   N’utilisez pas de trait de soulignement de début ou de fin.
-   Définissez tous les caractères restants comme des lettres, des chiffres ou des traits de soulignement.
-   Utilisez une convention d’affectation de noms cohérente.

    Bien qu’il ne soit pas nécessaire, une bonne Convention d’affectation de noms pour une classe est de deux composants joints par un trait de soulignement. Lorsque cela est possible, un nom de fournisseur doit constituer la première moitié du nom et un nom de classe descriptif doit être la deuxième partie.

> [!Note]  
> Les classes ne peuvent pas être modifiées pendant l’exécution des fournisseurs. vous devez arrêter l’activité, modifier la classe, puis redémarrer le service de gestion Windows. La détection d’une modification de classe n’est pas possible actuellement.

 

Dans MOF, créez une classe de base en la nommant avec le mot clé **Class** , mais sans indiquer une classe parente.

**Pour créer une classe de base à l’aide du code MOF**

1.  Utilisez le mot clé **Class** avec le nom de la nouvelle classe, suivi d’une paire d’accolades et d’un point-virgule. Ajoutez des propriétés et des méthodes pour la classe entre les accolades. L’exemple de code suivant est fourni.

    L’exemple de code suivant montre comment définir une classe de base.

    ``` syntax
    class MyClass_BaseDisk
    {
    };
    ```

    L’exemple de code suivant montre une définition incorrecte d’une classe de base.

    ``` syntax
    class MyClass_BaseDisk : CIM_LogicalDisk
    {
    };
    ```

2.  Ajoutez des [*qualificateurs*](gloss-q.md) de classe avant le mot clé class pour modifier la façon dont la classe est utilisée. Placez les qualificateurs entre crochets. Pour plus d’informations sur les qualificateurs permettant de modifier des classes, consultez [qualificateurs WMI](wmi-qualifiers.md). Utilisez le qualificateur **abstract** pour indiquer que vous ne pouvez pas créer une instance de cette classe directement. Les classes abstraites sont souvent utilisées pour définir des propriétés ou des méthodes qui seront utilisées par plusieurs classes dérivées. Pour plus d’informations, consultez [création d’une classe dérivée](creating-a-derived-class.md).

    L’exemple de code suivant définit la classe comme abstraite et définit le fournisseur qui fournira les données. La [*version*](gloss-f.md) du qualificateur **ToSubClass** indique que les informations contenues dans le qualificateur du **fournisseur** sont héritées par les classes dérivées.

    ``` syntax
    [Abstract, Provider("MyProvider") : ToSubClass]
    class MyClass_BaseDisk
    {
    };
    ```

3.  Ajoutez les propriétés et les méthodes de la classe à l’intérieur des crochets avant le nom de la propriété ou de la méthode. Pour plus d’informations, consultez [Ajout d’une propriété](adding-a-property.md) et [création d’une méthode](creating-a-method.md). Vous pouvez modifier ces propriétés et méthodes à l’aide de qualificateurs MOF. Pour plus d’informations, consultez [Ajout d’un qualificateur](adding-a-qualifier.md).

    L’exemple de code suivant montre comment modifier les propriétés et les méthodes avec des qualificateurs MOF.

    ``` syntax
    [read : ToSubClass, key : ToSubClass ] string DeviceID;
      [read : ToSubClass] uint32 State;
      [read : ToSubclass, write : ToSubClass] uint64 LimitUsers;
    ```

4.  Enregistrez le fichier MOF avec l’extension. mof.
5.  Inscrivez la classe avec WMI en exécutant [**Mofcomp.exe**](mofcomp.md) sur le fichier.

    **mofcomp.exe** *newmof. mof*

    Si vous n’utilisez pas le commutateur **-N** ou l' \# [**espace de noms du pragma**](pragma-namespace.md) de commande du préprocesseur pour spécifier un espace de noms, les classes MOF compilées sont stockées dans l' \\ espace de noms racine par défaut dans le référentiel. Pour plus d’informations, consultez [**mofcomp**](mofcomp.md).

L’exemple de code suivant combine les exemples de code MOF décrits dans la procédure précédente et montre comment créer une classe de base dans l' \\ espace de noms CIMV2 racine à l’aide de MOF.

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

Pour plus d’informations, consultez [création d’une classe dérivée](creating-a-derived-class.md) pour obtenir un exemple de classe dynamique dérivée de cette classe de base.

## <a name="creating-a-base-class-with-c"></a>Création d’une classe de base avec C++

La création d’une classe de base à l’aide de l’API WMI est principalement une série de commandes put qui définissent la classe et inscrivent la classe auprès de WMI. L’objectif principal de cette API est de permettre aux applications clientes de créer des classes de base. Toutefois, vous pouvez également faire en sorte qu’un fournisseur utilise cette API pour créer une classe de base. Par exemple, si vous pensez que le code MOF de votre fournisseur ne sera pas installé correctement, vous pouvez demander à votre fournisseur de créer automatiquement les classes appropriées dans le référentiel WMI. Pour plus d’informations sur les fournisseurs, consultez [écriture d’un fournisseur de classes](writing-a-class-provider.md).

> [!Note]  
> Les classes ne peuvent pas être modifiées pendant l’exécution des fournisseurs. vous devez arrêter l’activité, modifier la classe, puis redémarrer le service de gestion Windows. La détection d’une modification de classe n’est pas possible actuellement.

 

Le code requiert la compilation correcte de la référence suivante.


```C++
#include <wbemidl.h>
```



Vous pouvez créer une classe de base par programmation à l’aide [de l’API com pour WMI](com-api-for-wmi.md).

**Pour créer une nouvelle classe de base avec l’API WMI**

1.  Récupérez une définition de la nouvelle classe en appelant la méthode [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) avec le paramètre *strObjectPath* défini sur une valeur **null** .

    L’exemple de code suivant montre comment récupérer une définition pour une nouvelle classe.

    ```C++
    IWbemServices* pSvc = 0;
    IWbemContext* pCtx = 0;
    IWbemClassObject* pNewClass = 0;
    IWbemCallResult* pResult = 0;
    HRESULT hRes = pSvc->GetObject(0, 0, pCtx, &pNewClass, &pResult);
    ```

    

2.  Établissez un nom pour la classe en définissant la propriété système de **\_ \_ classe** avec un appel à la méthode [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    L’exemple de code suivant montre comment nommer la classe en définissant la propriété système de la **\_ \_ classe** .

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

    

3.  Créez la ou les propriétés de clé en appelant [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    L’exemple de code suivant décrit comment créer la propriété d' [**index**](swbemrefreshableitem-index.md) , qui est étiquetée comme une propriété de clé à l’étape 4.

    ```C++
      BSTR KeyProp = SysAllocString(L"Index");
      pNewClass->Put(KeyProp, 0, NULL, CIM_STRING);
    ```

    

4.  Attachez le qualificateur standard [**Key**](standard-qualifiers.md) à la propriété de clé en appelant d’abord la méthode [**IWbemClassObject :: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) , puis la méthode [**IWbemQualifierSet ::P ut**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) .

    L’exemple de code suivant montre comment attacher le qualificateur standard [**Key**](standard-qualifiers.md) à la propriété de clé.

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

    

5.  Créez d’autres propriétés de la classe avec [**IWbemClassObject ::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    L’exemple de code suivant décrit comment créer des propriétés supplémentaires.

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

    

6.  Inscrivez la nouvelle classe en appelant [**IWbemServices ::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    Étant donné que vous ne pouvez pas définir de clés et d’index après avoir inscrit une nouvelle classe, assurez-vous que vous avez défini toutes vos propriétés avant d’appeler [**PutClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass).

    L’exemple de code suivant décrit comment inscrire une nouvelle classe.

    ```C++
      hRes = pSvc->PutClass(pNewClass, 0, pCtx, &pResult);
      pNewClass->Release();
    ```

    

L’exemple de code suivant combine les exemples de code présentés dans la procédure précédente et montre comment créer une classe de base à l’aide de l’API WMI.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une classe](creating-a-class.md)
</dt> </dl>

 

 



