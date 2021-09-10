---
title: Architecture des objets connectables
description: Architecture des objets connectables
ms.assetid: 69949a3b-3ab8-4054-84d8-9256fbf39c7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9d8d2909942d1c04aed972e7891a6f4ae3f730
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363664"
---
# <a name="architecture-of-connectable-objects"></a>Architecture des objets connectables

L’objet connectable n’est qu’une partie de l’architecture globale des objets connectables. Cette technologie comprend les éléments suivants :

-   **Objet connectable.** Implémente l’interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) ; crée au moins un objet de point de connexion ; définit une interface sortante pour le client.
-   **Client.** Interroge l’objet pour obtenir des [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) pour déterminer si l’objet est connecté ; crée un objet récepteur pour implémenter l’interface sortante définie par l’objet connectable.
-   **Objet récepteur.** Implémente l’interface sortante ; utilisé pour établir une connexion à l’objet connectable.
-   **Objet point de connexion.** Implémente l’interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) et gère la connexion avec le récepteur du client.

Les relations entre le client, l’objet connectable, un point de connexion et un récepteur sont illustrées dans le diagramme suivant :

![Diagramme qui montre les points de connexion entre le client et l’objet connectable.](images/1cd44fec-5d2c-4427-846b-ccab7ec0b08a.png)

Avant que l’objet point de connexion appelle des méthodes dans l’interface du récepteur à l’étape 3 du diagramme précédent, il doit effectuer une opération [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface spécifique requise, même si le pointeur a déjà été passé dans l’appel de l’étape 2 à la méthode [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) .

Les deux objets Enumerator sont également impliqués dans cette architecture, mais ils ne sont pas affichés dans l’illustration. L’un est créé par une méthode dans [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) pour énumérer les points de connexion dans l’objet connectable. L’autre est créée par une méthode dans [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) pour énumérer les connexions actuellement établies à ce point de connexion. Un point de connexion peut prendre en charge plusieurs interfaces de récepteur connecté, et il doit itérer au sein de la liste de connexions chaque fois qu’il effectue un appel de méthode sur cette interface. Ce processus porte le nom de multidiffusion.

Lorsque vous travaillez avec des objets connectables, il est important de comprendre que l’objet connectable, chaque point de connexion, chaque récepteur et tous les énumérateurs sont des objets distincts avec des implémentations [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) distinctes, des décomptes de références distincts et des durées de vie distinctes. Un client qui utilise ces objets est toujours responsable de la libération de tous les décomptes de références qu’il détient.

> [!Note]  
> Un objet connectable peut prendre en charge plusieurs clients et peut prendre en charge plusieurs récepteurs au sein d’un client. De même, un récepteur peut être connecté à plusieurs objets connectables.

 

Les étapes permettant d’établir une connexion entre un client et un objet connectable sont les suivantes :

1.  Le client interroge [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) sur l’objet pour déterminer si l’objet est connectable. Si cet appel réussit, le client conserve un pointeur vers l’interface **IConnectionPointContainer** sur l’objet connectable et le compteur de référence d’objet connectable a été incrémenté. Dans le cas contraire, l’objet n’est pas connectable et ne prend pas en charge les interfaces sortantes.
2.  Si l’objet est connectable, le client tente ensuite d’obtenir un pointeur vers l’interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) sur un point de connexion dans l’objet connectable. Il existe deux méthodes pour obtenir ce pointeur, à la fois dans [**IConnectionPointContainer :: FindConnectionPoint**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-findconnectionpoint) et dans [**IConnectionPointContainer :: EnumConnectionPoints**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpointcontainer-enumconnectionpoints). Quelques étapes supplémentaires sont nécessaires si **EnumConnectionPoints** est utilisé. (Pour plus d’informations, consultez [utilisation de IConnectionPointContainer](using-iconnectionpointcontainer.md) .) En cas de réussite, l’objet connectable et le client prennent tous les deux en charge la même interface sortante. L’objet connectable le définit et l’appelle, et le client l’implémente. Le client peut ensuite communiquer via le point de connexion dans l’objet connectable.
3.  Le client appelle ensuite [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) sur le point de connexion pour établir une connexion entre son interface de récepteur et le point de connexion de l’objet. Après cet appel, le point de connexion de l’objet contient un pointeur vers l’interface sortante sur le récepteur.
4.  Le code à l’intérieur de [**Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) appelle [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur d’interface qui est passé, en demandant l’identificateur d’interface spécifique auquel il se connecte.
5.  L’objet appelle des méthodes sur l’interface du récepteur, si nécessaire, à l’aide du pointeur détenu par son point de connexion.
6.  Le client appelle [**Unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise) pour mettre fin à la connexion. Ensuite, le client appelle **IConnectionPoint :: Release** pour libérer sa conservation sur le point de connexion et, par conséquent, l’objet connectable principal également. Le client doit également appeler **IConnectionPointContainer :: Release** pour libérer sa conservation sur l’objet connectable principal.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces d’objets connectables](connectable-object-interfaces.md)
</dt> </dl>

 

 




