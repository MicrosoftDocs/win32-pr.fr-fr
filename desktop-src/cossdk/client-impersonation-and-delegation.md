---
description: Dans certains cas, une application serveur doit présenter une identité de clients aux ressources auxquelles elle accède au nom des clients, généralement pour faire en sorte que les contrôles d’accès ou l’authentification soient effectués sur l’identité des clients.
ms.assetid: fd75eb54-eefe-411f-a7aa-0bc8628f8778
title: Emprunt d’identité et délégation du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7557dcde4cadf559dd8e116cf4e7bece4221aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516182"
---
# <a name="client-impersonation-and-delegation"></a>Emprunt d’identité et délégation du client

Dans certains cas, une application serveur doit présenter l’identité d’un client aux ressources auxquelles elle accède au nom du client, généralement pour faire en sorte que les contrôles d’accès ou l’authentification soient effectués sur l’identité du client. Dans une certaine mesure, le serveur peut agir sous l’identité du client, une action appelée empruntant l’identité du client.

L' *emprunt d’identité* est la capacité d’un thread à s’exécuter dans un contexte de sécurité différent de celui du processus qui possède le thread. Le thread serveur utilise un jeton d’accès qui représente les informations d’identification du client et, avec cela, il peut accéder aux ressources auxquelles le client peut accéder.

L’utilisation de l’emprunt d’identité permet de s’assurer que le serveur peut faire précisément ce que le client peut faire. L’accès aux ressources peut être restreint ou développé, en fonction de ce que le client est autorisé à faire.

Vous pouvez choisir de faire en sorte qu’un serveur emprunte l’identité d’un client lors de la connexion à une base de données afin que la base de données puisse s’authentifier et autoriser le client pour lui-même. Ou, si votre application accède à des fichiers protégés par un descripteur de sécurité et pour permettre au client d’obtenir un accès autorisé aux informations contenues dans ces fichiers, l’application peut emprunter l’identité du client avant d’accéder aux fichiers.

## <a name="how-to-implement-impersonation"></a>Comment implémenter l’emprunt d’identité

L’emprunt d’identité requiert la participation du client et du serveur (et, dans certains cas, des administrateurs système). Le client doit indiquer sa volonté de laisser le serveur utiliser son identité, et le serveur doit supposer explicitement l’identité du client par programme. Pour plus d’informations, consultez les rubriques [Configuration requise côté client pour l’emprunt d’identité](client-side-requirements-for-impersonation.md) et [exigences côté serveur pour l’emprunt d’identité](server-side-requirements-for-impersonation.md).

## <a name="administrative-requirements-for-delegate-level-impersonation"></a>Configuration administrative requise pour l’emprunt d’identité Delegate-Level

Pour utiliser efficacement la forme d’emprunt d’identité la plus puissante, la *délégation*, qui est l’emprunt d’identité des clients sur le réseau, les comptes d’utilisateurs du client et du serveur doivent être correctement configurés dans le service Active Directory pour la prise en charge (en plus de l’autorité d’octroi du client pour l’emprunt d’identité au niveau du délégué), comme suit :

-   L’identité du serveur doit être marquée comme « approuvée pour la délégation » dans le service Active Directory.
-   L’identité du client ne doit pas être marquée comme « le compte est sensible et ne peut pas être délégué » dans le service Active Directory.

Ces fonctionnalités de configuration offrent à l’administrateur de domaine un degré élevé de contrôle sur la délégation, ce qui est souhaitable, compte tenu de la confiance (et donc des risques de sécurité). Pour plus d’informations sur la délégation, consultez [délégation et emprunt d’identité](/windows/desktop/com/delegation-and-impersonation).

## <a name="cloaking"></a>Masquer

En plus de l’autorité qu’un client accorde à un serveur via le niveau d’emprunt d’identité, la fonctionnalité de voilage du serveur détermine en grande partie comment l’emprunt d’identité se comportera. Le masquage affecte l’identité qui est réellement présentée par le serveur lorsqu’il effectue des appels au nom du client, son propre ou le client. Pour plus d’informations, consultez [masquage](cloaking.md).

## <a name="performance-implications"></a>Impact sur les performances

L’emprunt d’identité peut avoir un impact significatif sur les performances et la mise à l’échelle. Il est généralement plus coûteux d’emprunter l’identité d’un client sur un appel que d’effectuer l’appel directement. Voici quelques-uns des problèmes à prendre en compte :

-   La surcharge de calcul qui consiste à transmettre l’identité en modèles compliqués, en particulier si le voilage dynamique est activé.
-   La complexité générale de l’application de la vérification de la sécurité redondante à de nombreux emplacements, plutôt que de centraliser la couche intermédiaire.
-   Les ressources telles que les connexions de base de données, lors de l’ouverture d’emprunt d’identité d’un client, ne peuvent pas être réutilisées sur plusieurs clients, ce qui est un très grand obstacle à la mise à l’échelle.

Parfois, la seule solution efficace à un problème consiste à utiliser l’emprunt d’identité, mais cette décision doit être soigneusement pesée. Pour plus d’informations sur ces problèmes, consultez [sécurité des applications multiniveau](multi-tier-application-security.md).

## <a name="queued-components"></a>Composants en file d’attente

Les [composants en file d’attente](com--queued-components.md) ne prennent pas en charge l’emprunt d’identité. Lorsqu’un client effectue un appel à un objet mis en file d’attente, l’appel est effectué à l’enregistreur, qui l’empaquette dans le cadre d’un message sur le serveur. L’écouteur lit ensuite le message à partir de la file d’attente et le transmet au lecteur, qui appelle le composant serveur réel et effectue le même appel de méthode. Ainsi, lorsque le serveur reçoit l’appel, le jeton client d’origine n’est pas disponible via l’emprunt d’identité. La sécurité basée sur les rôles continue à s’appliquer, cependant, et la sécurité par programmation à l’aide de l’interface [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) fonctionnera. Pour plus d’informations, consultez [sécurité des composants en file d’attente](queued-components-security.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Authentification du client](client-authentication.md)
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

 

 
