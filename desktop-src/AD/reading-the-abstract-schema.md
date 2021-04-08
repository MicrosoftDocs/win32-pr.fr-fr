---
title: Lecture du schéma abstrait
description: Cette rubrique fournit un exemple de code et des instructions pour la lecture à partir du schéma abstrait, qui fournit un sous-ensemble des données stockées dans les objets attributeSchema et classSchema dans le conteneur de schéma.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- Active Directory de schéma, lecture du schéma abstrait
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842030"
---
# <a name="reading-the-abstract-schema"></a><span data-ttu-id="43979-104">Lecture du schéma abstrait</span><span class="sxs-lookup"><span data-stu-id="43979-104">Reading the Abstract Schema</span></span>

<span data-ttu-id="43979-105">Cette rubrique fournit un exemple de code et des instructions pour la lecture à partir du schéma abstrait, qui fournit un sous-ensemble des données stockées dans les objets **attributeSchema** et **classSchema** dans le conteneur de schéma.</span><span class="sxs-lookup"><span data-stu-id="43979-105">This topic provides a code example and guidelines for reading from the abstract schema, which provides a subset of the data stored in the **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="43979-106">Pour récupérer des données qui ne sont pas disponibles dans le schéma abstrait, lisez les données directement à partir du conteneur de schéma, comme décrit dans [lecture des objets AttributeSchema et classSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="43979-106">To retrieve data that is unavailable in the abstract schema, read the data directly from the schema container as described in [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="43979-107">Utilisez la chaîne de liaison « LDAP://schema » pour établir une liaison à un pointeur [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) sur le schéma abstrait.</span><span class="sxs-lookup"><span data-stu-id="43979-107">Use the "LDAP://schema" binding string to bind to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the abstract schema.</span></span> <span data-ttu-id="43979-108">Utilisez ce pointeur pour énumérer les entrées de la classe, de l’attribut et de la syntaxe dans le schéma abstrait.</span><span class="sxs-lookup"><span data-stu-id="43979-108">Use this pointer to enumerate the class, attribute, and syntax entries in the abstract schema.</span></span> <span data-ttu-id="43979-109">Vous pouvez également utiliser la méthode [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) pour récupérer des entrées individuelles.</span><span class="sxs-lookup"><span data-stu-id="43979-109">You can also use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to retrieve individual entries.</span></span>


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



<span data-ttu-id="43979-110">Utilisez une chaîne de liaison similaire, « LDAP://schema/ <object> », pour effectuer une liaison directe à une entrée de classe ou d’attribut dans le schéma abstrait.</span><span class="sxs-lookup"><span data-stu-id="43979-110">Use a similar binding string, "LDAP://schema/<object>", to bind directly to a class or attribute entry in the abstract schema.</span></span> <span data-ttu-id="43979-111">Dans cette chaîne, « &lt; Object &gt; » est le **lDAPDisplayName** d’une classe ou d’un attribut.</span><span class="sxs-lookup"><span data-stu-id="43979-111">In this string, "&lt;object&gt;" is the **lDAPDisplayName** of a class or attribute.</span></span> <span data-ttu-id="43979-112">Pour les classes liées à l’interface [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; pour les attributs, liez à l’interface [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .</span><span class="sxs-lookup"><span data-stu-id="43979-112">For classes bind to the [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) interface; for attributes, bind to [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) interface.</span></span>


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



<span data-ttu-id="43979-113">En outre, l’interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) fournit la propriété [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="43979-113">In addition, the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface provides the [**IADs.Schema**](/windows/desktop/ADSI/iads-property-methods) property.</span></span> <span data-ttu-id="43979-114">Cette propriété retourne l’ADsPath de la classe d’objet dans le format de chaîne de liaison de schéma abstrait.</span><span class="sxs-lookup"><span data-stu-id="43979-114">This property returns the ADsPath for the object class in abstract schema binding string format.</span></span> <span data-ttu-id="43979-115">Si vous avez un pointeur **IADs** vers un objet, vous pouvez effectuer une liaison à sa classe dans le schéma abstrait à l’aide de l’ADsPath retourné par **IADs. Schema**.</span><span class="sxs-lookup"><span data-stu-id="43979-115">If you have an **IADs** pointer to an object, you can bind to its class in the abstract schema using the ADsPath returned from **IADs.Schema**.</span></span>

<span data-ttu-id="43979-116">Pour les classes, le tableau suivant répertorie les principales propriétés fournies par le schéma abstrait.</span><span class="sxs-lookup"><span data-stu-id="43979-116">For classes, the following table lists key properties provided by the abstract schema.</span></span>



| <span data-ttu-id="43979-117">Propriété</span><span class="sxs-lookup"><span data-stu-id="43979-117">Property</span></span>                                                             | <span data-ttu-id="43979-118">Signification</span><span class="sxs-lookup"><span data-stu-id="43979-118">Meaning</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43979-119">**IADsClass. Abstract**</span><span class="sxs-lookup"><span data-stu-id="43979-119">**IADsClass.Abstract**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)            | <span data-ttu-id="43979-120">Indique s’il s’agit d’une classe abstraite.</span><span class="sxs-lookup"><span data-stu-id="43979-120">Indicates whether this is an abstract class.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="43979-121">**IADsClass. auxiliaire**</span><span class="sxs-lookup"><span data-stu-id="43979-121">**IADsClass.Auxiliary**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="43979-122">Indique s’il s’agit d’une classe auxiliaire.</span><span class="sxs-lookup"><span data-stu-id="43979-122">Indicates whether this is an auxiliary class.</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="43979-123">**IADsClass.AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="43979-123">**IADsClass.AuxDerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)      | <span data-ttu-id="43979-124">Tableau de classes auxiliaires dont cette classe dérive.</span><span class="sxs-lookup"><span data-stu-id="43979-124">Array of auxiliary classes this class derives from.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="43979-125">**IADsClass. Container**</span><span class="sxs-lookup"><span data-stu-id="43979-125">**IADsClass.Container**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="43979-126">Indique si les objets de cette classe peuvent contenir d’autres objets, ce qui est vrai si une classe comprend cette classe dans sa liste de **possibleSuperiors**.</span><span class="sxs-lookup"><span data-stu-id="43979-126">Indicates whether objects of this class can contain other objects, which is true if any class includes this class in its list of **possibleSuperiors**.</span></span>                                                                                                                                 |
| [<span data-ttu-id="43979-127">**IADsClass.DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="43979-127">**IADsClass.DerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)         | <span data-ttu-id="43979-128">Tableau de classes dont cette classe est dérivée.</span><span class="sxs-lookup"><span data-stu-id="43979-128">Array of classes that this class is derived from.</span></span>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="43979-129">**IADsClass.MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="43979-129">**IADsClass.MandatoryProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods) | <span data-ttu-id="43979-130">Récupère un tableau des propriétés obligatoires qui doivent être définies pour une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="43979-130">Retrieves an array of the mandatory properties that must be set for an instance of the class.</span></span> <span data-ttu-id="43979-131">La liste retournée inclut toutes les valeurs **mustContain** et **systemMustContain** pour la classe et les classes dont elle est dérivée, y compris les superclasses et les classes auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="43979-131">The returned list includes all the **mustContain** and **systemMustContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span> |
| [<span data-ttu-id="43979-132">**IADsClass. OID**</span><span class="sxs-lookup"><span data-stu-id="43979-132">**IADsClass.OID**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)                 | <span data-ttu-id="43979-133">Récupère le governsID de la classe.</span><span class="sxs-lookup"><span data-stu-id="43979-133">Retrieves the governsID of the class.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="43979-134">**IADsClass. (OptionalProperties)**</span><span class="sxs-lookup"><span data-stu-id="43979-134">**IADsClass.OptionalProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)  | <span data-ttu-id="43979-135">Récupère un tableau des propriétés facultatives qui peuvent être définies pour une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="43979-135">Retrieves an array of the optional properties that might be set for an instance of the class.</span></span> <span data-ttu-id="43979-136">La liste retournée inclut toutes les valeurs **mayContain** et **systemMayContain** pour la classe et les classes dont elle est dérivée, y compris les superclasses et les classes auxiliaires.</span><span class="sxs-lookup"><span data-stu-id="43979-136">The returned list includes all the **mayContain** and **systemMayContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span>   |
| [<span data-ttu-id="43979-137">**IADsClass.PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="43979-137">**IADsClass.PossibleSuperiors**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)   | <span data-ttu-id="43979-138">Récupère un tableau des valeurs **possibleSuperiors** pour la classe, qui indique les classes d’objets qui peuvent contenir des objets de cette classe.</span><span class="sxs-lookup"><span data-stu-id="43979-138">Retrieves an array of the **possibleSuperiors** values for the class, which indicates the object classes that can contain objects of this class.</span></span>                                                                                                                                        |



 

<span data-ttu-id="43979-139">Le schéma abstrait est stocké dans l’objet de sous- **schéma** dans le conteneur de schéma.</span><span class="sxs-lookup"><span data-stu-id="43979-139">The abstract schema is stored in the **subSchema** object in the schema container.</span></span> <span data-ttu-id="43979-140">Pour obtenir le nom unique de l’objet de sous- **schéma** , liez-le à RootDSE et lisez l’attribut **subSchemaSubEntry** , comme décrit dans [liaison sans serveur et RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="43979-140">To get the distinguished name of the **subSchema** object, bind to rootDSE and read the **subSchemaSubEntry** attribute, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span> <span data-ttu-id="43979-141">N’oubliez pas qu’il est plus efficace de lire le schéma abstrait en liant « LDAP://schema » que par la liaison directe à l’objet de sous- **schéma** .</span><span class="sxs-lookup"><span data-stu-id="43979-141">Be aware that it is more efficient to read the abstract schema by binding to "LDAP://schema", than by binding directly to the **subSchema** object.</span></span>

 

 