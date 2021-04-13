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
# <a name="anatomy-of-an-idl-file"></a>Anatomie d’un fichier IDL

Ces exemples de fichiers IDL illustrent les constructions fondamentales de la définition d’interface. L’allocation de mémoire, le marshaling personnalisé et la messagerie asynchrone sont quelques-unes des fonctionnalités que vous pouvez implémenter dans une interface COM personnalisée. Les attributs MIDL sont utilisés pour définir des interfaces COM. Pour plus d’informations sur l’implémentation des interfaces et des bibliothèques de types, y compris un résumé des attributs MIDL, consultez [définitions et bibliothèques de types d’interface](/windows/desktop/Midl/interface-definitions-and-type-libraries) dans le Guide du programmeur MIDL et référence. Pour obtenir une référence complète de tous les attributs, Mots clés et directives MIDL, consultez la référence sur le [langage MIDL](/windows/desktop/Midl/midl-language-reference).

## <a name="exampleidl"></a>Exemple. idl

L’exemple de fichier IDL suivant définit deux interfaces COM. À partir de ce fichier IDL, Midl.exe générera un proxy/stub et le code de marshaling et des fichiers d’en-tête. Une dissection ligne par ligne suit l’exemple.

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

L’instruction [**Import**](/windows/desktop/Midl/import) IDL est utilisée ici pour importer un fichier d’en-tête, Mydefs. h, qui contient des types définis par l’utilisateur, et Unknwn. idl, qui contient la définition de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), à partir de laquelle IFace1 et IFace2 dérivent.

L’attribut d' [**objet**](/windows/desktop/Midl/object) identifie l’interface en tant qu’interface d’objet et indique au compilateur MIDL de générer le code proxy/stub au lieu des stubs du client et du serveur RPC. Les méthodes d’interface d’objet doivent avoir un type de retour [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a)pour permettre au mécanisme RPC sous-jacent de signaler des erreurs pour les appels qui ne se terminent pas en raison de problèmes réseau.

L’attribut [**UUID**](/windows/desktop/Midl/uuid) spécifie l’identificateur d’interface (IID). Chaque interface, classe et bibliothèque de types doit être identifiée avec son propre identificateur unique. Utilisez l’utilitaire Uuidgen.exe pour générer un ensemble d’ID uniques pour vos interfaces et d’autres composants.

Le mot clé [**interface**](/windows/desktop/Midl/interface) définit le nom de l’interface. Toutes les interfaces d’objet doivent dériver, directement ou indirectement, de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

Le paramètre [**in**](/windows/desktop/Midl/in) direction spécifie un paramètre qui est défini uniquement par l’appelant. Le paramètre [**out**](/windows/desktop/Midl/out-idl) spécifie les données qui sont renvoyées à l’appelant. L’utilisation des deux attributs directionnels sur un paramètre spécifie que le paramètre est utilisé à la fois pour envoyer des données à la méthode et pour repasser les données à l’appelant.

L' [**attribut \_ par défaut du pointeur**](/windows/desktop/Midl/pointer-default) spécifie le type de pointeur par défaut ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)ou [**ptr**](/windows/desktop/Midl/ptr)) pour tous les pointeurs, à l’exception de ceux inclus dans les listes de paramètres. Si aucun type par défaut n’est spécifié, MIDL part du principe que les pointeurs uniques sont **uniques**. Toutefois, lorsque vous avez plusieurs niveaux de pointeurs, vous devez spécifier explicitement un type de pointeur par défaut, même si vous souhaitez que le type par défaut soit **unique**.

Dans l’exemple précédent, le tableau BkfstStuff \[ \] est un *tableau conforme*, dont la taille est déterminée au moment de l’exécution. L’attribut [**Max \_ is**](/windows/desktop/Midl/max-is) spécifie la variable qui contient la valeur maximale pour l’index de tableau.

L’attribut [**size \_ est**](/windows/desktop/Midl/size-is) également utilisé pour spécifier la taille d’un tableau ou, comme dans l’exemple précédent, plusieurs niveaux de pointeurs. Dans l’exemple, l’appel peut être effectué sans connaître à l’avance la quantité de données qui sera retournée.

## <a name="example2idl"></a>Example2. idl

L’exemple IDL suivant (qui réutilise les interfaces décrites dans l’exemple IDL précédent) illustre les différentes façons de générer des informations de bibliothèque de types pour les interfaces.

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

L’attribut [**helpString**](/windows/desktop/Midl/helpstring) est facultatif. vous l’utilisez pour décrire brièvement l’objet ou pour fournir une ligne d’État. Ces chaînes d’aide sont lisibles à l’aide d’un Explorateur d’objets, tel que celui fourni avec Microsoft Visual Basic.

L’attribut [**double**](/windows/desktop/Midl/dual) sur IFace3 crée une interface qui est à la fois une interface de dispatch et une interface com. Comme elle est dérivée de **IDispatch**, une interface double prend en charge l’automatisation, ce que spécifie l’attribut [**oleautomation**](/windows/desktop/Midl/oleautomation) . IFace3 importe Oaidl. idl pour récupérer la définition de **IDispatch**.

L’instruction [**Library**](/windows/desktop/Midl/library) définit la bibliothèque de types ExampleLib, qui a ses propres attributs [**UUID**](/windows/desktop/Midl/uuid), [**helpString**](/windows/desktop/Midl/helpstring)et [**version**](/windows/desktop/Midl/version) .

Dans la définition de la bibliothèque de types, la directive [**importlib**](/windows/desktop/Midl/importlib) apporte une bibliothèque de types compilée. Toutes les définitions de bibliothèque de types doivent intégrer la bibliothèque de types de base définie dans Stdole32. tlb.

Cette définition de bibliothèque de types montre trois façons différentes d’inclure des interfaces dans la bibliothèque de types. IFace3 est inclus simplement en le référençant dans l’instruction Library.

L’instruction [**coclass**](/windows/desktop/Midl/coclass) définit une classe de composant entièrement nouvelle, BkfstComponent, qui comprend deux interfaces précédemment définies, IFace1 et IFace2. L’attribut par défaut désigne IFace1 comme interface par défaut.

IFace4 est décrit dans l’instruction Library. L’attribut [**propput**](/windows/desktop/Midl/propput) sur Méthoded indique que la méthode exécute une action set sur une propriété du même nom. L’attribut [**propget**](/windows/desktop/Midl/propget) indique que la méthode récupère les informations d’une propriété du même nom que la méthode. L’attribut [**retVal**](/windows/desktop/Midl/retval) dans methodd désigne un paramètre OUTPUT qui contient la valeur de retour de la fonction.

 

 
