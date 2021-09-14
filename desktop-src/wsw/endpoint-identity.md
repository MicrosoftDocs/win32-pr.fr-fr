---
title: Identité du point de terminaison
description: Les types définis dans cette section sont utilisés pour définir l’identité de sécurité d’une adresse de point de terminaison.
ms.assetid: 39639b9a-32e2-44d2-9bda-a2ad23850de8
keywords:
- Services Web d’identité de point de terminaison pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7a3f7b95d5fc1b926d8bafb49b06f96c7d68fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230838"
---
# <a name="endpoint-identity"></a>Identité du point de terminaison

Les types définis dans cette section sont utilisés pour définir l’identité de sécurité d’une adresse de point de terminaison.

Les éléments d’API suivants font partie de la mise en retrait du point de terminaison :



| Énumération                                                       | Description                                                                                                                   |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**TYPE d’identité du point de \_ terminaison WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_endpoint_identity_type) | Type de l’identité du point de terminaison, utilisé comme sélecteur pour les sous-types de l' [**\_ \_ identité du point de terminaison WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity). |



 



| Structure                                                               | Description                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_identité du \_ point de terminaison du certificat WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_endpoint_identity)       | Type de l’identité du point de terminaison du certificat.                                                 |
| [**\_identité du \_ point de terminaison WS DNS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_dns_endpoint_identity)         | Type pour la spécification d’une identité de point de terminaison représentée par un nom DNS.                      |
| [**\_identité du point de terminaison WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_identity)                  | Type de base pour toutes les identités de point de terminaison.                                                   |
| [**\_identité du \_ point de terminaison WS RSA \_**](/windows/desktop/api/WebServices/ns-webservices-ws_rsa_endpoint_identity)         | Type de l’identité du point de terminaison RSA.                                                              |
| [**\_identité du \_ point de terminaison WS SPN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_spn_endpoint_identity)         | Type pour la spécification d’une identité de point de terminaison représentée par un SPN (nom de principal du service). |
| [**\_identité du \_ point de terminaison WS inconnue \_**](/windows/desktop/api/WebServices/ns-webservices-ws_unknown_endpoint_identity) | Type pour une identité de point de terminaison inconnue.                                                   |
| [**\_identité du \_ point de terminaison UPN WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_upn_endpoint_identity)         | Type pour la spécification d’une identité de point de terminaison représentée par un UPN (nom d’utilisateur principal).     |



 

 

 




