---
title: Obtention d’un pointeur vers un objet
description: Obtention d’un pointeur vers un objet
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc588518d5c3da884755d7db122738ca2fca257d76a1f8219867da357ef8444f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736698"
---
# <a name="getting-a-pointer-to-an-object"></a>Obtention d’un pointeur vers un objet

Comme COM n’a pas de modèle de classe strict, il existe quatre façons pour un client d’instancier ou d’obtenir un pointeur vers une interface sur un objet :

-   Appeler une fonction de bibliothèque COM qui crée un objet d’un type prédéterminé ; autrement dit, la fonction retourne un pointeur vers une seule interface spécifique pour une classe d’objet spécifique.
-   Appelez une fonction de bibliothèque COM qui peut créer un objet basé sur un identificateur de classe (CLSID) et qui retourne tout type de pointeur d’interface demandé.
-   Appelez une méthode d’une interface qui crée un autre objet (ou se connecte à une méthode existante) et retourne un pointeur d’interface sur cet objet distinct.
-   Implémentez un objet avec une interface par le biais de laquelle les autres objets transmettent directement leur pointeur d’interface au client.

Pour plus d’informations sur l’obtention de pointeurs vers d’autres interfaces sur un objet après le premier, consultez [QueryInterface : navigation dans un objet](queryinterface--navigating-in-an-object.md).

## <a name="creating-an-object-of-a-predetermined-type"></a>Création d’un objet d’un type prédéterminé

Il existe de nombreuses fonctions COM, telles que [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc), qui retournent des pointeurs vers des implémentations d’interface spécifiques. (**CoGetMalloc** récupère un pointeur vers l’allocateur de mémoire com standard.) La plupart d’entre elles sont des fonctions d’assistance, et la plupart de ces fonctions sont décrites dans les sections de référence de cette documentation, sous la zone spécifique à laquelle elles sont associées, telles que le stockage ou le transfert de données.

## <a name="creating-an-object-based-on-a-clsid"></a>Création d’un objet basé sur un CLSID

Il existe plusieurs fonctions qui, étant donné un CLSID, un client peut appeler pour créer une instance d’objet et obtenir un pointeur vers celle-ci. Toutes ces fonctions sont basées sur la fonction [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), qui crée un objet de classe et fournit un pointeur vers une interface qui vous permet de créer des instances de cette classe. Alors qu’il doit y avoir des informations qui indiquent sur quel système se trouve le serveur, il n’est pas nécessaire que ces informations soient contenues dans le client. Le client doit connaître uniquement le CLSID et jamais le chemin absolu du code du serveur. Pour plus d’informations, consultez [création d’un objet à l’aide d’un objet de classe](creating-an-object-through-a-class-object.md).

## <a name="returning-a-pointer-to-a-separate-object"></a>Retour d’un pointeur vers un objet distinct

Parmi les nombreuses méthodes d’interface qui retournent un pointeur vers un objet distinct, citons plusieurs méthodes qui créent et retournent un pointeur vers un *objet énumérateur*, ce qui vous permet de déterminer le nombre d’éléments d’un type donné géré par un objet. COM définit des interfaces pour énumérer un large éventail d’éléments, tels que des chaînes, des structures importantes, des monikers et des pointeurs d’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . Le moyen classique de créer une instance d’énumérateur et d’obtenir un pointeur vers son interface consiste à appeler une méthode à partir d’une autre interface. Par exemple, l’interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) définit deux méthodes, [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) et [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), qui retournent des pointeurs vers des interfaces sur deux objets d’énumération différents. Il existe de nombreux autres exemples dans COM de méthodes qui retournent des pointeurs vers des objets, tels que l’interface de document composé OLE [**IOleObject :: GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), qui, lorsqu’elle est appelée sur l’objet incorporé ou lié, retourne un pointeur vers l’implémentation de l’objet conteneur de [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite).

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>Implémentation d’un objet par le biais duquel passer un pointeur d’interface directement au client

Lorsque deux objets, tels qu’un conteneur de documents composés OLE et un serveur, ont besoin d’une communication bidirectionnelle, chacun implémente un objet contenant une méthode d’interface par l’intermédiaire de laquelle il peut passer un pointeur d’interface à l’autre objet. L’objet qui implémente, qui est également le client de l’objet créé, peut ensuite appeler la méthode et récupérer le pointeur passé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Clients et serveurs COM](com-clients-and-servers.md)
</dt> <dt>

[Responsabilités du serveur COM](com-server-responsibilities.md)
</dt> </dl>

 

 




