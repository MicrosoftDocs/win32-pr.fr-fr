---
title: Fédération
description: La Fédération permet à la délégation de l’autorité d’autorisation à d’autres membres d’un intersociété.
ms.assetid: 574496df-95dc-45f7-8c42-e646aec12e69
keywords:
- Services Web de Fédération pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45a02744c9c0a5358da35f4c31c20633c420fee9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104559898"
---
# <a name="federation"></a>Fédération

La Fédération permet à la délégation de l’autorité d’autorisation à d’autres membres d’un intersociété. Par exemple, considérez le problème d’entreprise suivant : la société de fabrication de pièces auto contoso Ltd souhaite autoriser les employés autorisés de son client Fabrikam Inc à accéder en toute sécurité au service Web de commande des pièces de contoso. Une solution de sécurité pour ce scénario est que contoso peut configurer un mécanisme d’approbation avec Fabrikam pour déléguer la décision d’autorisation d’accès à fabrikam. Ce processus peut fonctionner comme suit :

-   Fabrikam, lorsqu’il devient partenaire de contoso, configure un accord de confiance avec contoso. L’objectif de cette étape est d’accepter le type de jeton de sécurité et le contenu qui représenteront l’autorisation de Fabrikam et sera acceptable pour contoso. Par exemple, il peut être décidé qu’un certificat X. 509 approuvé avec le nom de sujet « CN = Fabrikam Inc Supplier STS » doit signer un jeton SAML pour que ce SAML soit accepté par le service Web contoso. En outre, il peut être décidé que la revendication de sécurité dans le jeton SAML émis doit être « https://schemas.contoso.com/claims/lookup » (pour l’autorisation de recherche de pièce) ou « https://schemas.contoso.com/claims/order » (pour l’autorisation de classement de pièces).
-   Lorsqu’un employé Fabrikam utilise l’application de classement des pièces internes, il contacte d’abord un service d’émission de jeton de sécurité (STS) au sein de fabrikam. Cet employé est authentifié à l’aide du mécanisme de sécurité Fabrikam interne (par exemple, nom d’utilisateur/mot de passe du domaine Windows), son autorisation de commander des pièces est vérifiée et il émet un jeton SAML de courte durée contenant les revendications appropriées et signé par le certificat X. 509 choisi ci-dessus. L’application de classement des pièces contacte ensuite le service Contoso présentant le jeton SAML émis pour authentifier et effectuer la tâche de tri.

Ici, le STS Fabrikam agit comme le « tiers émetteur » et le service de parties contoso agit comme « partie de confiance ». ![Diagramme montrant un tiers émetteur et une partie de confiance dans une Fédération.](images/stsmodel.png)

## <a name="federation-features"></a>Fonctionnalités de Fédération

Voici les fonctionnalités de sécurité prises en charge pour les tiers ou les rôles impliqués dans un scénario de Fédération :

-   Côté client : pour obtenir le jeton de sécurité du STS, il est possible d’utiliser la fonction [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) . Vous pouvez également utiliser une bibliothèque de fournisseurs de jetons de sécurité côté client comme CardSpace ou LiveID, puis utiliser leur sortie pour créer localement un jeton de sécurité à l’aide de [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken). Dans les deux cas, une fois que le client dispose du jeton de sécurité, il peut créer un canal vers le service qui spécifie la [**\_ \_ \_ \_ \_ liaison de sécurité de jeton WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding) pour présenter le jeton, ainsi qu’une liaison de sécurité de transport telle que la [**\_ \_ \_ \_ liaison de sécurité de transport WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) pour protéger le canal.
-   Côté serveur : dans un scénario de Fédération avec un service de jeton de sécurité qui émet des jetons SAML, le serveur peut utiliser la [**liaison de sécurité de message de WS \_ SAML \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding), ainsi qu’une liaison de sécurité de transport telle que la liaison de [**\_ sécurité de \_ transport \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) pour protéger le canal.
-   STS-Side : Notez que le STS est une application de service Web et qu’il peut spécifier les exigences de sécurité pour ceux qui demandent un jeton de sécurité à l’aide d’une structure de [**Description de sécurité**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) au moment de la création de l’écouteur comme tout autre service Web sécurisé. Il peut ensuite analyser les charges utiles des messages de demande entrants pour valider les demandes de jeton et renvoyer les jetons émis en tant que charges utiles de message de réponse. Actuellement, aucune fonctionnalité n’est fournie pour aider ces étapes d’analyse et d’émission.

Notez que le côté client peut gérer le jeton de sécurité émis de façon générique en tant que jeton de sécurité XML sans connaître le type de jeton ou effectuer un traitement spécifique au type de jeton. Toutefois, le serveur doit comprendre le type de jeton de sécurité spécifique afin de le comprendre et de le traiter. Les étapes de demande et de réponse de jeton de sécurité utilisent les constructions définies dans la spécification WS-Trust.

## <a name="more-complex-federation-scenarios"></a>Scénarios de Fédération plus complexes

Un scénario de Fédération peut impliquer plusieurs émission formant une chaîne de Fédération. Prenons l’exemple suivant :

-   Le client s’authentifie auprès du STS STS à l’aide d’un nom d’utilisateur et d’un mot de passe LiveID et obtient un jeton de sécurité T1.
-   Le client s’authentifie auprès de STS1 à l’aide de T1 et obtient un jeton de sécurité T2.
-   Le client s’authentifie auprès de STS2 à l’aide de T2 et obtient un jeton de sécurité T3.
-   Le client s’authentifie auprès du service cible à l’aide de T3.

Ici, L’LiveID STS, STS1, STS2 et S constituent la chaîne de Fédération. Les émission dans une chaîne de Fédération peuvent exécuter différents rôles pour le scénario d’application globale. Parmi ces rôles fonctionnels STS, citons le fournisseur d’identité, le décideur d’autorisation, Anonymizer et Resource Manager.

## <a name="sts-request-parameters-and-metadata-exchange"></a>Paramètres de demande STS et échange de métadonnées

Pour que le client réussisse un appel [**WsRequestSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsrequestsecuritytoken) , il doit connaître les paramètres de cet appel (tels que le type de jeton et les types de revendication requis), les spécifications de la description de la [**sécurité**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) du canal de demande au STS et l’adresse du [point de terminaison](endpoint-address.md) du STS. L’application cliente peut utiliser l’une des techniques suivantes pour déterminer ces informations :

-   Coder en dur les informations de l’application dans le cadre des décisions au moment de la conception.
-   Lisez ces informations à partir d’un fichier de configuration au niveau de l’application configuré par le programme de déploiement d’applications local.
-   Détectez dynamiquement ces informations au moment de l’exécution à l’aide de la fonctionnalité d' [importation de métadonnées](metadata-import.md) avec la structure de [**contrainte de \_ liaison de sécurité de \_ \_ message \_ \_ \_ de jeton WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) .

Pour illustrer l’utilisation de MEX dynamique avec la Fédération, considérez l’exemple 3 STS ci-dessus. Le client effectue tout d’abord un MEX dynamique avec des pour obtenir des informations sur T3 (c’est-à-dire, ce qu’il faut demander à partir de STS2), ainsi que l’adresse MEX dynamique STS2 (par exemple, où trouver STS2). Il utilise ensuite ces informations pour effectuer un MEX dynamique avec STS2 pour découvrir des informations sur T2 et STS1, et ainsi de suite.

Ainsi, les étapes MEX dynamiques s’effectuent dans l’ordre 4, 3, 2, 1 pour créer la chaîne de Fédération et les étapes de demande et de présentation du jeton sont effectuées dans l’ordre 1, 2, 3, 4 pour dérouler la chaîne de Fédération.

> [!Note]  
> Windows 7 et Windows Server 2008 R2 : WWSAPI prend uniquement en charge [WS-Trust](https://specs.xmlsoap.org/ws/2005/02/trust/WS-Trust.pdf) et [WS-SecureConversation](https://specs.xmlsoap.org/ws/2005/02/sc/WS-SecureConversation.pdf) comme défini par [Lightweight Web Services Security Profile (LWSSP)](/openspecs/windows_protocols/ms-lwssp/376af2f8-f4fe-4577-bfd5-370ac12cac2e). Pour plus d’informations sur l’implémentation de Microsoft, consultez la section relative à la [syntaxe du message](/openspecs/windows_protocols/ms-lwssp/d4f0f509-e14a-47b5-81e8-ade06a51d1ed) de LWSSP.

 

 

 