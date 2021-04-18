---
title: CSecureChannelClient, classe
description: CSecureChannelClient, classe
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Gestionnaire de périphériques Windows Media, classe CSecureChannelClient
- Gestionnaire de périphériques, classe CSecureChannelClient
- applications de bureau, classe CSecureChannelClient
- Référence de programmation, classe CSecureChannelClient
- référence pour Windows Media Gestionnaire de périphériques, classe CSecureChannelClient
- CSecureChannelClient, classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512319"
---
# <a name="csecurechannelclient-class"></a>CSecureChannelClient, classe

La classe **CSecureChannelClient** est une classe d’assistance (et non une interface) qui permet aux applications de s’authentifier, de chiffrer et de déchiffrer des données et de créer des Mac.

La classe **CSecureChannelClient** expose les méthodes suivantes.



| Méthode                                                            | Description                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Authenticate**](/previous-versions/ms983906(v=msdn.10))         | Déclenche l’échange de certificats entre les composants pour établir l’approbation.                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | Déchiffre les données reçues par le biais d’un paramètre.                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | Chiffre les données envoyées par le biais d’un paramètre.                                                                         |
| [**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10)) | Vérifie qu’un canal d’authentification sécurisé a été établi avec succès. Cette méthode n’est pas utilisée par les applications. |
| [**GetAppSec**](/previous-versions/ms868498(v=msdn.10))               | Récupère les niveaux de sécurité de l’application des composants locaux et distants.                                             |
| [**GetSessionKey**](/previous-versions/bb231590(v=vs.85))       | Récupère la clé de session active. Cette méthode n’est pas utilisée par les applications.                                               |
| [**MACFinal**](/previous-versions/bb231591(v=vs.85))                 | Libère le canal de code d’authentification de message (MAC) et récupère une valeur MAC finale.                                   |
| [**MACInit**](/previous-versions/bb231592(v=vs.85))                   | Acquiert un canal MAC (Message Authentication Code).                                                                     |
| [**MACUpdate**](/previous-versions/bb231593(v=vs.85))               | Ajoute une valeur à un code d’authentification de message (MAC).                                                                      |
| [**SetCertificate**](/previous-versions/ms868504(v=msdn.10))     | Spécifie le certificat et la clé privée du client de canal authentifié (SAC) sécurisé.                               |
| [**SetInterface**](/previous-versions/bb231595(v=vs.85))         | Sélectionne l’interface utilisée pour sécuriser les communications de canal authentifié (SAC).                                         |
| [**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))       | Définit la clé de session utilisée pour communiquer avec un autre composant. Cette méthode n’est pas utilisée par les applications.         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CSecureChannelServer, classe**](csecurechannelserver-class.md)
</dt> <dt>

[**Interface IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfaces pour les applications**](interfaces-for-applications.md)
</dt> </dl>

 

 