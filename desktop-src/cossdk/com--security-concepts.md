---
description: COM+ fournit plusieurs fonctionnalités de sécurité que vous pouvez utiliser pour protéger vos applications COM+, allant des services que vous configurez administrativement aux API que vous pouvez appeler dans le code.
ms.assetid: 686fb391-d337-41b4-bb51-b70f27a0c300
title: Concepts de sécurité de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ca5126f4b715f84c2b8801c8ec1adc29b3cbb83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033760"
---
# <a name="com-security-concepts"></a>Concepts de sécurité de COM+

COM+ fournit plusieurs fonctionnalités de sécurité que vous pouvez utiliser pour protéger vos applications COM+, allant des services que vous configurez administrativement aux API que vous pouvez appeler dans le code.

Dans la mesure du possible, pour les applications COM+, il est préférable d’utiliser la sécurité automatique, telle que la sécurité et l’authentification déclaratives basées sur les rôles, plutôt que de configurer la sécurité au sein des composants. L’utilisation de la sécurité automatique facilite l’écriture et la maintenance des composants, facilite la conception de la sécurité dans l’ensemble de l’application, et, car elle est configurée de façon administrative et plus facile à modifier la stratégie de sécurité d’une application. Ces services de sécurité automatique vous permettent de conserver toutes les fonctionnalités liées à la sécurité de vos composants. Lorsque vous pouvez activer les services et les configurer de manière appropriée, COM+ gère les détails de l’application de la stratégie de sécurité que vous spécifiez.

Toutefois, lorsque les services de sécurité automatique de COM+ ne font pas précisément ce que vous avez besoin de faire, vous pouvez les étendre, en vous appuyant sur la plateforme de sécurité automatique fournie par COM+. Si vous choisissez de ne pas utiliser la sécurité automatique ou si vous souhaitez l’utiliser, mais que vous devez l’utiliser pour répondre aux exigences de sécurité de votre application, vous disposez des options suivantes pour configurer la sécurité par programme :

-   La sécurité basée sur les rôles par programmation, par exemple, la vérification des rôles, disponible lorsque la sécurité basée sur les rôles est activée pour votre application.
-   Emprunt d’identité : lorsque vous souhaitez utiliser l’identité d’un client pour accéder à une ressource protégée.
-   Fonctionnalités d’audit basées sur les informations de contexte d’appel de sécurité, également disponibles lorsque la sécurité basée sur les rôles est activée.

Les mécanismes que vous utilisez pour protéger une application donnée dépendent des exigences particulières de cette application. Certains choix de sécurité peuvent affecter la façon dont vous écrivez des composants, et certains peuvent avoir un impact significatif sur la conception de l’application. Avant de prendre des décisions sur la façon d’implémenter une stratégie de sécurité pour une application, vous devez tenir compte de ses exigences de sécurité dans le contexte de sa conception globale (exigences de performances, accès aux données, conception physique) et choisir la combinaison de fonctionnalités de sécurité la plus appropriée. Pour plus d’informations sur l’implémentation de la sécurité par programmation, consultez [sécurité des composants de programmation](programmatic-component-security.md).

Des descriptions succinctes des catégories, fonctionnalités et problèmes de sécurité COM+ sont fournies ici, avec des liens vers des rubriques de cette section qui fournissent une présentation détaillée de chacun des domaines importants.

> [!Note]  
> Bien que cela ne soit pas abordé dans cette section, les composants mis en file d’attente présentent également des problèmes particuliers concernant les fonctionnalités de sécurité qui leur sont disponibles. Pour plus d’informations, consultez [sécurité des composants en file d’attente](queued-components-security.md) et [développement de composants en file d’attente](developing-queued-components.md).

 

## <a name="role-based-security"></a>Sécurité basée sur les rôles

La sécurité basée sur les rôles est la fonctionnalité centrale de la sécurité des applications COM+. À l’aide de rôles, vous pouvez créer de manière administrative une stratégie d’autorisation pour une application, en choisissant (jusqu’au niveau de la méthode, le cas échéant) les utilisateurs qui peuvent accéder aux ressources. En outre, les rôles fournissent une infrastructure pour l’application de la vérification de la sécurité dans le code, si votre application nécessite un contrôle d’accès plus affiné.

La sécurité basée sur les rôles repose sur un mécanisme général qui vous permet de récupérer des informations de sécurité concernant tous les appelants en amont dans la chaîne d’appels à votre composant. Cette fonctionnalité est particulièrement utile si vous souhaitez effectuer un audit et une journalisation détaillés. Pour obtenir une description des fonctionnalités d’audit fournies par COM+, consultez [accès aux informations de contexte](accessing-security-call-context-information.md)de l’appel de sécurité.

Pour obtenir une description des problèmes de sécurité et d’administration basés sur les rôles que vous devez prendre en compte lors de son utilisation, consultez [administration de la sécurité basée sur les rôles](role-based-security-administration.md).

## <a name="client-authentication"></a>Client Authentication (Authentification du client)

Avant de pouvoir autoriser les clients à accéder aux ressources, vous devez être certain qu’ils sont ceux qu’ils disent. Pour activer cette vérification d’identité, COM+ fournit des services d’authentification. Bien que ces services soient réellement fournis à un niveau plus fondamental par COM et Microsoft Windows, une application COM+ vous permet d’activer le service d’authentification de façon administrative afin qu’il fonctionne en coulisses, transparent pour l’application. Pour obtenir une description des services d’authentification, consultez [authentification du client](client-authentication.md).

## <a name="client-impersonation-and-delegation"></a>Emprunt d’identité et délégation du client

Dans certains cas, votre application doit travailler pour le compte d’un client à l’aide de l’identité du client, par exemple, lors de l’accès à une base de données qui va authentifier le client d’origine. Pour cela, votre application doit emprunter l’identité du client. COM+ offre des fonctionnalités permettant différents niveaux d’emprunt d’identité. L’emprunt d’identité est configuré de façon administrative, mais vous devez également prendre en charge l’emprunt d’identité avec le code des composants de votre application. Pour obtenir une description de l’emprunt d’identité et des problèmes relatifs à son utilisation, consultez [emprunt d’identité du client et délégation](client-impersonation-and-delegation.md).

## <a name="using-the-software-restriction-policy-in-com"></a>Utilisation de la stratégie de restriction logicielle dans COM+

Une stratégie de restriction logicielle fournit un moyen d’exécuter du code non approuvé et, par conséquent, potentiellement dangereux, dans un environnement limité afin qu’il ne puisse pas utiliser de manière abusive les privilèges de l’utilisateur. Pour ce faire, il affecte des niveaux de confiance aux fichiers que l’utilisateur peut exécuter. Par exemple, certains fichiers système peuvent avoir un niveau de confiance totale et bénéficier d’un accès illimité aux privilèges de l’utilisateur, tandis qu’un fichier qui a été téléchargé à partir d’Internet peut être complètement non approuvé et, par conséquent, autorisé à s’exécuter uniquement dans un environnement restreint où il n’est pas autorisé à utiliser des privilèges d’utilisateur sensibles à la sécurité.

La stratégie de restriction logicielle du système est contrôlée par le biais de l’outil d’administration stratégie de sécurité locale, qui permet aux administrateurs de configurer des niveaux de confiance pour des fichiers individuels. Toutefois, toutes les applications serveur COM+ s’exécutent dans le fichier dllhost.exe. Par conséquent, COM+ offre un moyen de spécifier la stratégie de restriction logicielle pour chaque application serveur afin qu’ils n’aient pas besoin de dépendre de la stratégie de restriction du fichier dllhost.exe. Pour plus d’informations sur l’utilisation de la stratégie de restriction logicielle dans COM+, consultez [utilisation de la stratégie de restriction logicielle dans com+](using-the-software-restriction-policy-in-com-.md).

## <a name="library-application-security"></a>Sécurité de l’application de bibliothèque

Les applications de bibliothèque ont des considérations spéciales en matière de sécurité. Étant donné que ces applications s’exécutent dans le processus du client, elles sont affectées par la sécurité appliquée par le processus d’hébergement, alors qu’elles ne peuvent pas contrôler la sécurité au niveau du processus. Pour obtenir une description des facteurs à prendre en compte pour les applications de bibliothèque, consultez sécurité des applications de [bibliothèque](library-application-security.md).

## <a name="multi-tier-application-security"></a>Sécurité des applications multiniveau

Les applications COM+ sont généralement des applications de niveau intermédiaire. autrement dit, ils déplacent des informations entre les clients et les ressources principales telles que les bases de données. Des choix difficiles peuvent être impliqués pour déterminer où la sécurité doit être appliquée et dans quelle mesure. La sécurité implique par nature des compromis en matière de performances. Les plus graves se produisent lorsque vous devez appliquer la vérification de sécurité à la fois au niveau des données et au niveau intermédiaire. Pour plus d’informations sur les problèmes à prendre en compte, consultez [sécurité des applications multiniveau](multi-tier-application-security.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification du client](client-authentication.md)
</dt> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Tâches de sécurité COM+](com--security-tasks.md)
</dt> <dt>

[Sécurité de l’application de bibliothèque](library-application-security.md)
</dt> <dt>

[Sécurité des applications multiniveau](multi-tier-application-security.md)
</dt> <dt>

[Sécurité des composants de programmation](programmatic-component-security.md)
</dt> <dt>

[Administration de la sécurité basée sur les rôles](role-based-security-administration.md)
</dt> <dt>

[Utilisation de la stratégie de restriction logicielle dans COM+](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



