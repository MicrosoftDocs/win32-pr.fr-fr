---
description: Instructions de base pour la conception d’applications COM+
ms.assetid: 2d08bd05-5b0c-480c-91fd-b2bf321fc21e
title: Instructions de base pour la conception d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6552022c3a9c2f50172164d1ed60811c5272e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111046"
---
# <a name="basic-guidelines-for-designing-com-applications"></a>Instructions de base pour la conception d’applications COM+

Pour tirer pleinement parti de COM+, vous pouvez utiliser quelques recommandations de base lors de la création d’une application :

-   **Modélisez votre état durable comme un schéma de base de données, à l’aide de l’outil de base de données de votre choix.** Presque toutes les applications doivent maintenir un État durable. Les bases de données fournissent les services nécessaires pour créer un stockage durable et évolutif de l’État. Par conséquent, la première étape de la création d’une application COM+ consiste à modéliser l’État durable de votre application en tant que schéma de base de données. La base de données que vous utilisez n’a pas vraiment d’importance. la plupart des bases de données commerciales sont compatibles avec COM+. Microsoft SQL Server est un bon exemple d’une solution que vous pouvez utiliser.

-   **Modélisez la logique de votre application COM+ sous la forme d’un ensemble d’interfaces COM.** Une fois que vous avez un schéma qui représente les informations d’état de l’application, modélisez les échanges qui se produisent dans l’application en tant qu’interfaces COM. Ces interfaces modéliseront le comportement de l’application. Il s’agit également de la phase de développement lorsque vous devez déterminer les services COM+ qui conviennent le mieux à votre application.

-   **Générez des dll de composant qui contiennent des composants qui utilisent le schéma de données physique et exposent une vue logique des données à d’autres composants (le premier élément de cette liste), ainsi que des composants implémentés en termes de modèle de données logique (le deuxième élément de cette liste).** Une fois que vous disposez de la structure de la logique et des informations d’État, vous pouvez commencer à écrire du code et vous pouvez maintenant écrire des composants COM basés sur des DLL qui implémentent les interfaces en termes de schéma défini. Vos composants agissent simplement comme manipulateurs pour l’utilisation de vos informations de base de données, et vos dll de composant vous permettent de créer une application COM+ qui fonctionne et dont l’échelle est correcte.

-   **Déployez les composants dans l’environnement COM+ à l’aide des services COM+ que vous avez sélectionnés.** Une fois que vous avez créé l’application, vous pouvez déployer l’application sur un réseau ou un cluster de serveurs. Vous pouvez désormais prendre des décisions en fonction des ressources disponibles, et vous pouvez adapter chaque composant pour obtenir des performances optimales.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Hypothèses et principes de conception de COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Conception de l’application COM+ à l’aide d’UML](designing-the-com--application-using-uml.md)
</dt> <dt>

[Conseils de conception générale pour l’utilisation de COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Optimisation des interactions avec le niveau de logique métier COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Autres outils Microsoft pour la création d’applications distribuées](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



