---
title: Utilisation de canaux authentifiés sécurisés
description: Utilisation de canaux authentifiés sécurisés
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Gestionnaire de périphériques Windows Media, authentification
- Gestionnaire de périphériques, authentification
- applications de bureau, authentification
- fournisseurs de services, authentification
- Guide de programmation, authentification
- Authentification
- Gestionnaire de périphériques Windows Media, communications sécurisées
- Gestionnaire de périphériques, communications sécurisées
- applications de bureau, communications sécurisées
- fournisseurs de services, communications sécurisées
- Guide de programmation, communications sécurisées
- communications sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028839"
---
# <a name="using-secure-authenticated-channels"></a>Utilisation de canaux authentifiés sécurisés

Windows Media Gestionnaire de périphériques permet l’authentification et la communication sécurisée entre les composants en fournissant deux classes d’assistance, [CSecureChannelClient](csecurechannelclient-class.md) (pour les applications) et [CSecureChannelServer](csecurechannelserver-class.md) (pour les fournisseurs de services), et une interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (pour les deux). Ensemble, ils composent une API pour l’utilisation de canaux authentifiés sécurisés (SAC). SAC gère les trois tâches suivantes pour les fournisseurs de services ou les applications à l’aide de Windows Media Gestionnaire de périphériques :

-   [Authentification du composant](component-authentication.md)
-   [Chiffrement et déchiffrement](encryption-and-decryption.md)
-   [Authentification des messages](message-authentication.md)

Une application ou un fournisseur de services doit gérer l’authentification, le chiffrement et le déchiffrement des composants ; l’authentification des messages est facultative.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Tâches communes aux applications et aux fournisseurs de services**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




