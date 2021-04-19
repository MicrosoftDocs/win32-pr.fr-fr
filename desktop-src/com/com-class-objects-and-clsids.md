---
title: Objets de classe COM et CLSID
description: Un serveur COM est implémenté en tant que classe COM.
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbfde2f379c4c7589db4cde283c8c67d720b21d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106542851"
---
# <a name="com-class-objects-and-clsids"></a>Objets de classe COM et CLSID

Un serveur COM est implémenté en tant que classe COM. Une *classe com* est une implémentation d’un groupe d’interfaces dans le code exécuté chaque fois que vous interagissez avec un objet donné. Il existe une distinction importante entre une classe C++ et une classe COM : en C++, une classe est un type, tandis qu’une classe COM est simplement une définition de l’objet et ne comporte aucun type, bien qu’un programmeur C++ puisse l’implémenter à l’aide d’une classe C++. COM est conçu pour permettre l’utilisation d’une classe par différentes applications, y compris les applications écrites sans connaissance de l’existence de cette classe particulière. Par conséquent, le code de classe pour un type donné d’objet existe dans une bibliothèque liée dynamique (DLL) ou dans une autre application exécutable (EXE).

Chaque classe COM est identifiée par un *CLSID*, un GUID 128 bits unique, que le serveur doit inscrire. COM utilise ce CLSID, à la demande d’un client, pour associer des données spécifiques à la DLL ou à l’EXE contenant le code qui implémente la classe, créant ainsi une instance de l’objet.

Pour les clients et les serveurs situés sur le même ordinateur, le CLSID du serveur est tout ce dont a besoin le client. Sur chaque ordinateur, COM gère une base de données (il utilise le registre système sur les plateformes Microsoft Windows et Macintosh) de tous les CLSID pour les serveurs installés sur le système. Il s’agit d’un mappage entre chaque CLSID et l’emplacement de la DLL ou de l’EXE qui héberge le code de ce CLSID. COM consulte cette base de données chaque fois qu’un client souhaite créer une instance d’une classe COM et utiliser ses services, de sorte que le client n’a jamais besoin de connaître l’emplacement absolu du code sur l’ordinateur.

Pour les systèmes distribués, COM fournit des entrées de Registre qui permettent à un serveur distant de s’inscrire lui-même pour une utilisation par un client. Alors que les applications ont besoin de connaître uniquement le CLSID d’un serveur, car elles peuvent s’appuyer sur le registre pour localiser le serveur, COM permet aux clients de remplacer les entrées de Registre et de spécifier des emplacements de serveur, afin de tirer pleinement parti du réseau. (Consultez [localisation d’un objet distant](locating-a-remote-object.md).)

La méthode de base pour créer une instance d’une classe s’effectue via un *objet de classe* com. Il s’agit simplement d’un objet intermédiaire qui prend en charge les fonctions communes à la création de nouvelles instances d’une classe donnée. La plupart des objets de classe utilisés pour créer des objets à partir d’un CLSID prennent en charge l’interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , une interface qui comprend la méthode [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) importante. Vous implémentez une interface **IClassFactory** pour chaque classe d’objet que vous offrez pour être instanciée. (Pour plus d’informations sur l’implémentation de **IClassFactory**, consultez [implémentation de IClassFactory](implementing-iclassfactory.md).)

> [!Note]  
> Les serveurs qui prennent en charge une autre interface de fabrique de classes personnalisée ne sont pas requis pour la prise en charge de [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) spécifiquement. Toutefois, les appels aux fonctions d’activation autres que [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) (par exemple [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)) requièrent que le serveur prenne en charge **IClassFactory**.

 

Lorsqu’un client souhaite créer une instance de l’objet du serveur, il utilise le CLSID de l’objet souhaité dans un appel à [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject). (Cet appel peut être direct ou implicite, via l’une des fonctions d’assistance de création d’objet.) Cette fonction localise le code associé au CLSID, crée un objet de classe et fournit un pointeur vers l’interface demandée. (**CoGetClassObject** prend un paramètre *riid* qui spécifie le pointeur d’interface souhaité du client.)

> [!Note]  
> COM n’a que quelques fonctions sur lesquelles la plupart des autres sont générées. Les plus importants sont probablement [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), qui sous-tend toutes les fonctions de création d’instance.

 

Avec ce pointeur, l’appelant peut créer une instance de l’objet et récupérer un pointeur vers une interface demandée sur l’objet. Il s’agit généralement d’une interface d’initialisation, utilisée pour activer l’objet (le placer dans l’État en cours d’exécution) afin que le client puisse faire tout ce qu’il veut avec l’objet. À l’aide des fonctions de base de COM, le client doit également veiller à libérer tous les pointeurs d’objet.

Un autre mécanisme d’activation d’instances d’objet s’effectue par le biais du moniker de classe. Les monikers de classe sont liés à l’objet de classe de la classe pour laquelle ils sont créés. Pour plus d’informations, consultez [monikers de classes](class-monikers.md).

COM fournit plusieurs fonctions d’assistance qui réduisent le travail de création d’instances d’objet. Celles-ci sont décrites dans [fonctions d’assistance de création d’instance](instance-creation-helper-functions.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un objet à l’aide d’un objet de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 