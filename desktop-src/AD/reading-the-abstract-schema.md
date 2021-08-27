---
title: Lecture du schéma abstrait
description: Cette rubrique fournit un exemple de code et des instructions pour la lecture à partir du schéma abstrait, qui fournit un sous-ensemble des données stockées dans les objets attributeSchema et classSchema dans le conteneur de schéma.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Active Directory de schéma, lecture du schéma abstrait
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7095dc4fb5ffe5f11f64781ecd423a60b3d434d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881305"
---
# <a name="reading-the-abstract-schema"></a>Lecture du schéma abstrait

Cette rubrique fournit un exemple de code et des instructions pour la lecture à partir du schéma abstrait, qui fournit un sous-ensemble des données stockées dans les objets **attributeSchema** et **classSchema** dans le conteneur de schéma. Pour récupérer des données qui ne sont pas disponibles dans le schéma abstrait, lisez les données directement à partir du conteneur de schéma, comme décrit dans [lecture des objets AttributeSchema et classSchema](reading-attributeschema-and-classschema-objects.md).

Utilisez la chaîne de liaison « LDAP://schema » pour établir une liaison à un pointeur [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) sur le schéma abstrait. Utilisez ce pointeur pour énumérer les entrées de la classe, de l’attribut et de la syntaxe dans le schéma abstrait. Vous pouvez également utiliser la méthode [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) pour récupérer des entrées individuelles.


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



Utilisez une chaîne de liaison similaire, « &lt; objet LDAP://Schema/ &gt; », pour effectuer une liaison directe à une entrée de classe ou d’attribut dans le schéma abstrait. Dans cette chaîne, « &lt; Object &gt; » est le **lDAPDisplayName** d’une classe ou d’un attribut. Pour les classes liées à l’interface [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; pour les attributs, liez à l’interface [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



En outre, l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) fournit la propriété [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) . Cette propriété retourne l’ADsPath de la classe d’objet dans le format de chaîne de liaison de schéma abstrait. Si vous avez un pointeur **IADs** vers un objet, vous pouvez effectuer une liaison à sa classe dans le schéma abstrait à l’aide de l’ADsPath retourné par **IADs. Schema**.

Pour les classes, le tableau suivant répertorie les principales propriétés fournies par le schéma abstrait.



| Propriété                                                             | Signification                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsClass. Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Indique s’il s’agit d’une classe abstraite.                                                                                                                                                                                                                                            |
| [**IADsClass. auxiliaire**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indique s’il s’agit d’une classe auxiliaire.                                                                                                                                                                                                                                           |
| [**IADsClass.AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Tableau de classes auxiliaires dont cette classe dérive.                                                                                                                                                                                                                                     |
| [**IADsClass. Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indique si les objets de cette classe peuvent contenir d’autres objets, ce qui est vrai si une classe comprend cette classe dans sa liste de **possibleSuperiors**.                                                                                                                                 |
| [**IADsClass.DerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | Tableau de classes dont cette classe est dérivée.                                                                                                                                                                                                                                       |
| [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Récupère un tableau des propriétés obligatoires qui doivent être définies pour une instance de la classe. La liste retournée inclut toutes les valeurs **mustContain** et **systemMustContain** pour la classe et les classes dont elle est dérivée, y compris les superclasses et les classes auxiliaires. |
| [**IADsClass. OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Récupère le governsID de la classe.                                                                                                                                                                                                                                                   |
| [**IADsClass. (OptionalProperties)**](/windows/desktop/ADSI/iadsclass-property-methods)  | Récupère un tableau des propriétés facultatives qui peuvent être définies pour une instance de la classe. La liste retournée inclut toutes les valeurs **mayContain** et **systemMayContain** pour la classe et les classes dont elle est dérivée, y compris les superclasses et les classes auxiliaires.   |
| [**IADsClass.PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | Récupère un tableau des valeurs **possibleSuperiors** pour la classe, qui indique les classes d’objets qui peuvent contenir des objets de cette classe.                                                                                                                                        |



 

Le schéma abstrait est stocké dans l’objet de sous- **schéma** dans le conteneur de schéma. Pour obtenir le nom unique de l’objet de sous- **schéma** , liez-le à RootDSE et lisez l’attribut **subSchemaSubEntry** , comme décrit dans [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md). N’oubliez pas qu’il est plus efficace de lire le schéma abstrait en liant « LDAP://schema » que par la liaison directe à l’objet de sous- **schéma** .

 

 
