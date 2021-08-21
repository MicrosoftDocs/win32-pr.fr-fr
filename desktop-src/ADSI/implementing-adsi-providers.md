---
title: Implémentation des fournisseurs d’interfaces de service Active Directory
description: Les interfaces ADSI (Active Directory Service Interfaces) sont des interfaces COM qui encapsulent des objets de service d’annuaire pour les exposer aux clients des services d’annuaire. En fournissant une implémentation d’ADSI, vous étendez votre client-base à l’ensemble des applications clientes ADSI.
ms.assetid: f86f36f0-44ff-41b7-8cf6-b97b721a8572
ms.tgt_platform: multiple
keywords:
- Implémentation des fournisseurs d’interfaces de service Active Directory ADSI
- Implémentation de l’interface ADSI des fournisseurs ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd3eb1275398a82a2ef179678e56cb9a7eda2e63eb4278906fc925fcb1d7cf6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427558"
---
# <a name="implementing-active-directory-service-interfaces-providers"></a>Implémentation des fournisseurs d’interfaces de service Active Directory

Les interfaces ADSI (Active Directory Service Interfaces) sont des interfaces COM qui encapsulent des objets de service d’annuaire pour les exposer aux clients des services d’annuaire. En fournissant une implémentation d’ADSI, vous étendez votre client-base à l’ensemble des applications clientes ADSI.

Comme pour toute implémentation COM, vous pouvez écrire un fournisseur ADSI dans de nombreux langages. les interfaces COM ADSI sont définies comme des interfaces doubles qui autorisent la résolution de noms au moment de l’exécution et au moment de la compilation et peuvent être appelées par des langages conformes à Automation tels que Visual Basic, Visual Basic édition scripting Edition, ainsi que des langages plus performants de performances et d’efficacité tels que C et C++. Les clients ADSI incluent également les applications Web à l’aide des composants logiciels enfichables pages et administration de Active Server via Microsoft Management Console.

Étant donné que l’interface ADSI fournit son propre OLE DB fournisseur, l’implémentation des fonctionnalités de recherche définies par [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) permet également aux clients ADSI d’interroger votre service d’annuaire à la recherche de données.

Tous les objets de service d’annuaire peuvent être représentés par un objet ADSI générique prenant en charge [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). ADSI fournit les blocs de construction nécessaires pour représenter les fonctionnalités et les services d’un service d’annuaire.

En outre, les interfaces méta ADSI représentent des objets communs utilisés par les administrateurs de l’annuaire. Vous mappez les propriétés des méta-interfaces avec les propriétés prises en charge par votre service d’annuaire. Les clients ADSI programmant sur les interfaces du service Active Directory accèdent à votre service d’annuaire dès que le fournisseur est installé et que le système a redémarré.

Si votre service d’annuaire prend en charge une représentation de schéma, la prise en charge des interfaces de gestion de schéma rend votre espace de noms accessible directement aux navigateurs de service d’annuaire. En publiant vos fonctionnalités par le biais du schéma, les clients peuvent interroger votre service d’annuaire en ligne et tirer parti des services que vous offrez. En raison de la disponibilité du schéma en ligne et de l’avantage de l’interface COM, vous pouvez continuer à mettre de nouvelles fonctionnalités à la disposition de votre logiciel client tout en prenant en charge les versions de niveau supérieur.

 

 




