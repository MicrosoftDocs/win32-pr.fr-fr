---
description: Autres outils Microsoft pour la création d’applications distribuées
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Autres outils Microsoft pour la création d’applications distribuées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513947"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a>Autres outils Microsoft pour la création d’applications distribuées

Outre les outils de COM+, Microsoft fournit les outils suivants pour aider le développeur à créer des applications distribuées :

-   Microsoft Data Access Components (MDAC). Microsoft fournit plusieurs voies pour la récupération de données à partir d’une multitude de sources. Par exemple, OLE DB offre un ensemble d’interfaces COM pour créer des composants de base de données. Les interfaces sont définies de sorte que les fournisseurs de données peuvent implémenter différents niveaux de prise en charge, en fonction des fonctionnalités du magasin de données sous-jacent. Étant donné que OLE DB est basé sur COM, il peut facilement être étendu, et les extensions sont implémentées en tant que nouvelles interfaces. OLE DB comprend également une interface de programmation au niveau de l’application, appelée ActiveX Data Objects (ADO). ADO expose des interfaces doubles. il peut donc facilement être utilisé à partir de langages de script, ainsi que Microsoft Visual C++, Visual Basic et d’autres outils de développement.

    > [!Note]  
    > Les développeurs peuvent également choisir d’utiliser une API générique, indépendante du fournisseur, telle que l’interface de programmation d’applications (API) de Microsoft Open Database Connectivity (ODBC). L’API ODBC est une interface en langage C permettant d’accéder aux données d’un SGBD à l’aide de langage SQL (SQL). Un gestionnaire de pilotes ODBC fournit les composants d’interface de programmation et d’exécution pour localiser des pilotes propres au SGBD. Les pilotes ODBC, généralement fournis par le fournisseur SGBD, traduisent les appels génériques du gestionnaire de pilotes ODBC en appels à la méthode d’accès aux données native. Le principal avantage de l’utilisation de l’API ODBC est que vous devez apprendre une seule API pour accéder à un large éventail de SGBD.

     

-   Microsoft SQL Server. En plus de fournir un système de base de données relationnelle robuste et éloquence, Microsoft SQL Server pouvez fournir une application distribuée avec le regroupement de connexions et la sécurité qui peuvent s’intégrer au modèle de sécurité Windows.

-   Intégration des transactions COM (COMTI). COMTI peut être utilisé pour intégrer des systèmes centraux à des systèmes Windows, y compris des applications COM+. COMTI utilise des protocoles de communication standard (par exemple, LU 6,2) pour la communication entre les ordinateurs Windows et les ordinateurs centraux et les mini-ordinateurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hypothèses et principes de conception de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Conception de l’application COM+ à l’aide d’UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Conseils de conception générale pour l’utilisation de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimisation des interactions avec le niveau de logique métier COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



