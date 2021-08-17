---
title: Structures du demandeur EAPHost
description: En savoir plus sur les structures d’API du demandeur EAPHost, telles que la \_ demande EAP cred \_ et le tableau des propriétés de la \_ méthode EAP \_ \_ .
ms.assetid: 77595f36-140d-4d8e-af8e-63e9de0031c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6703070eabbc571927569f28c39109bbe1eda2f1c70b621982dde3ab4ac3a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117904616"
---
# <a name="eaphost-supplicant-structures"></a>Structures du demandeur EAPHost

Les structures de l’API du demandeur EAPHost sont les suivantes.



| Structure                                                                        | Description                                                                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**\_demande EAP cred \_**](eap-cred-req.md)                                           | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations de modification des informations d’identification.                                    |
| [**réponse d’identification EAP \_ \_**](eap-cred-resp.md)                                         | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations de modification des informations d’identification.                                    |
| [**demande d’expiration d’un \_ cred EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)                            | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations d’expiration des informations d’identification                                     |
| [**réponse d’expiration d’un \_ cred EAP \_ \_**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))                      | Contient les informations d’identification EAP anciennes et nouvelles pour les opérations d’expiration des informations d’identification.                                    |
| [**\_ \_ demande d’ouverture de session EAP cred \_**](eap-cred-logon-req.md)                              | Contient les informations d’identification EAP pour l’authentification réseau.                                                                 |
| [**\_ \_ réponse d’ouverture de session EAP cred \_**](eap-cred-logon-resp.md)                            | Contient les informations d’identification EAP pour l’authentification réseau.                                                                 |
| [**\_données de \_ l’interface utilisateur interactive EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)                    | Contient des informations de configuration pour les composants d’interface utilisateur interactifs déclenchés sur un demandeur EAP.            |
| [**\_propriété de méthode EAP \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property)                             | Windows 7 ou version ultérieure : représente une propriété de méthode.                                                                    |
| [**Tableau des propriétés de la \_ méthode EAP \_ \_**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_array)                | Windows 7 ou version ultérieure : contient un tableau de structures de propriétés de méthode.                                                 |
| [**valeur de la propriété de la \_ méthode EAP \_ \_**](/previous-versions/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value)                | Windows 7 ou version ultérieure : contient une valeur de propriété de méthode.                                                                |
| [**valeur de propriété de la \_ méthode EAP \_ \_ \_ bool**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_bool)     | Windows 7 ou version ultérieure : contient une valeur de propriété de méthode de type de données BOOL.                                                 |
| [**valeur de propriété de la \_ méthode EAP \_ \_ \_ DWORD**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_dword)   | Windows 7 ou version ultérieure : contient une valeur de propriété de méthode de type de données DWORD.                                                |
| [**\_chaîne de \_ valeur de propriété \_ \_ de la méthode EAP**](/windows/desktop/api/EapTypes/ns-eaptypes-eap_method_property_value_string) | Windows 7 ou version ultérieure : contient une valeur de propriété de méthode de type de données string.                                               |
| [**\_informations d’authentification EAPHOST \_**](/windows/desktop/api/eaphostpeertypes/ns-eaphostpeertypes-eaphost_auth_info)                                 | Décrit les informations d’authentification actuelles au cours des différentes étapes du processus d’authentification EAP.          |
| [**EapHostPeerMethodResult**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                       | Contient les données de résultat générées par EAPHost au cours d’une session d’authentification qui est ensuite transmise à une méthode EAP. |
| [**EapHostPeerNapInfo**](/windows/win32/api/eaphostpeertypes/ns-eaphostpeertypes-eaphostpeermethodresult)                            | Windows 7 ou version ultérieure : contient les informations de Protection d’accès réseau (NAP) sur un demandeur EAP.                   |



 

 

 