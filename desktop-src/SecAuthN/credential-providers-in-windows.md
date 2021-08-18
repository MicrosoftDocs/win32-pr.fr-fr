---
description: Fournisseurs d’informations d’identification dans Windows 10
ms.assetid: BCF69196-D4E4-41D0-B372-5000FD50164B
title: Fournisseurs d’informations d’identification dans Windows 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38543127709007407c013a2a8ff047f7c91f4440351653061e894f4e7c2d90d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008797"
---
# <a name="credential-providers-in-windows-10"></a>Fournisseurs d’informations d’identification dans Windows 10

Les fournisseurs d’informations d’identification constituent le mécanisme principal d’authentification des utilisateurs : ils sont actuellement la seule méthode permettant aux utilisateurs de prouver leur identité, qui est requise pour les scénarios d’authentification du système et d’ouverture de session. avec Windows 10 et l’introduction de Microsoft Passport, les fournisseurs d’informations d’identification sont plus importants que jamais. ils seront utilisés pour l’authentification dans les applications, les sites Web et bien plus encore.

Microsoft fournit un large éventail de fournisseurs d’informations d’identification dans le cadre de Windows, tels que les mots de passe, les codes confidentiels, les cartes à puce et les Windows Hello (reconnaissance des empreintes, des visages et des Iris). Ils sont appelés « fournisseurs d’informations d’identification système » dans cet article. Les OEM, les entreprises et les autres entités peuvent écrire leurs propres fournisseurs d’informations d’identification et les intégrer facilement dans Windows. Ils sont appelés « fournisseurs d’informations d’identification tiers » dans cet article. Notez que les fournisseurs d’informations d’identification v1 et v2 sont pris en charge dans Windows 10. Il est important pour les créateurs et les gestionnaires de fournisseurs d’informations d’identification tiers de comprendre ces recommandations.

## <a name="system-credential-providers"></a>Fournisseurs d’informations d’identification système

Nous vous recommandons vivement de toujours disposer d’au moins un fournisseur d’informations d’identification système pour chaque utilisateur sur l’appareil, en plus des fournisseurs d’informations d’identification tiers. En outre, pendant la configuration du fournisseur d’informations d’identification tiers, chaque utilisateur de l’appareil doit être invité à configurer au moins un fournisseur d’informations d’identification système (si aucune autre option de récupération n’est disponible ; consultez le scénario A, ci-dessous).

### <a name="scenario-a"></a>Scénario A

Un utilisateur de compte local a configuré un fournisseur d’informations d’identification tiers et l’utilise régulièrement pour se connecter à l’appareil. Une journée, l’utilisateur installe une mise à jour de l’appareil qui interrompt le fournisseur d’informations d’identification tiers, et l’utilisateur n’a pas conscience de cette modification avant de redémarrer l’ordinateur.

Au redémarrage suivant, l’utilisateur se trouve sur l’écran d’ouverture de session et ne peut pas utiliser le fournisseur d’informations d’identification tiers attendu. Si l’utilisateur a configuré un fournisseur d’informations d’identification système, l’utilisateur est en mesure de se connecter à l’ordinateur à l’aide de celui-ci. Si ce n’est pas le cas, l’utilisateur n’a aucun moyen de récupérer le compte sur l’ordinateur.

### <a name="scenario-b"></a>Scénario B

Un utilisateur de compte MSA/AD/AAD a configuré un fournisseur d’informations d’identification tiers et l’utilise régulièrement pour se connecter à l’appareil. Une journée, l’utilisateur installe une mise à jour de l’appareil qui interrompt le fournisseur d’informations d’identification tiers, et l’utilisateur n’a pas conscience de cette modification avant de redémarrer l’ordinateur.

Au redémarrage suivant, l’utilisateur se trouve sur l’écran d’ouverture de session et ne peut pas utiliser le fournisseur d’informations d’identification tiers attendu. Si l’utilisateur a configuré un fournisseur d’informations d’identification système, l’utilisateur est en mesure de se connecter à l’ordinateur à l’aide de celui-ci. Sinon, si le fournisseur d’informations d’identification de mot de passe du système est disponible, l’utilisateur peut demander/réinitialiser à distance le mot de passe et l’utiliser pour se connecter à l’ordinateur. Si aucune de ces options n’est disponible, l’utilisateur n’a aucun moyen de récupérer le compte sur l’ordinateur.

### <a name="conclusion"></a>Conclusion

En résumé, nous voulons empêcher la désactivation de tous les fournisseurs d’informations d’identification système sur un appareil. Si des fournisseurs d’informations d’identification tiers peuvent répondre à des exigences d’authentification supplémentaires pour des groupes d’utilisateurs particuliers, il est très important de s’assurer que l’utilisateur peut toujours accéder à son ordinateur en cas de modification avec rupture. Les fournisseurs d’informations d’identification système fournissent cette garantie.

## <a name="custom-credential-providers"></a>Fournisseurs d’informations d’identification personnalisés

l’infrastructure du fournisseur d’informations d’identification Windows permet aux développeurs de créer des fournisseurs d’informations d’identification personnalisés. Lorsque [Winlogon](winlogon.md) souhaite collecter des informations d’identification, l’interface utilisateur de connexion interroge chaque fournisseur d’informations d’identification pour connaître le nombre d’informations d’identification qu’il souhaite énumérer. Une fois que tous les fournisseurs ont énuméré leurs vignettes, l’interface utilisateur d’ouverture de session les affiche à l’utilisateur. L’utilisateur interagit ensuite avec une vignette pour fournir les informations d’identification nécessaires. L’interface utilisateur d’ouverture de session soumet ces informations d’identification pour l’authentification. Les fournisseurs d’informations d’identification peuvent également être utilisés par l’interface utilisateur des informations d’identification lorsque les informations d’identification sont nécessaires. Pour obtenir la liste des scénarios dans lesquels un fournisseur d’informations d’identification peut être pris en charge, consultez [**\_ \_ \_ scénario d’utilisation du fournisseur**](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario) d’informations d’identification.

Grâce à ce système, il est beaucoup plus facile de créer un fournisseur d’informations d’identification que son historique. Une grande partie du travail est gérée par la combinaison de [Winlogon](winlogon.md), de l’interface utilisateur d’ouverture de session et de l’interface utilisateur des informations d’identification. Pour ce faire, vous devrez créer votre propre implémentation de [**ICredentialProvider**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider) et [**ICredentialProviderCredential**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential). Si vous implémentez un fournisseur d’informations d’identification v2, ce qui est recommandé, vous devrez également implémenter [**ICredentialProviderCredential2**](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovidercredential2).

Il est important de noter que les fournisseurs d’informations d’identification ne sont pas des mécanismes de mise en œuvre. Ils servent simplement à collecter et à sérialiser les informations d’identification, en les soumettant pour autorisation. L’autorité locale et les packages d’authentification seront gérés et toute application de sécurité nécessaire.

en associant des fournisseurs d’informations d’identification à du matériel pris en charge, vous pouvez étendre Windows pour prendre en charge la connexion avec les informations biométriques, les mots de passe, les codes confidentiels, les certificats de carte à puce ou tout package d’authentification personnalisé que vous choisissez de créer. Vous pouvez également personnaliser l’expérience de connexion pour l’utilisateur de différentes manières. Par exemple, lorsque l’interface utilisateur de connexion interroge votre fournisseur d’informations d’identification pour les vignettes d’informations d’identification, vous pouvez spécifier une vignette par défaut pour fournir une expérience personnalisée à un utilisateur. Les fournisseurs d’informations d’identification peuvent même être conçus pour prendre en charge l’authentification unique (SSO), l’authentification des utilisateurs sur un point d’accès sécurisé, ainsi que l’ouverture de session sur l’ordinateur.

les fournisseurs d’informations d’identification sont inscrits sur un ordinateur Windows et sont responsables des éléments suivants.

-   Description des informations d’identification requises pour l’authentification.
-   Gestion de la communication et de la logique avec les autorités d’authentification externes.
-   Empaquetage des informations d’identification pour l’ouverture de session interactive et réseau.

> [!TIP]
>
> N’oubliez pas que plusieurs fournisseurs d’informations d’identification peuvent être installés sur un seul ordinateur.

## <a name="wrapping-credential-providers"></a>Encapsulage des fournisseurs d’informations d’identification

L’encapsulation d’un fournisseur d’informations d’identification système peut être effectuée pour ajouter à ce fournisseur d’informations d’identification des fonctionnalités qui ne sont pas prises en charge en mode natif. Cela n’est pas recommandé, car cela peut entraîner un comportement problématique. Des modifications peuvent être apportées au fournisseur d’informations d’identification qui peuvent être en conflit avec le wrapper, ce qui peut entraîner une mauvaise expérience utilisateur ou même empêcher l’utilisateur d’accéder à son appareil. Cela est particulièrement vrai avec la cadence de mise à jour fréquente de Windows 10.

Si des fonctionnalités d’un fournisseur d’informations d’identification sont nécessaires qui ne sont pas incluses en mode natif, le chemin d’accès recommandé consiste à créer un fournisseur d’informations d’identification personnalisé. Il s’agit d’une approche plus stable qui ne prend pas de dépendances vis-à-vis des fournisseurs système.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[expérience de connexion Windows basée sur le fournisseur d’informations d’identification](https://go.microsoft.com/fwlink/?LinkId=717287)
</dt> <dt>

[ICredentialProvider](/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovider)
</dt> <dt>

[\_sérialisation des \_ informations d' \_ identification du fournisseur d’informations d’identification](/windows/desktop/api/credentialprovider/ns-credentialprovider-credential_provider_credential_serialization)
</dt> <dt>

[\_scénario d' \_ utilisation du fournisseur d’informations d’identification \_](/windows/desktop/api/credentialprovider/ne-credentialprovider-credential_provider_usage_scenario)
</dt> </dl>

 

 
