---
title: Accès aux interfaces à travers les Apartments
description: Accès aux interfaces à travers les Apartments
ms.assetid: 4e0467b9-bbf1-410c-8aab-40450a7f963a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 626707daf721aee3b440bb79ba2d1e084d154a98
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363308"
---
# <a name="accessing-interfaces-across-apartments"></a>Accès aux interfaces à travers les Apartments

COM permet à n’importe quel cloisonnement d’un processus d’obtenir l’accès à une interface implémentée sur un objet dans n’importe quel autre cloisonnement du processus. Cette opération s’effectue par le biais de l’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Cette interface a trois méthodes, qui vous permettent d’effectuer les opérations suivantes :

-   Inscrire une interface en tant qu’interface *globale* (échelle).
-   Obtient un pointeur vers cette interface à partir de tout autre cloisonnement via un cookie.
-   Révoque l’inscription globale d’une interface.

L’interface [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) est un moyen efficace pour un processus de stocker un pointeur d’interface dans un emplacement de mémoire accessible à partir de plusieurs cloisonnements au sein du processus, tels que des variables à l’ensemble du processus et des objets *agile* (objets marshalés en thread) qui contiennent des pointeurs d’interface vers d’autres objets.

Un objet agile ne tient pas compte de l’infrastructure COM sous-jacente dans laquelle il s’exécute ; en d’autres termes, le cloisonnement, le contexte et le thread sur lequel il s’exécute. L’objet peut contenir des interfaces spécifiques à un cloisonnement ou à un contexte. Pour cette raison, l’appel de ces interfaces à partir de partout où le composant agile s’exécute peut ne pas toujours fonctionner correctement. La table d’interface globale évite ce problème en garantissant qu’un proxy (ou pointeur direct) valide pour l’objet est utilisé, en fonction de l’endroit où l’objet agile s’exécute.

> [!Note]  
> La table d’interface globale n’étant pas portable au-delà des limites des processus ou des ordinateurs, elle ne peut pas être utilisée à la place du mécanisme de passage de paramètres normal.

 

Pour plus d’informations sur la création et l’utilisation d’une table d’interface globale, consultez les rubriques suivantes :

-   [Création de la table d’interface globale](creating-the-global-interface-table.md)
-   [Quand utiliser la table d’interface globale](when-to-use-the-global-interface-table.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Choix du modèle de thread](choosing-the-threading-model.md)
</dt> <dt>

[Apartments (cloisonnés) multithread](multithreaded-apartments.md)
</dt> <dt>

[Problèmes liés aux threads du serveur in-process](in-process-server-threading-issues.md)
</dt> <dt>

[Processus, threads et Apartments](processes--threads--and-apartments.md)
</dt> <dt>

[Communication monothread et multithread](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartments (cloisonnés) à thread unique](single-threaded-apartments.md)
</dt> </dl>

 

 




