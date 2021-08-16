---
title: Informations d'identification de sécurité
description: Les informations d’identification de sécurité sont un élément de preuve qu’une partie communicante possède qui peut être utilisée pour créer ou obtenir un jeton de sécurité.
ms.assetid: 70e260ce-9e45-436f-b6d1-b650a5c9c0e9
keywords:
- Services Web des informations d’identification de sécurité pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f5703d9f58e7fee57f1ce8465e0413a7ca3c246590b816e84f7419e80f6efb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192760"
---
# <a name="security-credentials"></a>Informations d'identification de sécurité

Les informations d’identification de sécurité sont un élément de preuve qu’une partie communicante possède qui peut être utilisée pour créer ou obtenir un jeton de sécurité. Ainsi, les informations d’identification sont généralement plus longues que les jetons de sécurité, et un jeton de sécurité peut être affiché en tant que manifeste d’exécution des informations d’identification de sécurité. Voici un exemple d’informations d’identification : un certificat d’ordinateur (qui peut être converti en un jeton de sécurité X. 509 au moment de l’exécution) ou une paire nom d’utilisateur/mot de passe pour un domaine (qui peut être utilisé pour obtenir un jeton de sécurité Kerberos).


Les informations d’identification sont spécifiées dans le cadre des [liaisons de sécurité](security-bindings.md).

Les éléments d’API suivants sont utilisés avec les informations d’identification de sécurité.

| Rappel                                                                  | Description                                              |
|---------------------------------------------------------------------------|----------------------------------------------------------|
| [**le \_ \_ rappel du certificat \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)                   | Fournit un certificat au runtime de sécurité.          |
| [**le \_ \_ rappel de mot de passe WS Validate \_**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback) | Valide une paire nom d’utilisateur/mot de passe côté récepteur. |



 



| Énumération                                                                                           | Description                                                   |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [**\_ \_ type d’informations d’identification WS CERT \_**](/windows/desktop/api/WebServices/ne-webservices-ws_cert_credential_type)                                         | Type des informations d’identification du certificat.                       |
| [**\_ \_ type d’informations d’identification WS username \_**](/windows/desktop/api/WebServices/ne-webservices-ws_username_credential_type)                                 | Type des informations d’identification du nom d’utilisateur/mot de passe.                 |
| [**\_ \_ \_ \_ type d’informations d’identification de l’authentification intégrée WS Windows \_**](/windows/desktop/api/WebServices/ne-webservices-ws_windows_integrated_auth_credential_type) | type de l’Windows informations d’identification d’authentification intégrées. |



 



| Structure                                                                                                   | Description                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ informations d’identification WS CERT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_credential)                                                          | Type de base abstrait pour tous les types d’informations d’identification de certificat.                                                          |
| [**\_ \_ informations d’identification du certificat personnalisé WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_cert_credential)                                           | Type pour spécifier les informations d’identification de certificat qui doivent être fournies par un rappel à l’application.             |
| [**\_ \_ \_ \_ informations d’identification de l’authentification intégrée Windows WS par défaut \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_windows_integrated_auth_credential) | Type pour fournir une Windows informations d’authentification intégrée basées sur le jeton de thread actuel.                  |
| [**\_ \_ \_ \_ informations d’identification de l’authentification intégrée Windows WS opaque \_**](/windows/desktop/api/WebServices/ns-webservices-ws_opaque_windows_integrated_auth_credential)   | Type pour fournir une Windows informations d’identification d’authentification intégrée.                                                    |
| [**\_ \_ informations d’identification du nom d’utilisateur WS String \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_username_credential)                                   | Type pour fournir une paire nom d’utilisateur/mot de passe sous forme de chaînes.                                                           |
| [**\_ \_ \_ \_ \_ informations d’identification d’authentification intégrée Windows WS String**](/windows/desktop/api/WebServices/ns-webservices-ws_string_windows_integrated_auth_credential)   | Type permettant de fournir un Windows informations d’identification sous forme de nom d’utilisateur, de mot de passe et de domaine.                                        |
| [**\_ \_ \_ informations d’identification du certificat WS subject name \_**](/windows/desktop/api/WebServices/ns-webservices-ws_subject_name_cert_credential)                              | Type pour la spécification d’informations d’identification de certificat à l’aide du nom d’objet du certificat, de l’emplacement du magasin et du nom du magasin. |
| [**\_ \_ informations d’identification du certificat WS empreinte \_**](/windows/desktop/api/WebServices/ns-webservices-ws_thumbprint_cert_credential)                                   | Type permettant de spécifier des informations d’identification de certificat à l’aide de l’empreinte numérique du certificat, de l’emplacement du magasin et du nom du magasin.   |
| [**\_ \_ informations d’identification WS username**](/windows/desktop/api/WebServices/ns-webservices-ws_username_credential)                                                  | Type de base abstrait pour toutes les informations d’identification de nom d’utilisateur/mot de passe.                                                         |
| [**\_ \_ \_ informations d’identification de l’authentification intégrée WS Windows \_**](/windows/desktop/api/WebServices/ns-webservices-ws_windows_integrated_auth_credential)                  | type de base abstrait pour tous les types d’informations d’identification utilisés avec l’authentification intégrée Windows.                          |



 

 

 




