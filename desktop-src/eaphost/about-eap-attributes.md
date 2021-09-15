---
title: Attributs EAP
description: Est une \_ structure d’attribut EAP qui contient un type de données prédéterminé relatif à une session d’authentification.
ms.assetid: 3c54cca2-cd3b-4149-bb0e-036d490cdd3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5348ee300c0e4d07d6aaf110ba9074b1ac32c02a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519748"
---
# <a name="eap-attributes"></a>Attributs EAP

Un attribut EAP est une structure d' [**\_ attributs EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute) qui contient un type de données prédéterminé relatif à une session d’authentification. Les attributs sont utilisés pour communiquer des informations entre les méthodes EAP et les demandeurs ou entre les méthodes et les authentificateurs EAP. Les implémentations d’homologue et d’authentificateur d’une méthode EAP peuvent échanger ces attributs sur un réseau.

La liste complète des types d’attributs pris en charge s’affiche dans la rubrique [**\_ \_ type d’attribut EAP**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type).

## <a name="attributes-consumed-by-supplicants"></a>Attributs consommés par les demandeurs

Les types d’attributs suivants sont consommés par les demandeurs 802.1 X.

-   **eatVendorSpecific**

Les types d’attributs suivants sont consommés par les demandeurs clients PPP.

-   **eatMinimum**
-   **eatEAPTLV**

Les types d’attributs suivants sont consommés par les demandeurs de serveur PPP.

-   **eatUserName**
-   **eatReplyMessage**
-   **eatState**
-   **eatSessionTimeout**
-   **eatEAPMessage**

## <a name="attributes-exported-by-methods"></a>Attributs exportés par des méthodes

Les types d’attributs suivants peuvent être exportés par les méthodes EAP.

-   **eatClearTextPassword**
-   **eatQuarantineSoH**
-   **eatMethodId**

Le type d’attribut suivant est exporté par les méthodes TLS (EAP [Transport Level Security)](/previous-versions/windows/embedded/ms885336(v=msdn.10)) (EAP-TLS).

-   **eatCertificateOID**

Les types d’attributs suivants sont exportés par les méthodes [Microsoft Challenge Handshake Authentication Protocol version 2,0](/previous-versions/windows/embedded/ms899190(v=msdn.10)) (MS-CHAPv2).

-   **eatUserName**
-   **eatCredentialsChanged**

Le type d’attribut suivant est consommé par le serveur NPS (Network Policy Server).

-   **eatCertificateOID**

Les types d’attributs suivants sont exportés par les méthodes [PEAP (Protected Extensible Authentication Protocol)](/previous-versions/windows/embedded/ms899190(v=msdn.10)) .

-   **eatUserName**
-   **eatPEAPEmbeddedEAPTypeId**
-   **eatPEAPFastRoamedSession**
-   **eatQuarantineSoH**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_attribut EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)
</dt> <dt>

[**\_type d’attribut EAP \_**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_attribute_type)
</dt> </dl>

 

 