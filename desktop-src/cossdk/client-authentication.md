---
description: L’authentification est le processus qui consiste à déterminer si les appelants sont réellement qui ils disent qu’ils sont&\# 8212 ; vérification de l’authenticité d’une revendication d’identité.
ms.assetid: c1b11f58-5bab-45d9-a686-86c95415990e
title: Client Authentication (Authentification du client)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472f16e32cb99f9f2c89c21012f1faa7f96af17878c34d16400f7d505c324398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638989"
---
# <a name="client-authentication"></a>Client Authentication (Authentification du client)

L’authentification est le processus qui consiste à déterminer si les appelants sont réellement qui ils disent qu’ils sont, en vérifiant l’authenticité d’une revendication d’identité. En général, cette opération peut être effectuée par le serveur et le client, chacun authentifiant l’autre. Toutefois, il est particulièrement important pour une application serveur qui autorise les clients, comme la sécurité basée sur les rôles, d’effectuer également l’authentification. L’authentification des clients est un prérequis pour une stratégie d’autorisation significative. Vous pouvez effectuer toutes les vérifications de rôle souhaitées, mais si vous ne savez pas si l’identité du client que vous vérifiez est authentique, votre application repose fondamentalement sur le système Honor.

Pour les applications COM+, l’authentification est un outil que vous pouvez activer et configurer de façon administrative, après quoi il fonctionne de manière transparente pour l’application. Vous spécifiez un niveau d’authentification de manière administrative à l’aide de l’outil d’administration Services de composants ou des fonctions d’administration. Pour plus d’informations sur la configuration de l’authentification, consultez [définition d’un niveau d’authentification pour une application serveur](setting-an-authentication-level-for-a-server-application.md) et [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md).

La définition de l’authentification signifie des choses différentes selon que le type d’application est une application de serveur ou de bibliothèque.

## <a name="setting-authentication-for-com-server-applications"></a>Définition de l’authentification pour les applications serveur COM+

Pour une application serveur COM+, vous définissez un niveau d’authentification qui détermine la façon dont l’authentification est effectuée lorsque les clients appellent des composants au sein de l’application. Vous pouvez choisir parmi plusieurs niveaux d’authentification qui fournissent différents degrés de sécurité, allant du non-authentification au chiffrement de chaque paquet et de tous les paramètres d’appel de méthode. Pour plus d’informations, consultez [définition d’un niveau d’authentification pour une application serveur](setting-an-authentication-level-for-a-server-application.md).

Une sécurité accrue est toutefois plus coûteuse en termes de performances, que vous devez prendre en considération lors de la configuration de votre application. COM+ négociera entre le niveau d’authentification spécifié par le client et le serveur. La façon dont cette négociation est effectuée présente l’avantage de vous permettre de contrôler l’authentification de façon administrative uniquement du côté serveur. Pour plus d’informations, consultez [négociation du niveau d’authentification](negotiation-of-authentication-level.md).

> [!Note]  
> Vous ne devez jamais spécifier un niveau d’authentification par programme à l’aide de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) dans une application com+. COM+ appelle **CoInitializeSecurity** pour vous, et cela ne peut être appelé qu’une seule fois par processus.

 

Les services d’authentification sous-jacents sont fournis par COM et Microsoft Windows. Dans un service d’authentification, un tiers fournit un certificat pour un utilisateur, en attestant de l’authenticité de l’identité de l’utilisateur. Cette certification est aussi crédible que l’autorité de certification et, à peu près de la même façon que la licence d’un conducteur ou un passeport, fait office de document de certification, elle dépend de l’autorité de l’émetteur. Pour plus d’informations sur les services d’authentification, consultez [com et packages de sécurité](/windows/desktop/com/com-and-security-packages) dans la documentation com.

## <a name="setting-authentication-for-com-library-applications"></a>Définition de l’authentification pour les applications de bibliothèque COM+

Pour une application de bibliothèque COM+, vous activez ou désactivez l’authentification pour déterminer si l’application sera soumise à l’authentification effectuée par le processus d’hébergement. Bien que l’authentification pour une application de bibliothèque COM+ soit principalement contrôlée par le processus d’hébergement, vous pouvez configurer l’application de bibliothèque de sorte qu’elle ne fasse pas partie de l’authentification. Autrement dit, les appels à l’application peuvent être authentifiés ou non authentifiés, et dans ce dernier cas, l’authentification des clients fonctionne toujours. Pour plus d’informations, consultez [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md).

En outre, vous pouvez être amené à authentifier le client au niveau de la base de données ou d’une application en aval : l’authentification des clients sur l’application COM+ seule peut ne pas suffire. Si c’est le cas, vous devez emprunter l’identité du client pour que l’identité du client soit propagée en aval. Pour plus d’informations sur l’emprunt d’identité, consultez [emprunt d’identité et délégation du client](client-impersonation-and-delegation.md). Pour plus d’informations sur les problèmes liés à la détermination de l’authentification au niveau des données, consultez [sécurité des applications multiniveau](multi-tier-application-security.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
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

 

 
