---
title: Structures de méthode homologue EAPHost
description: En savoir plus sur les structures d’API de méthode homologue EAPHost, telles que EapCertificateCredential et EapSimCredential.
ms.assetid: 546ef715-8f51-4f5a-a569-8bf64d52de85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56582c920536cabd294680df265d16ae51d8b4bd951f8efcdb988de677a2a2ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498618"
---
# <a name="eaphost-peer-method-structures"></a>Structures de méthode homologue EAPHost

Les structures de l’API de méthode homologue EAPHost sont les suivantes.



| Structure                                                              | Description                                                                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EapCertificateCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcertificatecredential)           | Contient des informations sur le certificat utilisé par la méthode EAP pour l’authentification.                                                                                                            |
| [**EapCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapcredential)                                 | Contient des informations sur le type d’informations d’identification et les informations d’identification appropriées. Cette valeur est transmise en tant qu’entrée à l’API [**EapPeerGetConfigBlobAndUserBlob**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeergetconfigblobanduserblob) . |
| [**\_ \_ routines de méthode HOMOLOGUe EAP \_**](/windows/desktop/api/eapmethodpeerapis/ns-eapmethodpeerapis-eap_peer_method_routines)        | Contient un ensemble de pointeurs fonction vers les API de méthode homologue EAPHost.                                                                                                                               |
| [**EapPeerMethodOutput**](/windows/win32/api/eapauthenticatoractiondefine/ns-eapauthenticatoractiondefine-eappeermethodoutput)                     | Contient les informations d’action retournées par une méthode homologue EAP.                                                                                                                                    |
| [**EapPeerMethodResult**](/windows/win32/api/eapmethodpeerapis/ns-eapmethodpeerapis-eappeermethodresult)                     | Contient les données de résultat générées par une méthode EAP lors de l’authentification.                                                                                                                             |
| [**EapSimCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapsimcredential)                           | Contient des informations sur la carte SIM qui est utilisée par la méthode EAP pour l’authentification.                                                                                                              |
| [**EapUsernamePasswordCredential**](/windows/desktop/api/eaptypes/ns-eaptypes-eapusernamepasswordcredential) | Contient le nom d’utilisateur et le mot de passe utilisés par la méthode EAP pour authentifier l’utilisateur.                                                                                                     |



 

 

 




