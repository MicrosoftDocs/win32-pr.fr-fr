---
title: CSecureChannelServer, classe
description: CSecureChannelServer, classe
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Gestionnaire de périphériques Windows Media, classe CSecureChannelServer
- Gestionnaire de périphériques, classe CSecureChannelServer
- fournisseurs de services, classe CSecureChannelServer
- Référence de programmation, classe CSecureChannelServer
- référence pour Windows Media Gestionnaire de périphériques, classe CSecureChannelServer
- CSecureChannelServer, classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727877"
---
# <a name="csecurechannelserver-class"></a>CSecureChannelServer, classe

La classe **CSecureChannelServer** est une classe d’assistance (pas une interface) qui permet à un fournisseur de services ou à un fournisseur de contenu sécurisé d’authentifier une application à l’aide de l’interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) , de chiffrer et de déchiffrer des données et de créer des signatures Mac. Le processus d’authentification nécessite que l’application crée un objet **CSecureChannelClient** et que le fournisseur de services crée un objet **CSecureChannelServer** . Les classes **CSecureChannelClient** et **CSecureChannelServer** sont déclarées dans la bibliothèque de liens statiques, Mssachlp. lib. Toutes les méthodes des interfaces du fournisseur de Gestionnaire de périphériques, du fournisseur de services et du fournisseur de contenu sécurisé de Windows Media peuvent retourner WMDM \_ E \_ NOTCERTIFIED pour indiquer que l’appelant ne s’est pas correctement authentifié.

La classe **CSecureChannelServer** expose les méthodes suivantes.



| Méthode                                                            | Description                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**DecryptParam**](/previous-versions/bb231598(v=vs.85))         | Déchiffre les données contenues dans un paramètre.                                                 |
| [**EncryptParam**](/previous-versions/ms868509(v=msdn.10))         | Chiffre les données contenues dans un paramètre.                                                 |
| [**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) | Vérifie qu’un canal d’authentification sécurisé a été établi avec succès.            |
| [**GetAppSec**](/previous-versions/bb231601(v=vs.85))               | Récupère les niveaux de sécurité de l’application des composants locaux et distants.               |
| [**GetSessionKey**](/previous-versions/bb231602(v=vs.85))       | Récupère la clé de session active.                                                          |
| [**MACFinal**](/previous-versions/ms868513(v=msdn.10))                 | Libère le canal de code d’authentification de message (MAC) et récupère une valeur MAC finale.     |
| [**MACInit**](/previous-versions/ms868514(v=msdn.10))                   | Acquiert un canal MAC (Message Authentication Code).                                       |
| [**MACUpdate**](/previous-versions/ms868515(v=msdn.10))               | Met à jour la valeur du code d’authentification de message (MAC) avec une valeur de paramètre.                 |
| [**SACAuth**](/previous-versions/ms868516(v=msdn.10))                   | Établit un canal authentifié sécurisé entre les composants.                              |
| [**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))   | Signale les protocoles pris en charge par un composant.                                             |
| [**SetCertificate**](/previous-versions/ms868518(v=msdn.10))     | Spécifie le certificat et la clé privée du serveur de canal authentifié (SAC) sécurisé. |
| [**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))       | Définit la clé de session utilisée pour communiquer avec un autre composant.                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**CSecureChannelClient, classe**](csecurechannelclient-class.md)
</dt> <dt>

[**Interface IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfaces pour les fournisseurs de services**](interfaces-for-service-providers.md)
</dt> <dt>

[**Utilisation de canaux authentifiés sécurisés**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 