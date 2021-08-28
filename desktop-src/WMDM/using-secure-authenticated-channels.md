---
title: Utilisation de canaux authentifiés sécurisés
description: Utilisation de canaux authentifiés sécurisés
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Gestionnaire de périphériques de média, authentification
- Gestionnaire de périphériques, authentification
- applications de bureau, authentification
- fournisseurs de services, authentification
- Guide de programmation, authentification
- Authentification
- Windows Gestionnaire de périphériques de média, communications sécurisées
- Gestionnaire de périphériques, communications sécurisées
- applications de bureau, communications sécurisées
- fournisseurs de services, communications sécurisées
- Guide de programmation, communications sécurisées
- communications sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a86eb364baca933eea1c81e587f99c9381786c5c3f62f2cefcfe3ceaed6e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124109"
---
# <a name="using-secure-authenticated-channels"></a>Utilisation de canaux authentifiés sécurisés

Windows Le Gestionnaire de périphériques de média permet l’authentification et la communication sécurisée entre les composants en fournissant deux classes d’assistance, [CSecureChannelClient](csecurechannelclient-class.md) (pour les applications) et [CSecureChannelServer](csecurechannelserver-class.md) (pour les fournisseurs de services), et une interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (pour les deux). Ensemble, ils composent une API pour l’utilisation de canaux authentifiés sécurisés (SAC). SAC gère les trois tâches suivantes pour les fournisseurs de services ou les applications à l’aide de Windows Gestionnaire de périphériques de média :

-   [Authentification du composant](component-authentication.md)
-   [Chiffrement et déchiffrement](encryption-and-decryption.md)
-   [Authentification des messages](message-authentication.md)

Une application ou un fournisseur de services doit gérer l’authentification, le chiffrement et le déchiffrement des composants ; l’authentification des messages est facultative.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Tâches communes aux applications et aux fournisseurs de services**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




