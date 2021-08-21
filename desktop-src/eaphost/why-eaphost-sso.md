---
title: Vue d’ensemble du scénario EAPHost SSO
description: Contient deux scénarios qui illustrent les avantages d’un demandeur pour lequel l’authentification unique (SSO) est activée.
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc9be7af26844004073f21154df5ac12cb44d4eaa04fddc457b729ffe5e1083
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042777"
---
# <a name="sso-eaphost-scenario-overview"></a>Vue d’ensemble du scénario EAPHost SSO

La rubrique suivante contient deux scénarios qui illustrent les avantages d’un demandeur pour lequel l’authentification unique (SSO) est activée.

## <a name="about-the-scenarios"></a>À propos des scénarios

L’authentification unique fournit des fonctionnalités permettant de conserver des informations d’identification utilisateur supplémentaires qui sont habituellement stockées dans l’objet BLOB d’utilisateur EAP. Contrairement à d’autres processus d’informations d’identification, les demandeurs SSO peuvent résoudre les situations de connexion telles que l’itinérance AP et la modification du mot de passe sans intervention de l’utilisateur.

## <a name="sso-eap-tls-pin-caching-behavior"></a>Comportement de mise en cache du code confidentiel EAP-TLS SSO

Un demandeur peut tenter l’authentification réseau à l’aide d’une méthode EAP basée sur une carte à puce, telle que EAP-TLS (Extensible Authentication Protocol Transport Layer Security). Dans ce scénario et dans des scénarios similaires, le demandeur obtient le code confidentiel de la carte à puce auprès de l’utilisateur et récupère un certificat d’utilisateur pour l’authentification réseau, suivi d’un appel à WinLogin sur l’ordinateur local. Une fois l’authentification réussie, le demandeur met en cache l’objet BLOB de l’utilisateur et ne stocke pas les informations de code confidentiel utilisateur.

Lorsque l’utilisateur se déplace vers un autre emplacement, la reprise de session et une nouvelle authentification doivent avoir lieu. Étant donné que le certificat ne peut pas être stocké avant l’ouverture de session, l’authentification de l’utilisateur échoue et le demandeur vide l’objet BLOB de l’utilisateur. À ce stade, le code PIN de l’utilisateur est requis pour récupérer le certificat de l’utilisateur à partir de la carte à puce pour l’authentification réseau. Étant donné que l’authentification unique met en cache le code confidentiel, le certificat peut être récupéré sans intervention de l’utilisateur. Sans l’authentification unique, EAP-TLS devrait à nouveau déclencher une interface utilisateur de collection de codes confidentiels.

Pour une approche étape par étape, consultez la page [comportement de la mise en cache du code confidentiel EAP-TLS](sso-eap-tls-pin-caching-behavior-.md).

## <a name="sso-password-change-behavior"></a>Comportement de modification du mot de passe SSO

Un demandeur peut tenter une authentification réseau à l’aide d’une méthode EAP basée sur un mot de passe telle que MS-CHAPv2 (Microsoft Challenge Handshake Authentication Protocol version 2,0), configurée pour utiliser les informations d’identification WinLogin. Dans ce scénario, le demandeur collecte les informations d’identification de l’utilisateur une seule fois et les fournit à EAPHost pour l’authentification réseau. Une fois l’authentification réseau réussie, le demandeur utilise le même ensemble d’informations d’identification pour WinLogin.

Toutefois, si des informations d’identification telles que le mot de passe de l’utilisateur ont été modifiées pendant l’authentification réseau sans demandeur SSO, l’appel WinLogin suivant entraîne un échec. L’authentification unique conserve les nouvelles informations d’identification et autorise un WinLogin sans intervention supplémentaire de l’utilisateur.

Pour une approche pas à pas, consultez comportement de [modification du mot de passe SSO](sso-password-change-behavior-.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[SSO et PLAP](understanding-sso-and-plap.md)
</dt> </dl>

 

 




