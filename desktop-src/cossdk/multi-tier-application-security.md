---
description: Sécurité des applications multiniveau
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Sécurité des applications multiniveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69ba43970c2af5ff6c7abb733767b721091f6a3d3407178d5360e5f96db11d99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070468"
---
# <a name="multi-tier-application-security"></a>Sécurité des applications multiniveau

Vous pouvez faire face à des choix difficiles pour déterminer précisément où appliquer la sécurité dans une application multiniveau basée sur des composants : au niveau de la base de données ? Au niveau intermédiaire ? Dans les composants ? Autre chose ? Importe? À mesure que les mécanismes de sécurité augmentent le nombre et la complexité, les baisses de performances et le comportement de l’application deviennent moins prévisibles. Toutefois, vous devez vous assurer que les données sont protégées, que les règles d’entreprise sont suivies et que l’activité importante est journalisée, et que votre application fonctionne toujours pour les clients comme prévu. Vous devez être certain que tous les chemins d’accès client à l’aide de votre application sont corrects et que les points de contrôle de sécurité que vous avez en place seront suffisants.

La décision la plus difficile est souvent d’assurer la sécurité au niveau de la base de données. Historiquement, c’est là que la sécurité est la plus étroite, car elle est perçue comme un règne qui doit être véritablement sécurisé, et les administrateurs de base de données sont très réticents à faire confiance à une autre personne pour mettre en œuvre la sécurité. Toutefois, l’application de la sécurité au niveau de la base de données peut être très coûteuse et difficile à mettre à l’échelle, ce qui est précisément le point d’écrire des applications multiniveaux en premier lieu.

La règle générale à suivre avec les applications multiniveaux évolutives à l’aide de COM+ est que, chaque fois que cela est possible, vous devez appliquer une sécurité détaillée dans l’application COM+ au niveau intermédiaire. Cela vous permet de tirer pleinement parti des services évolutifs fournis par COM+. S’authentifier au niveau de la base de données uniquement lorsque vous en avez absolument besoin et peser entièrement les implications en matière de performances.

Pour plus d’informations sur les problèmes à prendre en compte lorsque vous décidez de l’emplacement des contrôles de sécurité, consultez [décider où appliquer la sécurité](deciding-where-to-enforce-security.md).

Pour plus d’informations sur certains scénarios de base pour la sécurisation des applications multiniveau, consultez [scénarios de base pour la sécurisation des données dans les applications multicouches](basic-scenarios-for-securing-data-in-multi-tier-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification du client](client-authentication.md)
</dt> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Sécurité de l’application de bibliothèque](library-application-security.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> <dt>

[Administration de la sécurité basée sur les rôles](role-based-security-administration.md)
</dt> <dt>

[Utilisation de la stratégie de restriction logicielle dans COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



