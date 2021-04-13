---
title: Anatomie d’un fichier IDL
description: Ces exemples de fichiers IDL illustrent les constructions fondamentales de la définition d’interface.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "104321381"
---
# <a name="anatomy-of-an-idl-file"></a><span data-ttu-id="d2095-103">Anatomie d’un fichier IDL</span><span class="sxs-lookup"><span data-stu-id="d2095-103">Anatomy of an IDL File</span></span>

<span data-ttu-id="d2095-104">Ces exemples de fichiers IDL illustrent les constructions fondamentales de la définition d’interface.</span><span class="sxs-lookup"><span data-stu-id="d2095-104">These example IDL files demonstrate the fundamental constructs of interface definition.</span></span> <span data-ttu-id="d2095-105">L’allocation de mémoire, le marshaling personnalisé et la messagerie asynchrone sont quelques-unes des fonctionnalités que vous pouvez implémenter dans une interface COM personnalisée.</span><span class="sxs-lookup"><span data-stu-id="d2095-105">Memory allocation, custom marshaling, and asynchronous messaging are just a few of the features you can implement in a custom COM interface.</span></span> <span data-ttu-id="d2095-106">Les attributs MIDL sont utilisés pour définir des interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="d2095-106">MIDL attributes are used to define COM interfaces.</span></span> <span data-ttu-id="d2095-107">Pour plus d’informations sur l’implémentation des interfaces et des bibliothèques de types, y compris un résumé des attributs MIDL, consultez [définitions et bibliothèques de types d’interface](/windows/desktop/Midl/interface-definitions-and-type-libraries) dans le Guide du programmeur MIDL et référence.</span><span class="sxs-lookup"><span data-stu-id="d2095-107">For more information about implementing interfaces and type libraries, including a summary of MIDL attributes, see [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) in the MIDL Programmer's Guide and Reference.</span></span> <span data-ttu-id="d2095-108">Pour obtenir une référence complète de tous les attributs, Mots clés et directives MIDL, consultez la référence sur le [langage MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="d2095-108">For a complete reference of all MIDL attributes, keywords, and directives, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

## <a name="exampleidl"></a><span data-ttu-id="d2095-109">Exemple. idl</span><span class="sxs-lookup"><span data-stu-id="d2095-109">Example.idl</span></span>

<span data-ttu-id="d2095-110">L’exemple de fichier IDL suivant définit deux interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="d2095-110">The following example IDL file defines two COM interfaces.</span></span> <span data-ttu-id="d2095-111">À partir de ce fichier IDL, Midl.exe générera un proxy/stub et le code de marshaling et des fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="d2095-111">From this IDL file, Midl.exe will generate proxy/stub and marshaling code and header files.</span></span> <span data-ttu-id="d2095-112">Une dissection ligne par ligne suit l’exemple.</span><span class="sxs-lookup"><span data-stu-id="d2095-112">A line-by-line dissection follows the example.</span></span>

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

<span data-ttu-id="d2095-113">L’instruction [**Import**](/windows/desktop/Midl/import) IDL est utilisée ici pour importer un fichier d’en-tête, Mydefs. h, qui contient des types définis par l’utilisateur, et Unknwn. idl, qui contient la définition de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), à partir de laquelle IFace1 et IFace2 dérivent.</span><span class="sxs-lookup"><span data-stu-id="d2095-113">The IDL [**import**](/windows/desktop/Midl/import) statement is used here to bring in a header file, Mydefs.h, which contains user-defined types, and Unknwn.idl, which contains the definition of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), from which IFace1 and IFace2 derive.</span></span>

<span data-ttu-id="d2095-114">L’attribut d' [**objet**](/windows/desktop/Midl/object) identifie l’interface en tant qu’interface d’objet et indique au compilateur MIDL de générer le code proxy/stub au lieu des stubs du client et du serveur RPC.</span><span class="sxs-lookup"><span data-stu-id="d2095-114">The [**object**](/windows/desktop/Midl/object) attribute identifies the interface as an object interface and tells the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span> <span data-ttu-id="d2095-115">Les méthodes d’interface d’objet doivent avoir un type de retour [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)pour permettre au mécanisme RPC sous-jacent de signaler des erreurs pour les appels qui ne se terminent pas en raison de problèmes réseau.</span><span class="sxs-lookup"><span data-stu-id="d2095-115">Object interface methods must have a return type of [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), to allow the underlying RPC mechanism to report errors for calls that fail to complete due to network problems.</span></span>

<span data-ttu-id="d2095-116">L’attribut [**UUID**](/windows/desktop/Midl/uuid) spécifie l’identificateur d’interface (IID).</span><span class="sxs-lookup"><span data-stu-id="d2095-116">The [**uuid**](/windows/desktop/Midl/uuid) attribute specifies the interface identifier (IID).</span></span> <span data-ttu-id="d2095-117">Chaque interface, classe et bibliothèque de types doit être identifiée avec son propre identificateur unique.</span><span class="sxs-lookup"><span data-stu-id="d2095-117">Each interface, class, and type library must be identified with its own unique identifier.</span></span> <span data-ttu-id="d2095-118">Utilisez l’utilitaire Uuidgen.exe pour générer un ensemble d’ID uniques pour vos interfaces et d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="d2095-118">Use the utility Uuidgen.exe to generate a set of unique IDs for your interfaces and other components.</span></span>

<span data-ttu-id="d2095-119">Le mot clé [**interface**](/windows/desktop/Midl/interface) définit le nom de l’interface.</span><span class="sxs-lookup"><span data-stu-id="d2095-119">The [**interface**](/windows/desktop/Midl/interface) keyword defines the interface name.</span></span> <span data-ttu-id="d2095-120">Toutes les interfaces d’objet doivent dériver, directement ou indirectement, de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="d2095-120">All object interfaces must derive, directly or indirectly, from [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="d2095-121">Le paramètre [**in**](/windows/desktop/Midl/in) direction spécifie un paramètre qui est défini uniquement par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d2095-121">The [**in**](/windows/desktop/Midl/in) directional parameter specifies a parameter that is set only by the caller.</span></span> <span data-ttu-id="d2095-122">Le paramètre [**out**](/windows/desktop/Midl/out-idl) spécifie les données qui sont renvoyées à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d2095-122">The [**out**](/windows/desktop/Midl/out-idl) parameter specifies data that is passed back to the caller.</span></span> <span data-ttu-id="d2095-123">L’utilisation des deux attributs directionnels sur un paramètre spécifie que le paramètre est utilisé à la fois pour envoyer des données à la méthode et pour repasser les données à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="d2095-123">Using both directional attributes on one parameter specifies that the parameter is used both to send data to the method and to pass data back to the caller.</span></span>

<span data-ttu-id="d2095-124">L' [**attribut \_ par défaut du pointeur**](/windows/desktop/Midl/pointer-default) spécifie le type de pointeur par défaut ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)ou [**ptr**](/windows/desktop/Midl/ptr)) pour tous les pointeurs, à l’exception de ceux inclus dans les listes de paramètres.</span><span class="sxs-lookup"><span data-stu-id="d2095-124">The [**pointer\_default**](/windows/desktop/Midl/pointer-default) attribute specifies the default pointer type ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref), or [**ptr**](/windows/desktop/Midl/ptr)) for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="d2095-125">Si aucun type par défaut n’est spécifié, MIDL part du principe que les pointeurs uniques sont **uniques**.</span><span class="sxs-lookup"><span data-stu-id="d2095-125">If no default type is specified, MIDL assumes that single pointers are **unique**.</span></span> <span data-ttu-id="d2095-126">Toutefois, lorsque vous avez plusieurs niveaux de pointeurs, vous devez spécifier explicitement un type de pointeur par défaut, même si vous souhaitez que le type par défaut soit **unique**.</span><span class="sxs-lookup"><span data-stu-id="d2095-126">However, when you have multiple levels of pointers, you must explicitly specify a default pointer type, even if you want the default type to be **unique**.</span></span>

<span data-ttu-id="d2095-127">Dans l’exemple précédent, le tableau BkfstStuff \[ \] est un *tableau conforme*, dont la taille est déterminée au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2095-127">In the preceding example, the array BkfstStuff\[ \] is a *conformant array*, the size of which is determined at run time.</span></span> <span data-ttu-id="d2095-128">L’attribut [**Max \_ is**](/windows/desktop/Midl/max-is) spécifie la variable qui contient la valeur maximale pour l’index de tableau.</span><span class="sxs-lookup"><span data-stu-id="d2095-128">The [**max\_is**](/windows/desktop/Midl/max-is) attribute specifies the variable that contains the maximum value for the array index.</span></span>

<span data-ttu-id="d2095-129">L’attribut [**size \_ est**](/windows/desktop/Midl/size-is) également utilisé pour spécifier la taille d’un tableau ou, comme dans l’exemple précédent, plusieurs niveaux de pointeurs.</span><span class="sxs-lookup"><span data-stu-id="d2095-129">The [**size\_is**](/windows/desktop/Midl/size-is) attribute is also used to specify the size of an array or, as in the preceding example, multiple levels of pointers.</span></span> <span data-ttu-id="d2095-130">Dans l’exemple, l’appel peut être effectué sans connaître à l’avance la quantité de données qui sera retournée.</span><span class="sxs-lookup"><span data-stu-id="d2095-130">In the example, the call can be made without knowing in advance how much data will be returned.</span></span>

## <a name="example2idl"></a><span data-ttu-id="d2095-131">Example2. idl</span><span class="sxs-lookup"><span data-stu-id="d2095-131">Example2.idl</span></span>

<span data-ttu-id="d2095-132">L’exemple IDL suivant (qui réutilise les interfaces décrites dans l’exemple IDL précédent) illustre les différentes façons de générer des informations de bibliothèque de types pour les interfaces.</span><span class="sxs-lookup"><span data-stu-id="d2095-132">The following IDL example (which reuses the interfaces described in the previous IDL example) shows the various ways to generate type library information for interfaces.</span></span>

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

<span data-ttu-id="d2095-133">L’attribut [**helpString**](/windows/desktop/Midl/helpstring) est facultatif. vous l’utilisez pour décrire brièvement l’objet ou pour fournir une ligne d’État.</span><span class="sxs-lookup"><span data-stu-id="d2095-133">The [**helpstring**](/windows/desktop/Midl/helpstring) attribute is optional; you use it to briefly describe the object or to provide a status line.</span></span> <span data-ttu-id="d2095-134">Ces chaînes d’aide sont lisibles à l’aide d’un Explorateur d’objets, tel que celui fourni avec Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d2095-134">These help strings are readable with an object browser such as the one provided with Microsoft Visual Basic.</span></span>

<span data-ttu-id="d2095-135">L’attribut [**double**](/windows/desktop/Midl/dual) sur IFace3 crée une interface qui est à la fois une interface de dispatch et une interface com.</span><span class="sxs-lookup"><span data-stu-id="d2095-135">The [**dual**](/windows/desktop/Midl/dual) attribute on IFace3 creates an interface that is both a dispatch interface and a COM interface.</span></span> <span data-ttu-id="d2095-136">Comme elle est dérivée de **IDispatch**, une interface double prend en charge l’automatisation, ce que spécifie l’attribut [**oleautomation**](/windows/desktop/Midl/oleautomation) .</span><span class="sxs-lookup"><span data-stu-id="d2095-136">Because it is derived from **IDispatch**, a dual interface supports Automation, which is what the [**oleautomation**](/windows/desktop/Midl/oleautomation) attribute specifies.</span></span> <span data-ttu-id="d2095-137">IFace3 importe Oaidl. idl pour récupérer la définition de **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="d2095-137">IFace3 imports Oaidl.idl to get the definition of **IDispatch**.</span></span>

<span data-ttu-id="d2095-138">L’instruction [**Library**](/windows/desktop/Midl/library) définit la bibliothèque de types ExampleLib, qui a ses propres attributs [**UUID**](/windows/desktop/Midl/uuid), [**helpString**](/windows/desktop/Midl/helpstring)et [**version**](/windows/desktop/Midl/version) .</span><span class="sxs-lookup"><span data-stu-id="d2095-138">The [**library**](/windows/desktop/Midl/library) statement defines the ExampleLib type library, which has its own [**uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring), and [**version**](/windows/desktop/Midl/version) attributes.</span></span>

<span data-ttu-id="d2095-139">Dans la définition de la bibliothèque de types, la directive [**importlib**](/windows/desktop/Midl/importlib) apporte une bibliothèque de types compilée.</span><span class="sxs-lookup"><span data-stu-id="d2095-139">Within the type library definition, the [**importlib**](/windows/desktop/Midl/importlib) directive brings in a compiled type library.</span></span> <span data-ttu-id="d2095-140">Toutes les définitions de bibliothèque de types doivent intégrer la bibliothèque de types de base définie dans Stdole32. tlb.</span><span class="sxs-lookup"><span data-stu-id="d2095-140">All type library definitions should bring in the base type library defined in Stdole32.tlb.</span></span>

<span data-ttu-id="d2095-141">Cette définition de bibliothèque de types montre trois façons différentes d’inclure des interfaces dans la bibliothèque de types.</span><span class="sxs-lookup"><span data-stu-id="d2095-141">This type library definition demonstrates three different ways to include interfaces in the type library.</span></span> <span data-ttu-id="d2095-142">IFace3 est inclus simplement en le référençant dans l’instruction Library.</span><span class="sxs-lookup"><span data-stu-id="d2095-142">IFace3 is included merely by referencing it within the library statement.</span></span>

<span data-ttu-id="d2095-143">L’instruction [**coclass**](/windows/desktop/Midl/coclass) définit une classe de composant entièrement nouvelle, BkfstComponent, qui comprend deux interfaces précédemment définies, IFace1 et IFace2.</span><span class="sxs-lookup"><span data-stu-id="d2095-143">The [**coclass**](/windows/desktop/Midl/coclass) statement defines an entirely new component class, BkfstComponent, that includes two previously defined interfaces, IFace1 and IFace2.</span></span> <span data-ttu-id="d2095-144">L’attribut par défaut désigne IFace1 comme interface par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2095-144">The default attribute designates IFace1 as the default interface.</span></span>

<span data-ttu-id="d2095-145">IFace4 est décrit dans l’instruction Library.</span><span class="sxs-lookup"><span data-stu-id="d2095-145">IFace4 is described within the library statement.</span></span> <span data-ttu-id="d2095-146">L’attribut [**propput**](/windows/desktop/Midl/propput) sur Méthoded indique que la méthode exécute une action set sur une propriété du même nom.</span><span class="sxs-lookup"><span data-stu-id="d2095-146">The [**propput**](/windows/desktop/Midl/propput) attribute on MethodD indicates that the method performs a set action on a property of the same name.</span></span> <span data-ttu-id="d2095-147">L’attribut [**propget**](/windows/desktop/Midl/propget) indique que la méthode récupère les informations d’une propriété du même nom que la méthode.</span><span class="sxs-lookup"><span data-stu-id="d2095-147">The [**propget**](/windows/desktop/Midl/propget) attribute indicates that the method retrieves information from a property of the same name as the method.</span></span> <span data-ttu-id="d2095-148">L’attribut [**retVal**](/windows/desktop/Midl/retval) dans methodd désigne un paramètre OUTPUT qui contient la valeur de retour de la fonction.</span><span class="sxs-lookup"><span data-stu-id="d2095-148">The [**retval**](/windows/desktop/Midl/retval) attribute in MethodD designates an output parameter that contains the return value of the function.</span></span>

 

 
