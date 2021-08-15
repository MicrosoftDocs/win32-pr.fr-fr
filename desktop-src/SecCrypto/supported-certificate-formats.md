---
description: Répertorie les formats de certificat pris en charge par les services de certificats.
ms.assetid: e6a324d0-9b62-4625-a604-cb1eeca22aae
title: Formats de certificat pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ae0c4d638e957df5ddcf251ca64578a67a58b98890401c68593dd7a12c3952
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897630"
---
# <a name="supported-certificate-formats"></a>Formats de certificat pris en charge

Les services de certificats peuvent émettre les types de certificats suivants.



| Terme                                                                                                                                                                                                                                                                                                                                                                                             | Description                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="X.509_version_3_SSL-compatible_client_authentication_certificate"></span><span id="x.509_version_3_ssl-compatible_client_authentication_certificate"></span><span id="X.509_VERSION_3_SSL-COMPATIBLE_CLIENT_AUTHENTICATION_CERTIFICATE"></span>[*X. 509*](../secgloss/x-gly.md) version 3 certificat d’authentification client compatible SSL<br/> | Ce certificat d’authentification client identifie un client et est utilisé par les serveurs pour authentifier un client qui demande l’accès au serveur.<br/>     |
| <span id="X.509_v3_SSL-compatible_server_authentication_certificate"></span><span id="x.509_v3_ssl-compatible_server_authentication_certificate"></span><span id="X.509_V3_SSL-COMPATIBLE_SERVER_AUTHENTICATION_CERTIFICATE"></span>Certificat d’authentification serveur compatible SSL X. 509 v3<br/>                                                                                         | Ce certificat d’authentification serveur identifie un serveur et est utilisé par les clients pour authentifier un serveur auquel le client souhaite accéder.<br/> |
| <span id="S_MIME_certificate"></span><span id="s_mime_certificate"></span><span id="S_MIME_CERTIFICATE"></span>Certificat [*S/MIME*](../secgloss/s-gly.md)<br/>                                                                                                           | Ce certificat est utilisé par les clients pour la messagerie sécurisée sous le protocole S/MIME (Secure/Multipurpose Internet Mail Extensions).<br/>              |



 

En plus de ces certificats, vous pouvez également utiliser les services de certificats pour émettre d’autres certificats X. 509 en écrivant un module de stratégie personnalisé.

> [!Note]  
> « Certificat d’authentification de serveur » et « certificat de serveur » ainsi que « certificat d’authentification client » et « certificat client » sont des termes interchangeables.

 

En outre, les services de certificats incluent des modèles de certificats dans la configuration de l’autorité de certification d’entreprise Microsoft. consultez la documentation d’aide Windows pour connaître les modèles de certificats pour comprendre comment ils définissent les rôles de certificat.

 

 
