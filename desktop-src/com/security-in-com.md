---
title: Sécurité dans COM
description: la sécurité dans COM est fermement basée sur la sécurité fournie par Windows et les mécanismes de sécurité RPC sous-jacents.
ms.assetid: c9f6d06c-da24-48ea-908a-2462c33f7ee3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5e462317d85f7c445d4d8a5ae0aa4d9d3ee724
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363379"
---
# <a name="security-in-com"></a>Sécurité dans COM

la sécurité dans COM est fermement basée sur la sécurité fournie par Windows et les mécanismes de sécurité RPC sous-jacents. La sécurité COM repose sur l' *authentification* (le processus de vérification de l’identité d’un appelant) et l' *autorisation* (le processus de détermination si un appelant est autorisé à faire ce qu’il demande). Il existe deux principaux types de sécurité dans COM : la *sécurité de l’activation* et la sécurité de l' *appel*. La sécurité d’activation détermine si un client peut lancer un serveur. Une fois le serveur lancé, vous pouvez utiliser la sécurité de l’appel pour contrôler l’accès aux objets d’un serveur.

Dans ce modèle de sécurité, les serveurs gèrent et aident à protéger les objets, les clients obtiennent l’accès aux objets via des serveurs, et les serveurs peuvent tenter d’accéder au client en usurpant l’identité du client.

Le système implémente le protocole d’authentification Kerberos V5 et le package de sécurité Schannel. Il comprend également des fonctionnalités telles que l’emprunt d’identité au niveau du délégué, l’authentification mutuelle, la possibilité de définir des niveaux d’authentification pour une AppID dans le registre et le masquage. À l’aide de la sécurité COM, vous pouvez implémenter des objets qui peuvent effectuer des opérations privilégiées sans compromettre la sécurité.

Étant donné que de nombreuses fonctionnalités de sécurité COM sont disponibles, il est utile de déterminer à l’origine le type de sécurité dont votre application a besoin. Pour la plupart des applications, la définition d’un niveau de sécurité acceptable peut être un processus simple, mais vous pouvez également utiliser la sécurité COM pour prendre en charge des scénarios de sécurité très complexes.

Vous pouvez définir la sécurité échelle à l’aide de Dcomcnfg.exe pour définir le registre ou en appelant [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Deux interfaces principales, [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) et [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) (et les fonctions d’assistance associées), vous permettent de définir la sécurité au niveau des appels au sein de votre programme.

Pour en savoir plus sur la sécurité COM, consultez les rubriques suivantes :

-   [Détermination de vos besoins en matière de sécurité](determining-your-security-needs.md)
-   [Valeurs par défaut de sécurité COM](com-security-defaults.md)
-   [Sécurité d’activation](activation-security.md)
-   [Valeurs de sécurité](security-values.md)
-   [Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
-   [Activation de la sécurité COM à l’aide de DCOMCNFG](enabling-com-security-using-dcomcnfg.md)
-   [Désactivation de la sécurité](turning-off-security.md)
-   [Sécurité côté serveur](server-side-security.md)
-   [Négociation de sécurité permanente](security-blanket-negotiation.md)
-   [Packages COM et de sécurité](com-and-security-packages.md)
-   [améliorations de la sécurité DCOM dans Windows XP service pack 2 et Windows Server 2003 service pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
-   [Listes de Access Control pour COM](access-control-lists-for-com.md)
-   [Moniker d’élévation COM](the-com-elevation-moniker.md)

 

 