---
title: Utilisation de IProvideClassInfo
description: Utilisation de IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363652"
---
# <a name="using-iprovideclassinfo"></a>Utilisation de IProvideClassInfo

Un objet connectable peut offrir les interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) et [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) afin que ses clients puissent examiner facilement ses informations de type. Cette fonctionnalité est importante pour traiter les interfaces sortantes, qui, par définition, sont définies par un objet mais implémentées par un client sur son propre objet récepteur. Dans certains cas, une interface sortante est connue au moment de la compilation pour l’objet connectable et l’objet récepteur. C’est le cas avec [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).

Dans d’autres cas, toutefois, seul l’objet connectable connaît ses définitions d’interface sortantes au moment de la compilation. Dans ce cas, le client doit obtenir les informations de type pour l’interface sortante afin qu’il puisse fournir dynamiquement un récepteur prenant en charge les points d’entrée corrects, comme suit :

1.  Le client énumère les points de connexion, puis, pour obtenir les IID des interfaces sortantes prises en charge par l’objet connectable, appelle [**IConnectionPoint :: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) pour chaque point de connexion.
2.  Le client interroge l’objet connectable pour l’une des interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .
3.  Le client appelle les méthodes dans les interfaces [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) pour obtenir les informations de type pour l’interface sortante.
4.  Le client crée un objet récepteur qui prend en charge l’interface sortante.
5.  Le processus se poursuit et le client appelle [**IConnectionPoint :: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) pour connecter son récepteur au point de connexion.

Dans les informations de type, la [**source**](/windows/desktop/Midl/source) d’attribut marque une [**interface**](/windows/desktop/Midl/interface) ou [**dispinterface**](/windows/desktop/Midl/dispinterface) listée sous une [**coclasse**](/windows/desktop/Midl/coclass) comme une interface sortante. Ceux qui sont répertoriés sans cet attribut sont considérés comme des interfaces entrantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces d’objets connectables](connectable-object-interfaces.md)
</dt> <dt>

[Fournir des informations sur la classe](providing-class-information.md)
</dt> </dl>

 

 